# Stage 3 — Solution Risks and Assumptions

**Solution:** Exception timeline and recovery hub  
**Status:** Awaiting approval

## Assumptions

| ID | Assumption | Type | Confidence | Validation |
|---|---|---|---|---|
| A1 | Customers prefer one clear next action over more raw tracking detail | Desirability | Medium | Prototype test |
| A2 | A shared timeline reduces repeated support contacts | Value | Medium | Historical case analysis and pilot |
| A3 | Amazon can reconcile delivery, support, refund, and replacement events | Feasibility | Low/Medium | Technical discovery |
| A4 | Support agents can act on the same state customers see | Operational | Medium | Agent walkthrough |
| A5 | Customers will choose a self-service recovery path when eligibility is clear | Desirability | Medium | Concept test |
| A6 | Refund settlement dates can be shown accurately enough to build trust | Feasibility | Low/Medium | Payments data audit |
| A7 | High-severity cases can be detected consistently | Operational | Medium | Incident taxonomy review |
| A8 | One exception type is narrow enough for an MVP | Scope | High | Product review |

## Risks and mitigations

| Risk | Impact | Likelihood | Mitigation | Owner |
|---|---|---:|---|---|
| Conflicting event sources produce a misleading timeline | Trust damage | High | Show confidence states; define authoritative event per state | Product + Engineering |
| Customers interpret investigation as an admission of failure | Brand impact | Medium | Use plain language and action-focused copy | Product + Content |
| Self-service recovery denies a legitimate claim | Financial and trust harm | Medium | Add human escalation and audit trail | Operations |
| Refund status is shown as complete before settlement | Financial anxiety | Medium | Separate initiated, processing, and settled states | Payments |
| More verification steps slow delivery | Convenience loss | Medium | Use risk-based verification only for disputed/high-value cases | Logistics |
| Case ownership increases support workload | Cost increase | Medium | Pilot with high-severity cases; measure handling time | Support |
| MVP expands into a platform rewrite | Delivery delay | High | Limit to one exception type and one customer flow | Product |
| Notifications become noisy | Customer annoyance | Low/Medium | Notify only on meaningful state changes | CRM |
| Accessibility is weak under stress | Exclusion and errors | Medium | Test screen readers, contrast, text labels, and plain language | Design |

## Kill criteria

Pause or redesign if:

- timeline accuracy is below an agreed threshold;
- recovery recommendations create more incorrect outcomes than the current flow;
- repeat contacts do not improve after sufficient exposure;
- customers prefer direct human support for the selected exception;
- the required integrations cannot be delivered without expanding MVP scope.

## Approval questions

1. Which risk should be tested first: event accuracy, recovery eligibility, or customer comprehension?
2. Which internal team owns the pilot?
3. What error rate is acceptable before the timeline should be hidden or downgraded to a generic support flow?
