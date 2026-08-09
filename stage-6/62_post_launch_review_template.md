# Stage 6 — Post-Launch Review Template

Use this template for the controlled pilot and any extended exposure. Replace placeholders with real evidence; preserve the original baseline and cohort definitions.

## Header

| Field | Entry |
|---|---|
| Review date | `[YYYY-MM-DD]` |
| Review window | `[start]` to `[end]` |
| Exposure phase | `Internal alpha / Shadow / Controlled pilot / Extended pilot` |
| Cohort and exclusions | `[link to approved definition]` |
| Baseline window | `[link and dates]` |
| Feature flag state | `[off / limited / on for approved cohort]` |
| Incident status | `[none / open P0/P1/P2]` |

## Day 1 review

- Exposure and event counts reconcile: `[yes/no]`
- Case-linkage completeness: `[actual]` versus `≥95%`
- Source conflicts: `[actual]` versus `≤5%`
- Customer-facing accuracy sample: `[n]` cases, `[n]` correct
- Support queue impact: `[actual]` versus baseline
- Decision: `Continue / Pause / Rollback`
- Owner and next review: `[name, date]`

## Day 7 review

- Primary outcome changes: `[actuals versus baseline/control]`
- Understood-next rate: `[actual]`
- Recovery completion: `[actual]`
- Incorrect recovery / false final / duplicate financial action: `[counts]`
- SLA breach and reopen rate: `[actuals]`
- Open defects and incidents: `[links]`
- Decision: `Extend / Iterate / Rollback / Stay blocked`

## Day 30 scale review

- Evidence completeness: `[complete/incomplete]`
- Primary metrics pass: `[yes/no]`
- Guardrails pass: `[yes/no]`
- Support capacity and handle time pass: `[yes/no]`
- Segment stability: `[summary]`
- Customer research or sampled-case learning: `[summary]`
- Recommendation: `Scale / Iterate / Rollback / Stay blocked`

## Learning log

| Observation | Evidence | Interpretation | Product response | Owner | Due date |
|---|---|---|---|---|---|
| `[observation]` | `[metric/case/incident link]` | `[what it means]` | `[change or follow-up]` | `[owner]` | `[date]` |

## Approval record

| Function | Reviewer | Decision | Date | Notes |
|---|---|---|---|---|
| Product | `[name]` | `[approve/revise/block]` | `[date]` | `[notes]` |
| Engineering | `[name]` | `[approve/revise/block]` | `[date]` | `[notes]` |
| Operations / Support | `[name]` | `[approve/revise/block]` | `[date]` | `[notes]` |
| Payments / Policy | `[name]` | `[approve/revise/block]` | `[date]` | `[notes]` |
| Analytics | `[name]` | `[approve/revise/block]` | `[date]` | `[notes]` |
| Privacy / Security | `[name]` | `[approve/revise/block]` | `[date]` | `[notes]` |
