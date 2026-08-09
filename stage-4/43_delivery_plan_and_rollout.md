# Stage 4 — Delivery Plan and Rollout

**Product:** Amazon India
**Feature:** Unified exception resolution — delivered but not received
**Status:** Ready for cross-functional sequencing

## 1. Workstreams

| Workstream | Deliverable | Accountable owner | Key dependency |
|---|---|---|---|
| Product and policy | MVP rules, copy, recovery eligibility, escalation thresholds | Product + Operations | Policy decision service |
| Case orchestration | Canonical case, state transitions, idempotent actions, audit | Engineering | Support workflow and event sources |
| Customer experience | Banner, timeline, recovery options, resolution status | Product Design + App/Web Eng | Read model and copy review |
| Support operations | Queue ownership, SLA, scripts, escalation, training | Support Operations | Case state and owner contract |
| Delivery and payments | Event authority, refund/settlement, replacement confirmation | Delivery + Payments | Orchestration contract |
| Analytics | Instrumentation, baseline, cohorting, guardrails dashboard | Analytics | Event taxonomy and case ID |
| Research and validation | E1–E4 usability, agent, historical, feasibility tests | UX Research | Wireframes and test data |

## 2. Sequence

### Gate A — Definition and validation

Confirm the PRD, data authorities, copy, policy rules, test scenarios, baseline metrics, and E1–E4 results. Exit when no unresolved P0 ambiguity remains.

### Gate B — Internal alpha

Use synthetic cases across current, stale, conflicting, ineligible, duplicate, and missed-SLA conditions. Validate customer and agent parity, audit, accessibility, and idempotency. Exit when P0 acceptance criteria pass.

### Gate C — Shadow mode

Generate the proposed state and recovery recommendation without exposing it to customers. Compare against existing outcomes and measure conflict, policy, and owner/SLA accuracy. Exit when event and eligibility guardrails pass for the agreed observation window.

### Gate D — Limited pilot

Expose the experience to a small, monitored cohort of delivered-but-not-received cases. Retain a comparable baseline or control. Provide a visible support fallback and daily incident review. Exit when primary metrics move in the expected direction without guardrail breach.

### Gate E — Scale decision

Expand by cohort only after Product, Operations, Engineering, Support, Payments, Delivery, and Analytics sign the release-readiness checklist. Keep rollback available until the post-scale observation period closes.

## 3. Pilot cohort design

- Start with one delivery region and a balanced mix of Prime/non-Prime customers.
- Exclude fraud investigations, high-value orders above the agreed policy threshold, and cases with unresolved identity or payment risk from automated recovery.
- Hold out a comparable baseline or control to compare repeat contacts, resolution time, and recovery completion.
- Review daily: event conflicts, false-positive rate, missed SLAs, duplicate actions, support transfer rate, and customer feedback.

## 4. RACI-style decision ownership

| Decision | Responsible | Accountable | Consulted | Informed |
|---|---|---|---|---|
| MVP scope and copy | Product, Design | Product | Operations, Support, Research | Engineering, Analytics |
| Policy eligibility | Operations, Policy | Operations | Payments, Inventory, Support | Product |
| State and event contract | Engineering | Engineering | Delivery, Payments, Support, Analytics | Product |
| Pilot readiness | Product, Engineering, Operations | Product | Support, Delivery, Payments, Analytics | Leadership |
| Scale/rollback | Product, Engineering, Operations | Product leadership | All workstream owners | Support and customer-facing teams |

## 5. Release gates

### Alpha entry

PRD approved; contract reviewed; synthetic test cases available; support owner and SLA defined; instrumentation mapped.

### Pilot entry

P0 acceptance criteria pass; event conflict rate is below the agreed threshold; recovery eligibility is policy-safe; accessibility review passes; rollback tested; support training complete.

### Scale entry

Repeat contacts per case or comprehension improves versus baseline; no critical incorrect recovery; no unresolved critical incident; missed-SLA recovery is operationally staffed; analytics and alerting are live.

## 6. Rollback

Disable the customer-facing exception hub with a feature flag while preserving the case record and support path. Existing cases remain visible in the fallback support workflow. Do not reverse an already initiated refund or replacement automatically; reconcile through the owning workflow and communicate the confirmed state.
