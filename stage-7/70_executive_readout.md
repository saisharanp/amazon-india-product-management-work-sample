# Final Executive Readout — Unified Exception Resolution

**Product:** Amazon India
**Scope:** Customer-reported delivered-but-not-received exception
**Portfolio status:** End-stage product-management worksample; broad scale intentionally blocked

## Executive decision

Proceed with a controlled pilot only after the Stage 5 approval items, Stage 6 readiness checklist, real baseline, event instrumentation, support preparation, and rollback drill are approved. Do not represent this package as a live Amazon launch or as measured Amazon performance.

## Customer problem

When an order is marked delivered but the customer has not received it, the customer must reconstruct what happened across tracking, notifications, and support. The resulting uncertainty is amplified when ownership, refund/replacement status, and the next update time are unclear.

## Product recommendation

Add a narrow delivered-but-not-received resolution layer to the existing order-detail experience:

- one customer-readable timeline;
- one `case_id` and accountable owner/queue;
- one next-update promise;
- policy-validated recovery choices or human escalation;
- clear refund, replacement, or delivery confirmation;
- shared state for customer, support, delivery, payments, and analytics;
- no independent automated financial execution in the first pilot.

## Why this opportunity

The directional public-feedback sample repeatedly surfaced delivery-status accuracy, support ownership, agent contactability, refund clarity, and return-policy consistency. The sample contains 22 coded public records and is explicitly directional, not statistically representative.

## Product-management evidence chain

**Public feedback → coded themes → personas/journey → opportunity tree and scoring → concept selection → Figma wireframes → PRD and backlog → validation protocol → pilot scorecard → launch/rollback gate.**

## Pilot boundary

Start with eligible cases that have reliable event linkage in one approved delivery region or fulfilment context, balanced for Prime/non-Prime representation. Exclude fraud investigations, unresolved identity/payment risk, high-value cases above the approved policy threshold, repeated-claim cases, and policy ambiguity from automated recovery.

## Decision criteria

Scale is eligible only after real pilot evidence shows improvement in confirmed resolution within the promised SLA, without regression in repeat contacts or comprehension and without incorrect recovery, false final outcomes, duplicate financial actions, unacceptable source conflicts, SLA breaches, or support-capacity harm.

## Current risks

- Delivery, payment, refund, and support systems may disagree.
- A unified timeline can expose unresolved internal ownership gaps.
- A recovery recommendation can be unsafe if policy or authoritative data is stale.
- Missing instrumentation can create a false sense of success.

## Next accountable actions

1. Complete the readiness checklist.
2. Instrument the real controlled pilot.
3. Run daily operating reviews and incident handling.
4. Produce Day 1, Day 7, and Day 30 readouts.
5. Record a final Go, Iterate, Rollback, Scale, or Stay blocked decision.

## Links

- Figma prototype: https://www.figma.com/design/BL3cvaVa3Yzxwv8Nsu37Wu
- GitHub repository: https://github.com/saisharanp/amazon-india-product-management-work-sample
- GitHub execution queue: https://github.com/saisharanp/amazon-india-product-management-work-sample/issues
- Final portfolio review issue: https://github.com/saisharanp/amazon-india-product-management-work-sample/issues/23
