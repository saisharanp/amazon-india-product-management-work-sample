# Stage 2 — Recommended Opportunity Brief

**Product:** Amazon India  
**Recommended opportunity:** Unified post-purchase exception resolution  
**Status:** Awaiting approval

## Recommendation

Prioritize a unified post-purchase exception experience that helps customers:

1. Understand what happened.
2. Know who owns the case.
3. Choose a recovery path.
4. See the expected refund, replacement, or delivery outcome.

The first MVP should focus on one exception type to limit integration risk. The recommended starting point is **delivered but not received**, because it combines the strongest delivery, support, trust, and escalation signals.

## Evidence

- Multiple public records describe incorrect delivery status or missing handoff.
- Several records describe repeated support contacts or inconsistent answers.
- Refund and return records show financial and fairness anxiety.
- Amazon’s official app description creates a clear promise around tracking, returns, refunds, and support, making promise-to-experience gaps measurable.

## Target segment

Primary: trust-sensitive exception resolvers, especially frequent, high-value, Prime, remote-area, and time-sensitive buyers.  
Secondary: convenience-led repeat buyers whose retention depends on reliable recovery.

## Expected value

### Customer value

- Less uncertainty and repeated effort.
- Faster access to the correct resolution path.
- More confidence in refund/replacement outcomes.

### Business value

- Lower repeat-contact volume.
- Lower escalation and support handling cost.
- Better recovery satisfaction.
- Reduced trust and membership churn risk.

### Strategic value

Protects Amazon’s core convenience proposition by making failure recovery feel dependable.

## MVP hypothesis

> If Amazon shows one accurate exception timeline, one accountable owner, and one clear next action for “delivered but not received” cases, then repeat contacts will decrease and post-resolution trust will improve.

## Success metrics

### Primary

- Repeat contacts per exception case
- Time to confirmed resolution
- Recovery completion rate

### Customer

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
- Customers may prefer human contact for high-value incidents.
- More evidence or verification could add delivery friction.

## Options considered

| Option | Decision |
|---|---|
| Unified exception resolution | Recommended |
| Refund transparency only | Backup / vertical slice |
| Delivery confidence only | Backup for last-mile-focused scope |
| Support case ownership only | Required enabler, not complete customer solution |

## Approval required

1. Approve the unified post-purchase exception experience as the opportunity.
2. Approve “delivered but not received” as the first MVP exception type, or choose refund-pending instead.
3. Approve proceeding to Stage 3 solution concepts and prototype discovery.

**Status: Awaiting approval.**
