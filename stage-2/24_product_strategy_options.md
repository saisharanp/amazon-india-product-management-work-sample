# Stage 2 — Product Strategy Options

**Product:** Amazon India  
**Status:** Awaiting approval

## Option A — Unified exception resolution experience

Create one post-purchase experience that connects delivery events, support ownership, recovery choice, and refund/replacement status.

**Strengths**

- Addresses the strongest combined evidence signal.
- Creates a shared product/service outcome.
- Can reduce both customer effort and support cost.
- Enables measurable improvements across multiple journey points.

**Risks**

- Requires cross-team and cross-system integration.
- May expose inconsistencies between internal event sources.
- Needs careful scope control to avoid becoming a platform rewrite.

**Recommendation:** Primary option.

## Option B — Refund transparency first

Improve refund amount, deductions, settlement stage, and expected date before expanding into delivery and support.

**Strengths**

- Clear MVP boundary.
- High customer and financial trust value.
- Easier to test with a focused prototype.

**Risks**

- Does not solve the original delivery-status or ownership problem.
- May reduce anxiety without reducing repeat contacts.
- Depends on payment and policy data quality.

**Recommendation:** Backup option or first vertical slice of Option A.

## Option C — Delivery confidence and handoff verification

Improve delivery-status vocabulary, handoff evidence, OTP/recipient confirmation, and non-receipt reporting.

**Strengths**

- Addresses critical “delivered but not received” failures.
- Potentially prevents avoidable disputes.
- Strong operational and trust relevance.

**Risks**

- May require courier and last-mile changes beyond the app.
- Evidence collection can create delivery friction.
- Does not fully solve refund or support inconsistency.

**Recommendation:** Backup option for a delivery-focused scope.

## Option D — Support case ownership and escalation

Create a structured case record, owner, SLA, escalation rule, and shared resolution state for delivery/return/refund issues.

**Strengths**

- Directly addresses repeated-contact and conflicting-answer signals.
- Potential to reduce support cost.
- Strong fit with service blueprinting.

**Risks**

- Can become an internal operations project with weak customer visibility.
- Requires agent tooling and policy alignment.
- Benefits may be hard to attribute without operational data.

**Recommendation:** Enabler for Option A.

## Strategy recommendation

Select Option A as the strategic direction, but define the first MVP around **one high-severity exception type**—for example, “delivered but not received” or “refund pending after cancellation.” Use Option B or D as the initial vertical slice depending on technical feasibility.

## Decision required

Approve Option A as the strategic direction and select the first exception type for Stage 3 solution discovery.
