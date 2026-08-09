# Stage 4 — Product Requirements Document

**Product:** Amazon India
**Feature:** Unified exception resolution — delivered but not received
**Status:** Ready for cross-functional review
**Decision owner:** Product Management

## 1. Product decision

Build a customer-facing resolution layer on the existing order-detail experience. When a customer reports non-receipt after a delivery scan, Amazon should create or retrieve one case, explain the current state, identify the accountable owner or queue, show the next update time, and present a policy-validated recovery path or human escalation. The layer must not independently execute a refund or replacement.

## 2. Problem

Customers can see a delivery event without having the item. The current failure mode makes them reconstruct what happened across order tracking, notifications, and support contacts. This creates uncertainty, repeated explanations, inconsistent answers, and low confidence in refund or replacement outcomes.

Stage 1 feedback analysis identified post-purchase exception clarity, ownership, and recovery as the strongest opportunity signal. Stage 2 selected delivered-but-not-received as the bounded MVP. Stage 3 validated the Exception Timeline and Recovery Hub as the best concept and identified event consistency as the primary risk.

## 3. Target users

### Primary

Discovery users are trust-sensitive customers who report non-receipt after a delivered scan, especially frequent buyers, Prime members, high-value orders, remote-area deliveries, and time-sensitive purchases.

The first pilot is narrower: eligible cases with reliable event linkage in one approved delivery region or fulfilment context, balanced for Prime/non-Prime representation. Fraud investigations, unresolved identity/payment risk, high-value cases above the approved policy threshold, and policy-ambiguous cases are excluded from automated recovery.

### Secondary

Support agents and delivery operations teams who need one shared case state to avoid conflicting updates and repeated handoffs.

## 4. Hypothesis

If Amazon shows one accurate exception timeline, one accountable owner, and one next-update promise for eligible delivered-but-not-received cases, then the percentage of cases reaching confirmed resolution within the promised SLA will improve without increasing unsafe recovery or support burden.

## 5. Goals and non-goals

### Goals

- Make the exception visible from the affected order page.
- Explain the current customer-readable state and what is still being checked.
- Create one case ID and owner/queue shared across customer and support views.
- Show the next update time when an SLA exists.
- Offer policy-validated recovery options with amount, date, and outcome visible, or route to human review.
- Close the loop with confirmed delivery, replacement, or refund status.
- Instrument the journey for E1–E5 validation and pilot decisions.

### Non-goals

- Rebuild delivery-event capture or handoff evidence infrastructure.
- Create a new refund, replacement, or delivery policy.
- Cover every exception type in the first release.
- Replace the complete support-agent console.
- Predict exceptions before the customer reports them.
- Change marketplace search, seller quality, or checkout flows.

## 6. MVP journey

1. Delivery is marked delivered; customer reports non-receipt from the order page.
2. Amazon creates or retrieves a single exception case.
3. The order page shows an exception banner: what happened, what Amazon is checking, and the next update time.
4. Customer opens the timeline with normalized events, owner/queue, and current state.
5. When policy and evidence allow, customer sees an eligible recovery choice; otherwise the case routes to human support.
6. Customer selects a policy-validated option; Amazon confirms eligibility and records the selection idempotently.
7. Customer sees recovery-in-progress status, amount/date or delivery date, and the case owner.
8. Amazon confirms the authoritative outcome, records recovery feedback, and allows policy-based reopen.

## 7. Customer-visible state model

| State | Customer meaning | Customer message | Allowed action |
|---|---|---|---|
| Exception detected | Delivery evidence needs review | “We’re checking an issue with this delivery.” | View timeline; wait for update |
| Waiting on partner | Courier or partner evidence is pending | “We need one more update. Next update by…” | Provide information; contact support |
| Recovery available | A safe recovery path is ready | “Choose how you’d like us to resolve this.” | Select eligible option |
| Resolution in progress | Selected outcome is executing | “Your refund/replacement is being processed.” | View amount/date; contact support |
| Resolved | Outcome is confirmed | “This case is resolved.” | View details; reopen within policy |

## 8. Business rules

- A case is uniquely identified by `case_id`; retrying the same customer action must not create a duplicate case or recovery request.
- A case is created or retrieved only after the customer reports non-receipt from the affected order or an agent records that report.
- The customer sees normalized event labels, not internal queue names, raw scan codes, or contradictory source records.
- Each customer-visible state has an authority map. A delivery scan proves a scan occurred, not that the customer received the package.
- When authoritative sources conflict, show an honest investigation state, preserve the last safe state, record the conflict for agents, and route ambiguous cases to human support.
- A displayed next-update time must map to an active owner and SLA; if the SLA is unavailable, show “We’ll update you when we know more” and provide support access.
- Recovery options must be calculated from the existing policy and payment/inventory truth. The experience must not invent eligibility.
- High-value, deadline-sensitive, suspected fraud, policy ambiguity, repeated-claim, or repeated-SLA-breach cases must route to human support.
- The first pilot does not independently execute financial recovery; it presents existing policy decisions and records customer intent for the owning workflow.
- Refund initiated and refund settled are separate states; the customer-facing copy must distinguish them.
- Every resolution must include a reason, owner, timestamp, and source record for audit.

## 9. Success metrics

### Primary

- Confirmed resolution within promised SLA: increase versus matched baseline or holdout.

### Secondary

- Repeat contacts per exception case: reduce versus matched baseline.
- Time to confirmed resolution: reduce versus matched baseline.
- Recovery completion rate: increase without guardrail breach.

### Customer

- 80% of usability participants identify the current state correctly.
- 80% identify the next action without facilitator help.
- 75% find owner and next-update time.
- 75% select an eligible recovery path.
- Post-resolution agreement with “I understood what would happen next.”

### Guardrails

- Incorrect recovery decisions.
- False final outcome.
- Duplicate financial action.
- Source conflict rate.
- False-positive exception cases.
- Unresolved cases beyond SLA.
- Support handle time and transfer count.
- Case reopen rate and notification opt-out rate.

## 10. Dependencies

Delivery event normalization and authority map; order and delivery identifiers; support case workflow; recovery policy; inventory availability; refund initiation and settlement status; notification service; analytics pipeline; accessibility review; support training; operations SLA definition; approved pilot cohort and comparison design.

## 11. Approval gate

Approve this PRD when Product, Support Operations, Delivery, Payments, Analytics, and Engineering agree on the delivered-but-not-received MVP boundary, canonical state model, authority map, pilot cohort, comparison design, and guardrail thresholds. No scale decision is valid until event accuracy, policy safety, support capacity, and confirmed-resolution-within-SLA evidence pass the release-readiness checklist.
