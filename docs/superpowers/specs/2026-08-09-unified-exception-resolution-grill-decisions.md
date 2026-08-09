# Agreed Product Decisions from Case-Study Grill

**Date:** 2026-08-09
**Product:** Amazon India
**Feature:** Delivered but not received exception resolution
**Purpose:** Record the decisions applied across the case study after structured stress-testing.

## Positioning

This is a senior Product Manager portfolio worksample, not a claim of a live Amazon launch, internal Amazon performance, market prevalence, or quantified ROI.

## Scope decision

- **MVP in scope:** a customer-reported delivered-but-not-received case from the order-detail page.
- **MVP experience:** truthful state, one `case_id`, accountable owner/queue, next-update promise, safe support escalation, and policy-validated recovery choices.
- **Adjacent, not MVP:** delayed delivery, damaged/wrong item, refund-pending, return disputes, cancellation, proactive exception prediction, and discovery controls.

## Evidence decision

The 22 public records demonstrate recurring directional pain and justify discovery. They do not establish incidence, market size, causal impact, revenue effect, or Amazon-wide severity. Internal delivery, support, payment, policy, and retention data are required before investment sizing.

## Pilot decision

Start with a small cohort of eligible delivered-but-not-received cases with reliable event linkage, balanced Prime/non-Prime representation, and one selected delivery region or fulfilment context. Exclude fraud investigations, unresolved identity/payment risk, high-value cases above the approved policy threshold, and policy-ambiguous cases from automated recovery.

## Measurement decision

- **Primary outcome:** percentage of eligible cases reaching confirmed resolution within the promised SLA.
- **Secondary outcomes:** repeat contacts per case, confirmed-resolution time, recovery completion, and customer comprehension/trust.
- **Guardrails:** incorrect recovery, false final outcome, duplicate financial action, source conflict, SLA breach, support handle time, and case-linkage completeness.

## Architecture and safety decision

The product is a customer-facing resolution layer over existing authoritative systems. It does not rebuild delivery, payments, refunds, or support infrastructure. Each state has an authority map. Conflicts produce an honest investigation state and human escalation; the product does not invent eligibility or independently execute financial recovery.

## Stop/scale decision

Rollback immediately for duplicate financial actions, false final outcomes, privacy exposure, or unsafe recovery. Stay blocked when evidence is missing, synthetic, contradictory, or not approved. Scale only after real controlled-pilot evidence and cross-functional approval.
