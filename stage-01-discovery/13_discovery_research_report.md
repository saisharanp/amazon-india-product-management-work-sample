# Stage 1 — Amazon India Discovery Research Report

**Prepared:** 2026-08-09    
**Stage status:** Awaiting approval    
**Evidence sample:** 22 coded public records; directional, not statistically representative

## Executive summary

The strongest discovery signal is not a lack of Amazon capabilities. Amazon’s public product description emphasizes selection, payments, order tracking, returns, COD, Amazon Pay/UPI, and support. The recurring negative signal is that exception journeys do not reliably convert those capabilities into a trustworthy outcome.

Across the accessible sample, delivery-status accuracy, delivery-agent contactability, support ownership, refund clarity, and return-policy consistency repeatedly appear together. This creates a compounding trust problem: a customer cannot tell what happened, cannot reach a clear owner, and cannot predict when money or a replacement will arrive.

The highest-confidence discovery opportunity is therefore:

> **Make delivery exceptions legible, owned, and recoverable from one case timeline; validate delivered-but-not-received as the first bounded slice.**

This is a discovery recommendation, not a final solution decision. It requires validation with Amazon’s internal delivery, support, refund, and retention data.

## Research method

### Sources and sample

The sample contains 22 public records captured on 2026-08-09:

| Source | Records | Role in analysis |
|---|---:|---|
| India App Store reviews/listing | 7 | Primary app and service experience evidence |
| Google Play / third-party review summaries | 4 | Scale and directional theme context |
| Reddit public discussions | 9 | Qualitative incident and trust narratives |
| Trustpilot | 1 | Service-level customer support context |
| Reviews.io | 1 | Refund-timing context |
| **Total** | **22** | **Directional discovery sample** |

The Stage 0 target was up to 380 records. Only 22 records are included here because public review pages expose uneven, paginated, and sometimes aggregated content in this environment. The smaller sample is explicitly disclosed rather than presented as complete collection.

### Coding framework

Each record was coded for:

- Product, platform, source, URL, date, and access date
- Journey stage
- Theme and subtheme
- Sentiment
- Severity
- Evidence type
- Likely locus: app/product, service/support, policy, payment, seller, logistics, or unknown
- User segment and category when supported
- Business impact signal and requested change

Frequency is sample prevalence: coded records containing a theme divided by 22 records. It is not a market prevalence estimate.

## Key findings

### 1. Delivery exceptions are the central trust break

Public records repeatedly describe orders marked delivered when not received, missing delivery-agent contact, cancellation after delivery promises, or tracking states that do not match reality. This appears across App Store reviews, Reddit, Trustpilot, and aggregator summaries.

**Interpretation:** The customer problem is not simply “late delivery.” It is uncertainty plus lack of recourse when the system state conflicts with the customer’s reality.

### 2. Support is experienced as fragmented rather than owned

Several records describe waiting, repeated contacts, conflicting answers, unavailable chat/call options, or agents who cannot see the same delivery facts. Support is often the second failure after the original fulfilment problem.

**Interpretation:** A support channel may exist, but the customer experience lacks clear case ownership, shared state, and an explicit resolution clock.

### 3. Refund and return confidence is inconsistent

The sample includes concerns about pending refunds, refunds shown as complete before money is received, deductions after damaged delivery, and inconsistent instructions about self-return and eligibility.

**Interpretation:** Customers need a precise explanation of refund state, amount, source, expected settlement date, and next action—not only a “refund issued” status.

### 4. Discovery quality matters, but is less severe in this sample

Sorting and filtering reliability appears in direct App Store feedback, and community discussion raises broader UX and returns concerns. These issues can waste time and reduce consideration, but the observed severity is lower than non-delivery or financial-resolution issues.

### 5. Amazon’s strengths create a sharper expectation gap

Public product documentation and positive summaries emphasize broad selection, convenience, payment choice, returns, and tracking. When an exception occurs, the gap between the promise and the actual resolution can make the experience feel worse than an ordinary delay.

## Theme and severity summary

The companion workbook calculates counts from the coded sample. Directionally:

- Delivery reliability is the most repeated negative journey theme.
- Support access/consistency is the most repeated cross-cutting service theme.
- Refunds/returns are fewer than delivery complaints but high impact because they involve money and fairness.
- Positive themes cluster around selection, convenience, and usability when the core journey works.

The most severe records are concentrated in:

1. False or incomplete delivery outcomes
2. Missing or damaged orders without clear support access
3. Refund deductions, delays, or inconsistent policy explanations

## Top 10 problems

| Rank | Problem | Evidence signal | Severity | Confidence | Business implication |
|---:|---|---|---|---|---|
| 1 | Delivery marked complete when customer did not receive the order | Multiple App Store and service reviews | Critical | High | Trust loss, contacts, refunds, churn |
| 2 | No clear owner for delivery exceptions | App Store, Reddit, Trustpilot | High | High | Repeat contacts and support cost |
| 3 | Delivery-agent contact/status is unavailable or unreliable | App Store and Reddit | High | Medium/High | Missed handoffs and anxiety |
| 4 | Refund state is unclear or slower than promised | Reddit, Reviews.io, aggregators | High | Medium/High | Financial anxiety and escalations |
| 5 | Return instructions differ across agents or channels | Reddit | High | Medium | Rework, delayed refunds, perceived unfairness |
| 6 | Support lacks a consistent cross-channel case timeline | Reddit and App Store | High | Medium/High | Repeated explanations and low confidence |
| 7 | Quantity or cancellation outcomes are not transparent | App Store bulk-order review | Critical | Medium | Event failure and high-value churn |
| 8 | Sorting/filtering does not reliably apply | App Store review | High | Medium | Discovery friction and lower conversion |
| 9 | Customers cannot verify the cause of a failed delivery | App Store and Reddit | Medium/High | Medium | Perceived blame shifting |
| 10 | Prime value is questioned when fulfilment fails | Reddit and review summaries | High | Medium | Subscription dissatisfaction and churn |

## Personas

Detailed personas are in [14_user_personas.md](14_user_personas.md). The primary discovery persona is the **Trust-sensitive exception resolver**: a customer who can tolerate normal delivery variation but needs certainty, ownership, and fair recovery when an order goes wrong.

## Recommended problem statement

> **For Amazon India customers whose order status, delivery outcome, or refund does not match reality, the current experience makes it difficult to understand what happened, reach an accountable owner, and predict the next resolution step. This creates repeated effort, financial anxiety, and loss of trust.**

## Opportunity areas

1. **Unified exception timeline:** one customer-visible timeline connecting order, delivery scan, agent attempt, support case, refund/replacement, and next action.
2. **Confidence-based delivery states:** distinguish “delivered,” “reported delivered,” “investigating,” and “refund/replacement initiated.”
3. **Resolution ownership:** one case owner or queue with a visible SLA and escalation rule.
4. **Refund transparency:** show amount, deductions, source, bank settlement stage, and expected date.
5. **Discovery integrity:** verify that selected sort/filter criteria are applied and visible.

## Research gaps

- Internal incidence rates by city, courier, seller, category, and Prime status
- Actual refund settlement time versus displayed promise
- Support contact rate and repeat-contact rate for delivery exceptions
- Whether customers prefer replacement, refund, or delivery recovery
- Accessibility and language differences across Indian regions
- Whether product-level or logistics-level interventions create the largest retention impact

## Recommendation for Stage 2

Proceed to problem definition with the primary opportunity focused on **delivered-but-not-received exception transparency and ownership**. Keep refund, return, delayed-delivery, and discovery-integrity themes as adjacent opportunities rather than combining them into the first MVP.

## Approval required

1. Approve the primary problem area.
2. Approve delivered-but-not-received as the first product slice, with adjacent refund, return, delayed-delivery, and discovery themes retained for later validation.
3. Approve proceeding to Stage 2 problem definition and opportunity assessment.

**Status: Awaiting approval.**
