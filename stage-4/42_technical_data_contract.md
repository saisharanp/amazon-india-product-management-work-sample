# Stage 4 — Technical and Data Contract

**Product:** Amazon India
**Feature:** Unified exception resolution — delivered but not received
**Purpose:** Define the interface between delivery events, case orchestration, recovery policy, customer surfaces, support, and analytics.

## 1. Canonical exception case

```json
{
  "case_id": "EX-49281",
  "exception_type": "DELIVERED_NOT_RECEIVED",
  "order_id": "123-4567890-1234567",
  "delivery_id": "DLV-8842",
  "customer_state": "RECOVERY_AVAILABLE",
  "state_reason": "Delivery scan exists but customer reported non-receipt",
  "owner": {"type": "QUEUE", "display_label": "Amazon Delivery Support"},
  "next_update_at": "2026-08-09T18:00:00+05:30",
  "recovery_options": ["DELIVERY_RETRY", "REPLACEMENT", "REFUND"],
  "selected_recovery": null,
  "last_updated_at": "2026-08-09T10:45:00+05:30",
  "version": 3,
  "audit_reference": "AUD-49281-03"
}
```

`case_id`, `order_id`, and `delivery_id` are identifiers only. Payment credentials, full address, and unnecessary personal data do not belong in the customer-facing contract.

## 2. Normalized customer states

| State | Entry condition | Exit condition | Source of truth |
|---|---|---|---|
| `EXCEPTION_DETECTED` | Non-receipt report accepted | Owner/SLA assigned or safe fallback | Case orchestration |
| `WAITING_ON_PARTNER` | Partner evidence is required | Evidence received or escalation rule fires | Case orchestration + delivery |
| `RECOVERY_AVAILABLE` | Eligible options are calculated | Selection accepted or case escalated | Policy decision record |
| `RESOLUTION_IN_PROGRESS` | Recovery request accepted | Confirmation event received | Recovery workflow |
| `RESOLVED` | Confirmed delivery, refund settlement, or replacement confirmation | Policy-based reopen | Case orchestration |

Internal event names may be richer, but the customer state can only be one of the normalized values above.

## 3. Event contract

| Field | Required | Definition |
|---|---|---|
| `event_id` | Yes | Globally unique event identifier |
| `event_type` | Yes | Source event name; retained for audit, not customer copy |
| `case_id` | Yes after case creation | Canonical exception case |
| `order_id` | Yes | Amazon order identifier |
| `delivery_id` | Required for delivery events | Delivery identifier |
| `occurred_at` | Yes | When the source event happened |
| `received_at` | Yes | When orchestration received it |
| `source_system` | Yes | Delivery, support, policy, inventory, payment, or notification |
| `source_version` | Yes | Version of the source payload |
| `dedupe_key` | Yes | Stable key for idempotent processing |
| `confidence` | Conditional | Source confidence when available |
| `visibility` | Yes | `CUSTOMER`, `AGENT`, or `AUDIT_ONLY` |

### Idempotency

The orchestration layer must deduplicate on `dedupe_key` and retain the first accepted source event plus later corrections. Customer actions use a client-generated request key scoped to `case_id` and action type.

## 4. Source authority and conflict handling

| Data element | Authoritative system | Fallback behavior |
|---|---|---|
| Delivery scan | Delivery event service | Show investigation state if event freshness or confidence fails |
| Case owner and SLA | Support case workflow | Show fallback contact path if absent |
| Recovery eligibility | Policy decision service | Do not show selectable options on timeout |
| Replacement availability | Inventory service | Recalculate at confirmation; show unavailable if changed |
| Refund initiation | Payment/refund workflow | Show processing state, never settled |
| Refund settlement | Payment settlement record | Keep case in progress until confirmation |

When sources conflict, the customer surface uses the safest normalized state, records the conflict for agents, and emits `case_data_conflict_detected` for monitoring.

## 5. Customer read model

The order page consumes a read model with:

- current normalized state and human-readable message;
- timeline entries with customer-safe labels and timestamps;
- owner display label and `next_update_at` when available;
- eligible recovery options with outcome, amount, and expected date;
- selected recovery and confirmed outcome;
- support and reopen actions;
- `case_version` for stale-write protection.

Writes must be accepted by the case orchestration boundary, not directly by the customer surface.

## 6. State transition rules

- A case may move forward only when the transition event is valid for the current version.
- A stale write returns the current case state and requires the client to refresh.
- `RESOLVED` requires a confirmation event from the relevant delivery, payment, or replacement workflow.
- Reopen creates an auditable child action linked to the original case; it does not erase the prior resolution.
- Any unhandled exception routes to support and preserves the last safe customer state.

## 7. Observability

Required operational measures: event freshness, conflict rate, case-creation success, state-transition rejection, recovery eligibility latency, duplicate-action rate, SLA breach rate, notification mismatch rate, and customer/agent read-model divergence.

Required analytics events: `exception_viewed`, `timeline_expanded`, `recovery_option_viewed`, `recovery_option_selected`, `case_owner_viewed`, `next_update_viewed`, `support_contact_started`, `case_reopened`, `refund_status_viewed`, `recovery_completed`, and `recovery_feedback_submitted`.
