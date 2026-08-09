# Stage 3 — Service Blueprint

**Solution direction:** Delivered-but-not-received exception timeline and recovery hub
**Status:** Awaiting approval

## Blueprint

| Customer action | Customer-facing experience | Frontstage people/process | Backstage capability | Systems/data | Failure risk |
|---|---|---|---|---|---|
| Opens delivered order | Exception banner with plain-language status and report action | Help entry point and issue classification | Create or retrieve case after customer report | Order and delivery events | Wrong or stale status |
| Reads timeline | Event sequence with confidence and timestamps | Support can see same timeline | Reconcile events and normalize labels | Event bus, delivery scans, case record | Conflicting timestamps |
| Reports issue | One-tap non-receipt action | Case created with priority | Route to correct queue and preserve case ID | Support CRM, order ID, delivery ID | Case not routed |
| Reviews options | Policy-validated recovery choice or human-review path | Eligibility explanation | Apply policy and inventory/payment rules; no independent financial execution | Policy engine, inventory, payments | Incorrect eligibility |
| Tracks case | Owner/queue and next update time | Agent updates shared case state | SLA and escalation automation | Case workflow, notifications | Missed SLA |
| Receives outcome | Outcome, amount, date, and next step | Support closes or escalates | Confirm settlement or replacement | Refund, replacement, delivery systems | Outcome marked complete too early |
| Rates recovery | Short recovery feedback prompt | Feedback linked to incident | Aggregate outcome and learnings | Survey, analytics, support data | Feedback not tied to root cause |

## Customer-visible state model

| State | Meaning | Customer message | Allowed action |
|---|---|---|---|
| On track | Expected event is progressing | “Your order is on track for delivery by…” | Track order |
| Exception detected | Customer report is accepted and evidence needs investigation | “We’re checking an issue with this delivery.” | View timeline; get update time; contact support |
| Recovery available | A policy-backed option is ready | “Choose an available way to resolve this.” | Select option or contact support |
| Waiting on partner | Amazon needs courier/seller/payment evidence | “We need one more update; next update by…” | Provide information; contact support |
| Resolution in progress | Chosen action is executing | “Your refund/replacement is being processed.” | View amount/date |
| Resolved | Outcome is confirmed | “This case is resolved.” | Reopen within policy; rate recovery |

## Operating model

- **Product:** owns customer experience, event vocabulary, and measurement.
- **Operations:** owns exception policy, escalation rules, and service-level thresholds.
- **Delivery/logistics:** owns event accuracy, handoff evidence, and partner data.
- **Support:** owns case resolution and agent adherence.
- **Payments:** owns refund status, deductions, and settlement accuracy.
- **Analytics:** owns event instrumentation and outcome reporting.

## Blueprint decisions for validation

1. Which system is authoritative for each event?
2. What minimum evidence is needed to show “delivered” with confidence?
3. Which cases require a human owner versus a policy-validated recovery path?
4. What is the customer promise when an SLA is missed?
5. Which state changes should trigger proactive notification?
