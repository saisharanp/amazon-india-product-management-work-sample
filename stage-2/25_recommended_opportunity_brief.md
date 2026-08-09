# Stage 2 — Recommended Opportunity Brief

**Product:** Amazon India  
**Recommended opportunity:** Delivered-but-not-received resolution layer
**Status:** Awaiting approval

## Recommendation

Prioritize a narrow resolution layer for delivered-but-not-received cases that helps customers:

1. Understand what happened.
2. Know who owns the case.
3. Choose a recovery path.
4. See a policy-validated recovery outcome without independently executing a financial action.

The first MVP should focus on one exception type to limit integration risk. The recommended starting point is **delivered but not received**, because it combines the strongest delivery, support, trust, and escalation signals.

## Evidence

- Multiple public records describe incorrect delivery status or missing handoff.
- Several records describe repeated support contacts or inconsistent answers.
- Refund and return records show financial and fairness anxiety.
- Amazon’s official app description creates a clear promise around tracking, returns, refunds, and support, making promise-to-experience gaps measurable.

## Target segment

Discovery segment: trust-sensitive exception resolvers, including frequent, Prime, remote-area, high-value, and time-sensitive buyers.

Initial pilot segment: eligible delivered-but-not-received cases with reliable event linkage in one approved delivery region or fulfilment context, balanced for Prime/non-Prime representation. Exclude fraud investigations, unresolved identity/payment risk, high-value cases above the approved policy threshold, and policy-ambiguous cases from automated recovery.

## Expected value

### Customer value

- Less uncertainty and repeated effort.
- Faster access to the correct resolution path.
- More confidence in refund/replacement outcomes.

### Business value

- Lower repeat-contact volume.
- Lower escalation and support handling cost.
- Better recovery satisfaction.
- A testable hypothesis about trust and membership churn risk; no quantified impact is claimed without internal data.

### Strategic value

Protects Amazon’s core convenience proposition by making failure recovery feel dependable.

## MVP hypothesis

> If Amazon shows one accurate exception timeline, one accountable owner, and one clear next action for eligible “delivered but not received” cases, then the share of cases reaching confirmed resolution within the promised SLA will improve without increasing unsafe recovery or support burden.

## Success metrics

### Primary

- Confirmed resolution within promised SLA

### Secondary customer and operational outcomes

- Repeat contacts per exception case
- Time to confirmed resolution
- Recovery completion rate
- Post-resolution CSAT
- “I understood what would happen next” agreement
- Trust recovery / likelihood to purchase again

### Guardrails

- False-positive delivery disputes
- Unresolved cases beyond SLA
- Refund or replacement errors
- Support handle time

## Dependencies

- Delivery event and handoff data
- Customer support case state
- Refund/replacement eligibility and policy
- Customer notification system
- Analytics event instrumentation
- Agent workflow alignment

## Key risks

- Data sources disagree about status.
- A unified timeline exposes internal inconsistency.
- Customers may prefer human contact for high-value incidents; those cases are excluded from automated recovery in the first pilot.
- More evidence or verification could add delivery friction.

## Options considered

| Option | Decision |
|---|---|
| Unified exception resolution | Recommended |
| Refund transparency only | Backup / vertical slice |
| Delivery confidence only | Backup for last-mile-focused scope |
| Support case ownership only | Required enabler, not complete customer solution |

## Approval required

1. Approve delivered-but-not-received resolution as the primary MVP opportunity.
2. Approve the initial pilot cohort exclusions and the no-independent-financial-action rule.
3. Approve proceeding to Stage 3 solution concepts and prototype discovery.

**Status: Awaiting approval.**
