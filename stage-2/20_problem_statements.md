# Stage 2 — Problem Statements

**Product:** Amazon India  
**Evidence base:** Stage 1 public-feedback sample of 22 records  
**Status:** Awaiting approval

## Problem framing

Amazon India’s public product promise emphasizes convenience, selection, payments, delivery tracking, easy returns, and customer support. The Stage 1 evidence suggests that the largest trust failures occur when an order enters an exception state and the customer cannot reconcile the system status with reality.

The problem is therefore framed around **exception clarity and recovery**, not around one isolated delivery or refund defect.

## Candidate problem statements

### P1 — Unclear delivery exception

For Amazon India customers whose package is delayed, missing, incorrectly marked delivered, or cancelled, the experience does not consistently explain what happened, what evidence exists, or what will happen next. Customers repeat contacts, wait without a reliable deadline, or escalate publicly.

### P2 — Unowned support case

For customers contacting Amazon India about a delivery, return, or refund exception, support interactions can feel fragmented because the customer cannot see one accountable owner, one case timeline, or a consistent next action across channels.

### P3 — Opaque refund or return outcome

For customers expecting a refund or replacement after a failed order, Amazon India does not always make the eligibility, amount, deductions, settlement stage, or expected completion date easy to understand.

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

> **For Amazon India customers whose order enters a delivery, return, or refund exception, the current experience makes it difficult to understand what happened, reach an accountable owner, and predict the next resolution step. This creates repeated effort, financial anxiety, and avoidable loss of trust.**

## Why this problem

- It is supported by multiple source types, not one isolated review.
- It affects high-severity moments involving delivery, money, and trust.
- It connects several repeated themes: delivery reliability, support consistency, and refund clarity.
- It can be measured through operational and product outcomes.
- It creates a coherent opportunity for product, operations, support, and payments teams to solve together.

## Non-goals

- Redesign all delivery operations.
- Guarantee that every delivery succeeds.
- Replace human support in every case.
- Solve marketplace seller quality or product authenticity in this stage.
- Build a complete competitor benchmark.

## Stage 2 decision

Recommend prioritizing P1 + P2 as the primary opportunity area, with P3 as a tightly related backup or MVP slice.
