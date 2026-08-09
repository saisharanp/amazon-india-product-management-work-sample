# Stage 4 — Release Readiness and Risks

**Product:** Amazon India
**Feature:** Unified exception resolution — delivered but not received

## Launch checklist

| Area | Ready when | Evidence | Owner | Status |
|---|---|---|---|---|
| Product scope | MVP and non-goals are approved | Signed PRD | Product | Not started |
| Policy safety | Eligibility and escalation rules pass scenario review | Policy test results | Operations | Not started |
| Event accuracy | Authority, freshness, and conflict behavior pass | Shadow-mode report | Delivery/Engineering | Not started |
| Case integrity | Duplicate reports and stale writes are safe | Idempotency tests | Engineering | Not started |
| Recovery integrity | Refund, replacement, and delivery outcomes are confirmed correctly | End-to-end test evidence | Payments/Inventory | Not started |
| Customer usability | E1/E2 thresholds pass | Research readout | UX Research | Not started |
| Support readiness | Queue, SLA, scripts, and training are complete | Training sign-off | Support Operations | Not started |
| Accessibility | Screen-reader, contrast, keyboard, and localization checks pass | Accessibility review | Design/QA | Not started |
| Measurement | Baseline, events, dashboard, alerts, and cohort assignment work | Analytics validation | Analytics | Not started |
| Rollback | Feature flag and fallback path are tested | Rollback drill | Engineering/Product | Not started |

## Risk register

| ID | Risk | Trigger | Mitigation | Owner | Decision rule |
|---|---|---|---|---|---|
| R1 | Delivery and support states disagree | Conflict rate exceeds agreed guardrail | Use safest normalized state; route to support; fix authority mapping | Engineering | Pause exposure if customer copy is wrong |
| R2 | Refund or replacement is shown as complete too early | Confirmation event missing or delayed | Separate initiated/in-progress/settled states; block `RESOLVED` | Payments | Stop automated resolution on mismatch |
| R3 | Customers choose an ineligible recovery | Eligibility changes between display and confirmation | Recalculate at confirmation and show clear fallback | Operations | No scale if incorrect recovery is material |
| R4 | Case duplicates increase contact noise | Duplicate case or action keys observed | Enforce case/action idempotency and retry-safe response | Engineering | Roll back on financial duplication |
| R5 | SLA promise is missed | Owner update exceeds next-update time | Escalation queue, proactive apology copy, and support fallback | Support Ops | Review daily; pause if missed-SLA rate rises |
| R6 | Timeline increases anxiety | Comprehension or trust falls in E1/E2 | Simplify copy; progressive detail; human escalation | Product/Research | Iterate before pilot |
| R7 | Support handle time rises | Agent workflow requires repeated lookup | Shared case read model and training | Support Ops | Hold scale until parity is restored |
| R8 | Instrumentation cannot link outcomes | Missing `case_id` or event mismatch | Contract validation and analytics reconciliation | Analytics | No pilot decision without trusted data |

## Kill criteria

Stop or roll back the customer-facing hub if any of the following occurs:

- a customer receives a duplicate refund or replacement;
- the experience displays a false final outcome;
- event conflicts make the current state materially misleading;
- support cannot access the same case state;
- privacy, security, or accessibility review finds a release-blocking issue;
- pilot guardrails breach the agreed threshold for two consecutive review periods.

## Review sign-off

The release is not ready for scale until Product, Engineering, Operations, Support, Delivery, Payments, Analytics, and UX Research record approval against the checklist and the rollback drill is complete.
