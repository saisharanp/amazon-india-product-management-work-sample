# Stage 2 — Problem Statements

**Product:** Amazon India  
**Evidence base:** Stage 1 public-feedback sample of 22 records  
**Status:** Awaiting approval

## Problem framing

Amazon India’s public product promise emphasizes convenience, selection, payments, delivery tracking, easy returns, and customer support. The Stage 1 evidence suggests that the largest trust failures occur when an order enters an exception state and the customer cannot reconcile the system status with reality.

The discovery problem is framed around **exception clarity and recovery**, but the product decision intentionally narrows the first MVP to one exception type: delivered but not received.

## Candidate problem statements

### P1 — Delivered but not received

For Amazon India customers whose package is marked delivered but not received, the experience does not consistently explain what happened, what evidence exists, who owns the investigation, or what will happen next. Customers repeat contacts, wait without a reliable deadline, or escalate publicly.

### P2 — Unowned support case

For customers contacting Amazon India about a delivered-but-not-received case, support interactions can feel fragmented because the customer cannot see one accountable owner, one case timeline, or a consistent next action across channels.

### P3 — Opaque refund or return outcome

For customers who become eligible for a refund or replacement after a delivered-but-not-received investigation, Amazon India does not always make the eligibility, settlement stage, or expected completion date easy to understand.

### P4 — Low-confidence delivery handoff

For customers whose order is recorded as delivered, the app may not give enough confidence that the handoff reached the intended recipient or location, making non-receipt disputes difficult to resolve.

### P5 — Fragile discovery controls

For intent-driven shoppers, inconsistent sorting or filtering can make it difficult to narrow Amazon’s catalog and trust that the selected criteria are being applied.

## Root-cause hypotheses

- Delivery, seller, support, and payment systems may expose different states to customers and agents.
- Exception policies may be optimized for internal processing rather than customer comprehension.
- A “refund issued” event may be shown before bank settlement is complete.
- Support agents may not share one structured case record across delivery and payments.
- Discovery controls may change or fail silently across app versions and catalog types.

These are hypotheses requiring internal data and user research.

## Recommended problem to solve

> **For Amazon India customers whose order is marked delivered but not received, the current experience makes it difficult to understand what happened, reach an accountable owner, and predict the next resolution step. This creates repeated effort, financial anxiety, and avoidable loss of trust.**

## Why this problem

- It is supported by multiple source types, not one isolated review.
- It affects high-severity moments involving delivery, money, and trust.
- It connects several repeated themes: delivery reliability, support consistency, and refund clarity.
- It can be measured through operational and product outcomes.
- It creates a bounded opportunity for product, operations, support, delivery, and payments teams to solve together.

## Non-goals

- Redesign all delivery operations.
- Guarantee that every delivery succeeds.
- Replace human support in every case.
- Solve marketplace seller quality or product authenticity in this stage.
- Build a complete competitor benchmark.

## Stage 2 decision

Recommend P1 as the primary product problem. Treat P2 as a required enabler, P3 as an adjacent follow-on, and P5 as out of scope for this case study.
