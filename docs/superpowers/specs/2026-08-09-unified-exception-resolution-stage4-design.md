# Unified Exception Resolution — Stage 4 Product Design

**Product:** Amazon India
**Stage:** Delivery planning
**Decision status:** Approved to proceed from Stage 3

## Goal

Convert the approved “Exception Timeline and Recovery Hub” concept into a delivery-ready MVP for Amazon India’s **delivered but not received** exception journey.

## Product boundary

The MVP starts when a delivery is marked delivered but the customer reports non-receipt. It ends when the customer receives a confirmed delivery, replacement, or refund outcome. The experience must show one customer-readable state, one case owner or queue, one next-update time, and one eligible recovery action.

Refund-pending, damaged-item, seller-cancellation, and proactive exception detection are explicitly later slices. They can reuse the same state model and case contract after the first MVP is stable.

## Design decisions

1. **Customer surface:** extend the existing order-detail page with an exception banner and linked case timeline.
2. **Canonical case:** create one exception case ID that joins order, delivery, support, payment, and recovery records.
3. **Customer state:** expose normalized states rather than raw operational events.
4. **Recovery:** show only policy-eligible options and the expected customer-facing outcome for each option.
5. **Promise discipline:** display a next-update time only when the owning workflow provides a measurable SLA.
6. **Human fallback:** route high-value, deadline-sensitive, or policy-ambiguous cases to support instead of forcing automation.
7. **Measurement:** treat repeat contacts per case, confirmed-resolution time, recovery completion, comprehension, and guardrails as the release decision system.

## Delivery units

| Unit | Responsibility | Review artifact |
|---|---|---|
| Customer experience | Banner, timeline, recovery choice, resolution status | PRD and wireframes |
| Case orchestration | Case creation, state transitions, owner, SLA | Technical/data contract |
| Recovery policy | Eligibility, refund/replacement/delivery options | Requirements and acceptance criteria |
| Support operations | Queue ownership, escalation, missed-SLA handling | Service blueprint and rollout plan |
| Analytics | Event taxonomy, experiment cohorts, guardrails | Measurement plan and prioritization workbook |

## Decision gates

Before build: approve MVP scope, canonical state model, data authority rules, and E1–E4 validation outputs.

Before pilot: pass event accuracy, policy safety, accessibility, support readiness, instrumentation, and rollback checks.

Before scale: show a favorable signal on repeat contact or comprehension without guardrail breaches.

## Success definition

The MVP is ready to scale when customers can correctly explain what happened and what happens next, select an eligible recovery path without support intervention, and receive an outcome that matches the displayed promise.
