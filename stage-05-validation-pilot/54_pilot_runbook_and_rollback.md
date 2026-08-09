# Stage 5 — Pilot Runbook and Rollback

**Product:** Amazon India
**Feature:** Unified exception resolution — delivered but not received

## 1. Pilot operating model

### Before exposure

- Confirm cohort rules, exclusions, baseline window, feature flag, and support queue.
- Confirm the approved cohort is limited to delivered-but-not-received reports with reliable event linkage in one region or fulfilment context; high-risk and policy-ambiguous cases route to human review.
- Validate event linkage, recovery eligibility, owner/SLA, analytics, alerting, and rollback in a non-customer environment.
- Train support on the shared `case_id`, normalized states, customer copy, and escalation script.
- Publish the daily review sheet with volume, conflict, recovery, SLA, and support metrics.

### During daily review

1. Reconcile cases created, cases exposed, and cases with linked analytics events.
2. Review event conflicts, stale reads, duplicate actions, and policy fallbacks.
3. Compare confirmed resolution within SLA, repeat contacts, and resolution time with the baseline/control.
4. Sample resolved cases for customer-facing accuracy.
5. Record incidents, owner, mitigation, and decision in the approval log.

### Pilot exit

Exit to an extended pilot only when confirmed resolution within SLA improves, secondary metrics do not regress, no critical guardrail breaches occur, support capacity is stable, and the full readiness checklist is signed. Exit to iteration when comprehension or recovery choice fails. Exit to rollback when customer truth, financial safety, privacy, or high-risk routing is compromised.

## 2. Incident severity

| Severity | Example | Action |
|---|---|---|
| P0 | Duplicate refund/replacement, false final outcome, privacy exposure | Disable feature flag immediately; preserve cases; incident lead and reconciliation |
| P1 | Material event conflict, high incorrect recovery, widespread missed SLA | Pause new exposure; route to support; correct authority or policy mapping |
| P2 | Copy confusion, isolated stale update, non-critical analytics gap | Keep monitored if safe; assign fix and review next day |

## 3. Rollback procedure

1. Product or incident lead declares rollback and records reason.
2. Engineering disables the customer-facing feature flag for new exposures.
3. Existing cases remain in the canonical case workflow and support can resolve them.
4. Customer surfaces fall back to the safe order/support experience; no automated refund or replacement is reversed.
5. Payments, Delivery, and Support reconcile in-progress outcomes from authoritative systems.
6. Analytics marks the rollback timestamp and separates exposed, treated, and fallback cases.
7. Product, Engineering, Operations, and Support approve re-enable criteria after root-cause review.

## 4. Re-enable criteria

- Root cause is identified and tested.
- Affected cases are reconciled.
- P0/P1 guardrail is back within threshold.
- Support has updated instructions.
- Monitoring and alerting are verified.
- Rollback drill is repeated successfully.
