# Stage 5 — Validation Readout

**Product:** Amazon India
**Feature:** Unified exception resolution — delivered but not received
**Evidence status:** Synthetic worksample demonstration; not Amazon internal or live pilot data

## Executive summary

The proposed scorecard structure shows how to compare the current experience with a delivered-but-not-received resolution layer. In the synthetic six-case comparison, the proposed arm improves repeat-contact and resolution-time examples while keeping incorrect recovery at zero and reducing SLA breaches. This is sufficient to demonstrate a **go/no-go decision method**, not to claim product impact.

Recommendation: proceed to a controlled pilot only after real baseline instrumentation, policy validation, support readiness, and rollback testing are complete. Do not scale from this synthetic readout.

## Synthetic comparison

| Metric | Baseline example | Proposed example | Direction | Interpretation |
|---|---:|---:|---|---|
| Confirmed resolution within SLA | Not observed | Not observed | Pending | Primary outcome requires real baseline and pilot data |
| Repeat contacts per case | 2.50 | 0.83 | Better | Fewer repeated explanations in the proposed flow |
| Confirmed-resolution time, hours | 47.83 | 26.67 | Better | Faster example closure |
| “Understood next” rate | 0% | 100% | Better | Synthetic proxy for comprehension |
| Incorrect recovery rate | 0% | 0% | Guardrail holds | No incorrect recovery in sample |
| SLA breach rate | 66.7% | 16.7% | Better | One proposed-arm breach remains |
| Support contacts per case | 2.50 | 0.83 | Better | Directional support-effort example |

## What the replay demonstrates

- Raw case rows can be linked to an arm and a case ID.
- Primary metrics and guardrails can be calculated with auditable formulas.
- Event conflict can be present without automatically forcing an unsafe recovery.
- A proposed flow can route an ambiguous case to support rather than selecting a financial outcome.
- A release recommendation can require both primary improvement and guardrail safety.

## What the replay does not demonstrate

- It does not estimate Amazon’s actual exception volume, conversion, cost, or customer impact.
- It does not validate event accuracy, policy eligibility, or technical latency in production.
- It does not establish statistical significance.
- It does not replace E1–E5 research or a controlled pilot.

## Required real-pilot evidence

1. A trusted baseline with case-linked repeat contacts and resolution timestamps.
2. A pre-registered cohort and comparison approach.
3. Real event-conflict, incorrect-recovery, missed-SLA, and support-handle-time monitoring.
4. UX Research sign-off on comprehension and recovery choice.
5. Operations sign-off on owner/SLA capacity and escalation.
6. Engineering sign-off on idempotency, audit, and rollback.

## Decision

**Synthetic decision:** the workbook formulas pass illustrative thresholds and recommend controlled-pilot preparation. Because the target and inputs are synthetic, this is a mechanics demonstration only; it does not authorize customer exposure or scale.
**Portfolio decision:** keep scale blocked until real pilot evidence is collected and approved.
