# Stage 6 — Operating Metrics and Alerts

## Measurement principles

- Use `case_id` as the join key across order, delivery, payment, support, notification, and recovery events.
- Separate baseline/control, pilot exposure, fallback, and excluded cohorts.
- Report both aggregate results and sampled case accuracy; an average cannot hide an unsafe individual outcome.
- Do not populate actuals from the Stage 5 synthetic replay.

## Metric contract

| Metric | Type | Definition | Target / threshold | Action if breached |
|---|---|---|---|---|
| Repeat contacts per case | Primary | Support contacts after the first exception case is opened | Improve versus baseline | Iterate if no meaningful improvement |
| Confirmed-resolution time | Primary | Hours from case creation to authoritative outcome | Improve versus baseline | Iterate if slower without a safety benefit |
| Understood-next rate | Customer | Share of sampled customers who can identify the next action | ≥ 75% in research/pilot sample | Fix copy or flow before expansion |
| Recovery completion rate | Customer | Eligible customers completing the chosen safe recovery path | Improve versus baseline | Investigate eligibility, trust, or UX failure |
| Incorrect recovery rate | Guardrail | Recovery outcome conflicts with policy or authoritative truth | 0 tolerated | Pause and investigate immediately |
| False final outcome | Guardrail | Customer is told the issue is final before authoritative confirmation | 0 tolerated | P0 rollback |
| Duplicate financial action | Guardrail | More than one refund/credit/replacement action for the same case | 0 tolerated | P0 rollback and reconciliation |
| Event conflict rate | Data quality | Cases with contradictory or stale source events | ≤ 5% pilot ceiling | Pause or narrow exposure |
| SLA breach rate | Operations | Cases exceeding the published confirmation/recovery SLA | ≤ 20% unless baseline is worse and approved | Iterate or hold expansion |
| Support handle time | Operations | Average support handling time for exposed cases | No >15% increase | Hold expansion; improve tooling |
| Case-linkage completeness | Data quality | Exposed cases with complete `case_id` event chain | ≥ 95% | No decision until fixed |
| Reopen rate | Customer/quality | Resolved cases reopened for the same exception | Improve versus baseline | Iterate before scale |

## Alert levels

| Severity | Trigger | Response |
|---|---|---|
| P0 | Duplicate financial action, false final outcome, privacy exposure, or unsafe customer harm | Disable new exposure immediately; notify incident lead, Payments, Engineering, Product, and Support |
| P1 | Incorrect recovery, material source conflict, or widespread missed SLA | Pause expansion; route affected cases to support; root-cause review within one business day |
| P2 | Copy confusion, isolated stale update, or non-critical instrumentation gap | Assign owner and due date; review next operating day |

## Required dashboard slices

At minimum, segment by delivery region, promise type, seller/fulfilment path, payment method where permitted, exception subtype, new versus repeat customer, and pilot/control cohort. Suppress or aggregate slices that create privacy risk or insufficient sample sizes.

## Review questions

1. Did the customer get a more truthful and actionable explanation?
2. Did the proposed recovery match policy and the authoritative outcome?
3. Did the feature reduce repeat contacts without shifting work to Support?
4. Are missing events or conflicting sources large enough to make the result unreliable?
5. Is there a safe, tested rollback path for every exposed case?
