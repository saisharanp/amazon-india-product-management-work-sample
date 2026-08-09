# Unified Exception Resolution — Stage 5 Validation Design

**Product:** Amazon India
**Stage:** Validation and pilot decisioning
**Decision status:** Approved to proceed from Stage 4

## Goal

Show how the delivered-but-not-received MVP would be validated, measured, operated, and approved for a controlled pilot.

## Evidence boundary

This stage creates a field-ready protocol and a clearly labeled synthetic case replay. The replay is a worksample for demonstrating formulas, cohort comparison, guardrails, and decision rules. It is not Amazon internal data, a live experiment, or evidence that the Amazon product currently behaves this way.

## Design choices

1. Use Stage 3 E1–E4 research questions and Stage 4 release gates as the measurement backbone.
2. Use a small case-level replay to make the analysis auditable from raw rows to scorecard outputs.
3. Compare a baseline arm with a proposed-experience arm on repeat contacts, resolution time, comprehension, SLA breach, and incorrect recovery.
4. Treat guardrails as release blockers even if primary metrics improve.
5. Recommend only a controlled pilot from synthetic evidence; never recommend scale from fabricated or simulated data.

## Deliverables

| Deliverable | Purpose |
|---|---|
| Validation protocol | Defines research questions, participants, tasks, analysis, and pass/fail thresholds |
| Synthetic case replay CSV | Provides auditable example rows for the scorecard |
| Pilot scorecard workbook | Calculates cohort metrics and captures decisions |
| Validation readout | Demonstrates how findings and recommendation should be written |
| Pilot runbook and rollback | Defines daily operations, incident response, and safe disablement |
| Stage 5 approval gate | Captures approval before controlled pilot and later scale |

## Decision gates

- **Validation gate:** comprehension and recovery-choice tests pass without critical policy or accessibility issues.
- **Pilot gate:** synthetic scorecard demonstrates the calculation path; real pilot requires a trusted baseline, event-linked case IDs, support readiness, and rollback drill.
- **Scale gate:** requires real pilot evidence, not the synthetic replay, and must pass all guardrails.
