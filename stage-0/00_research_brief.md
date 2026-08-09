# Stage 0 — Research Brief

**Project:** Market analysis of user feedback for two Indian ecommerce apps  
**Working product:** Amazon India  
**Prepared:** 2026-08-09  
**Stage status:** Awaiting approval

## Product-management showcase

This work sample will explicitly demonstrate thematic analysis, JTBD, journey mapping, opportunity solution trees, RICE prioritization, PRD writing, story mapping, usability testing, phased rollout planning, and North Star/funnel measurement. The planned tool workflow is: Notion or Confluence for research documentation, Excel/Google Sheets for evidence and scoring, FigJam/Miro for mapping, Figma for prototyping, Jira/Linear for delivery planning, and Amplitude/Mixpanel/GA4 for measurement. See [04_pm_frameworks_and_tools.md](04_pm_frameworks_and_tools.md) for the full framework-to-artifact map.

## Executive summary

This project will analyze customer feedback for the Amazon India mobile shopping experience and convert the evidence into a portfolio-ready product-management case study. The scope is intentionally limited to one large marketplace so the research can go deeper into discovery, trust, payments, fulfilment, returns, support, and accessibility without dilution from cross-product comparison.

The working hypothesis is that Amazon benefits from strong selection, price visibility, and delivery reach, while the highest-value opportunities may sit at trust and post-purchase moments: product authenticity and review confidence, delivery/return transparency, payment reliability, and resolution quality. This is a hypothesis for testing, not a finding.

Public evidence supports the choice of product: the Amazon India Google Play listing, India App Store listing, and public community discussions provide accessible signals about UX, returns, reviews, reliability, and accessibility. These signals establish research relevance but do not establish prevalence.

## Product selection and rationale

### Selection criteria

Products were selected against these criteria:

1. **Market relevance:** widely used consumer ecommerce apps in the target market.
2. **Journey coverage:** Amazon supports marketplace shopping from search through delivery and returns.
3. **Feedback abundance:** public app-store reviews and other user discussions are available at meaningful volume.
4. **Depth potential:** one-product scope allows deeper segmentation, journey analysis, and evidence review.
5. **Portfolio value:** the work can demonstrate discovery, prioritization, product strategy, and delivery thinking.

### Working product

**Amazon India**  
Scope: India-facing Amazon shopping app (`in.amazon.mShop.android.shopping`). It provides a broad marketplace, shopping, payment, order tracking, and related services. The Google Play listing is a primary source for app metadata, ratings, reviews, and developer-provided privacy information.

### Why not include quick-commerce apps in this phase

Quick-commerce products and other marketplaces are excluded from the baseline analysis. They may be used only as contextual references if the evidence shows that a market benchmark is necessary.

## Research objectives

- Identify recurring, evidence-backed customer problems in the Amazon India app.
- Separate product strengths from service, seller, logistics, and policy complaints.
- Map Amazon’s end-to-end shopping journey and identify the highest-friction moments.
- Estimate problem severity, frequency directionally, and business impact.
- Identify high-confidence opportunities suitable for product discovery.
- Produce an auditable chain from customer evidence to product recommendation.

## Research questions

1. Where do users experience the most friction in search, evaluation, checkout, delivery, returns, and support?
2. Which complaints are app/product issues versus seller, logistics, policy, or expectation issues?
3. Which positive experiences create trust, repeat use, and willingness to recommend?
4. How do trust signals, product reviews, seller quality, and delivery promises affect purchase confidence?
5. Are there differences by user segment, device/platform, geography, category, or purchase value?
6. Which problems appear sufficiently frequent and severe to justify product investment?

## Proposed scope and sampling window

- **Geography:** India; English-language public feedback for the baseline. Indian-language feedback will be noted as a gap unless translation quality and provenance can be maintained.
- **Platforms:** Android first because Google Play provides a large, review-rich public sample; the India App Store will be used as a secondary platform source where accessible.
- **Feedback period:** proposed rolling 12-month window from 2025-08-09 through 2026-08-09, with older high-signal context retained only when it explains a persistent issue.
- **Initial written-review sample:** target 250 reviews from Google Play, stratified by star rating and recency; target 50 reviews from the India App Store where accessible; target 50 relevant public community posts. Final sample counts will be reported after collection.
- **Unit of analysis:** a review/post, with individual claims coded separately when one review contains multiple issues.

## Hypotheses to test

| ID | Hypothesis | Evidence needed | Falsifier |
|---|---|---|---|
| H1 | Post-purchase issues create more severe dissatisfaction than browsing issues. | Coded negative feedback by journey stage and severity. | Browsing/search issues dominate high-severity feedback. |
| H2 | Trust problems cluster around seller/product authenticity, review quality, or misleading listing information. | Direct user claims plus corroborating themes across sources. | Trust themes are rare or isolated after sampling. |
| H3 | Delivery and returns are major drivers of repeat-use intent. | Feedback connecting fulfilment/returns to churn, repeat purchase, or advocacy. | Users report fulfilment issues without impact on relationship. |
| H4 | The two apps differentiate more through service execution than core catalog/search features. | Comparative theme and journey analysis. | Core discovery or pricing differences explain most preference statements. |

## Analysis framework

Each feedback item will be tagged with:

- Product and platform
- Source type, URL, access date, and published date if available
- Star rating or sentiment signal
- Journey stage
- Theme and subtheme
- User segment, inferred only when supported
- Sentiment: positive, mixed, negative, neutral/unclear
- Severity: low, medium, high, critical
- Evidence type: direct observation, opinion, request, allegation, or context
- Likely locus: app/product, seller, logistics, payments, policy, support, or unknown
- Business implication
- Confidence: high, medium, low

Frequency will be reported as sample prevalence, not market prevalence. Sentiment and thematic coding will be directional unless a source provides a statistically valid population sample.

## Timeline and approval gates

| Stage | Output | Gate |
|---|---|---|
| 0 | Research brief, source plan, collection template, risks | Approve products, scope, sample plan, and ethical guardrails |
| 1 | Discovery dataset, coding, findings, personas, journeys, competitor view | Approve the evidence-backed problem area |
| 2 | Problem framing and opportunity prioritization | Approve the opportunity to solve |
| 3 | Concepts, wireframes, service blueprint, experiment plan | Approve the solution direction |
| 4 | PRD, stories, release plan, analytics, QA | Approve MVP and delivery plan |
| 5 | Usability plan and results | Approve changes before build/launch |
| 6 | Launch readiness and go/no-go memo | Approve launch decision |
| 7 | Post-launch evaluation and final case study | Approve outcome and roadmap recommendation |

## Limitations and guardrails

- Public reviews are self-selected and overrepresent unusually positive or negative experiences.
- App-store review counts and rating displays vary by country, platform, and time.
- A review may describe a seller, courier, policy, or payment partner rather than the app itself.
- Ratings should not be treated as equivalent to customer satisfaction or product quality.
- No personal data beyond what is necessary for auditability will be retained; usernames, order IDs, phone numbers, and addresses will be redacted.
- Direct quotations will be short and used only when necessary to preserve meaning; otherwise findings will be paraphrased with attribution.
- Automated collection will not bypass access controls, authentication, robots restrictions, or site terms.

## Decisions required for approval

1. Approve Amazon India as the sole product in scope.
2. Approve India as the market and the 12-month proposed feedback window.
3. Approve Android-first sampling with iOS and community sources as secondary evidence.
4. Approve the proposed target sample and stratification approach.
5. Approve the coding framework and the rule that observed evidence, interpretation, and recommendation remain separate.
6. Approve proceeding to Stage 1 discovery collection.

## Primary sources identified for setup

- [Amazon India Shop, Pay, miniTV — Google Play](https://play.google.com/store/apps/details?hl=en-US&id=in.amazon.mShop.android.shopping)
- [Amazon Shopping — Google Play](https://play.google.com/store/apps/details?id=com.amazon.mShop.android.shopping)
- [Amazon India — India App Store](https://apps.apple.com/in/app/amazon-india-shop-pay-minitv/id1478350915)
- [Reddit discussion: Amazon India UX and returns](https://www.reddit.com/r/IndiaTech/comments/1uujci6/amazon_has_the_worst_ux_out_of_any_shopping_app/)

## Stage 0 status

**Awaiting approval.** No feedback has been coded and no product opportunity has been selected yet.
