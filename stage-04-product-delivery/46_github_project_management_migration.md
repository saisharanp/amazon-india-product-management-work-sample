# GitHub Product-Management Execution Index

**System of record:** GitHub Issues in the private repository
**Repository:** https://github.com/saisharanp/amazon-india-product-management-work-sample
**Purpose:** Convert the Stage 4 backlog, validation approvals, and launch-readiness work into one actionable issue queue with labels and acceptance summaries.

## Migration decision

No Linear, Jira, Asana, or Monday connector was available in this session. GitHub Issues was selected because the product-management work sample already lives in this private GitHub repository, preserving traceability between requirements, documentation, design, and execution.

## Issue map

| Requirement | GitHub issue | Labels |
|---|---|---|
| UR-01 Surface exception banner | [Issue #3](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/3) | stage-04-product-delivery, mvp, must |
| UR-02 Create one case | [Issue #1](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/1) | stage-04-product-delivery, mvp, must |
| UR-03 Normalized timeline | [Issue #9](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/9) | stage-04-product-delivery, mvp, must |
| UR-04 Owner and next update | [Issue #7](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/7) | stage-04-product-delivery, mvp, must |
| UR-05 Recovery options | [Issue #5](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/5) | stage-04-product-delivery, mvp, must |
| UR-06 Duplicate recovery protection | [Issue #6](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/6) | stage-04-product-delivery, mvp, must |
| UR-07 Confirmed resolution | [Issue #10](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/10) | stage-04-product-delivery, mvp, must |
| UR-08 Human support routing | [Issue #11](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/11) | stage-04-product-delivery, mvp, must |
| UR-09 Notification consistency | [Issue #2](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/2) | stage-04-product-delivery, mvp |
| UR-10 Accessibility/localization | [Issue #12](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/12) | stage-04-product-delivery, mvp, must |
| UR-11 Measurement events | [Issue #8](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/8) | stage-04-product-delivery, mvp, must |
| UR-12 Audit and parity | [Issue #4](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/4) | stage-04-product-delivery, mvp, must |

## Stage 5 approval issues

- [FIGMA-01 — Review editable Figma wireframes](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/13)
- [V01 — Approve validation protocol](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/16)
- [V02 — Approve measurement contract](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/15)
- [V03 — Approve controlled pilot readiness](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/14)
- [V04 — Keep scale gate blocked](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/17)

## Stage 6 launch and scale issues

| Issue | Workstream | Exit evidence | Status |
|---|---|---|---|
| [S01 — Complete launch readiness checklist](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/18) | Launch readiness | Signed checklist, policy/source-of-truth review, rollback drill | Open |
| [S02 — Instrument real pilot metrics and alerts](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/19) | Real pilot instrumentation | Confirmed-resolution-within-SLA primary metric, dashboard, event QA, cohort and baseline definitions | Open |
| [S03 — Run daily pilot review and incident cadence](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/20) | Operating review | Daily review log, incident record, support reconciliation | Open |
| [S04 — Produce Day-7 and Day-30 evidence readout](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/21) | Post-launch readout | Day 1, Day 7, and Day 30 evidence package | Open |
| [S05 — Keep broad scale blocked until real evidence passes](https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/22) | Scale decision | Approved decision record; scale stays blocked until criteria pass | Open |

## Operating usage

- The Stage 4 workbook remains the editable prioritization model and source for the issue titles.
- GitHub Issues is the execution queue for status, assignee, labels, discussion, and acceptance tracking.
- Figma is the design-review source for customer-facing screen decisions.
- Stage 5 approval issues must be closed or explicitly revised before the next stage begins.
- Stage 6 issues remain open until real evidence supports the next operating or scale decision.
