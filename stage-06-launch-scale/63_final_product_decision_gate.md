# Stage 6 — Final Product Decision Gate

**Product:** Amazon India
**Feature:** Unified exception resolution — delivered but not received
**Status:** Scale blocked pending real pilot evidence

## Decision options

| Decision | Meaning | Required action |
|---|---|---|
| Go to controlled pilot | Readiness is complete and the approved pilot may begin | Enable only the approved cohort and start daily review |
| Iterate | Safe to continue learning, but outcome, comprehension, or operational target is not met | Pause expansion, fix the named issue, and define the next test |
| Rollback | A safety, truthfulness, privacy, financial, or severe operational guardrail failed | Disable new exposure and reconcile affected cases |
| Scale | Real pilot and extended-pilot evidence pass all primary and guardrail requirements | Obtain cross-functional approval and expand in measured increments |
| Stay blocked | Evidence, approval, or data quality is incomplete | Do not expand; complete the missing evidence |

## Scale criteria

Scale is eligible only when all are true:

1. The baseline/control and cohort definition are documented.
2. Confirmed resolution within the promised SLA improves against the approved baseline or holdout; repeat contacts and comprehension do not regress.
3. Incorrect recovery, false final outcome, and duplicate financial action are zero.
4. Event conflict, SLA breach, handle time, reopen rate, and linkage completeness are within approved limits.
5. A sampled-case review confirms customer-facing truth and actionable next steps, including correct human routing for high-risk or ambiguous cases.
6. Support, Payments, Delivery, Analytics, Engineering, Product, and Privacy/Security approvals are recorded where applicable.
7. No unresolved P0/P1 incident affects interpretation.

## Current recommendation

**Stay blocked for broad scale.** Stage 5 supplies a synthetic worksample and a pilot mechanism, not live evidence. The next authorized action is to complete the readiness checklist and instrument a real controlled pilot after the required approvals.

## Decision record

| Field | Entry |
|---|---|
| Decision | `Stay blocked / Go / Iterate / Rollback / Scale` |
| Decision date | `[YYYY-MM-DD]` |
| Evidence package | `[scorecard, dashboard, sample review, incident log]` |
| Cohort | `[definition and size]` |
| Decision owner | `[name]` |
| Approvers | `[names and functions]` |
| Next review | `[date]` |
| Conditions to change decision | `[explicit measurable conditions]` |

## Handoff

- Figma wireframes: https://www.figma.com/design/BL3cvaVa3Yzxwv8Nsu37Wu
- GitHub issue queue: https://github.com/saisharanp/amazon-india-product-management-work-sample/issues
- Stage 6 scorecard: `64_launch_scorecard.xlsx`
