# Stage 0 — Assumptions, Risks, and Controls

**Project:** Amazon India user-feedback market analysis  
**Prepared:** 2026-08-09  
**Status:** Awaiting approval

## Assumptions

1. Amazon India is sufficiently broad and feedback-rich for a standalone end-to-end product analysis.
2. Public app-store reviews and community posts can provide directional discovery evidence without representing Amazon’s full customer population.
3. A 12-month review window will capture current product/service conditions while limiting historical noise.
4. English-language feedback is a usable first-pass sample for an India-focused portfolio case study.
5. The analyst can distinguish app defects from seller, courier, payment partner, and policy issues with reasonable confidence when the text provides clues.
6. The research objective is opportunity discovery, not causal measurement or market sizing.
7. Any business-impact estimate will be explicitly labeled as an assumption or scenario until validated with internal data.

## Risks and controls

| Risk | Potential impact | Likelihood | Control | Residual risk |
|---|---|---:|---|---:|
| Self-selection bias in public reviews | Overstates extreme experiences | High | Stratify by rating and source; report sample limitations | Medium |
| Review volume or rating differs by locale/platform | Invalid within-product comparison | Medium | Capture country, platform, access date, and displayed counts | Low/Medium |
| Feedback is about seller/courier rather than app | Mis-targeted product recommendation | High | Add likely-locus field and separate product vs service themes | Medium |
| Duplicated or syndicated complaints | Inflated theme frequency | Medium | Deduplicate by text, URL, event, and narrative similarity | Low |
| Access restrictions or review pagination | Incomplete or non-representative sample | Medium | Use accessible public pages only; log unavailable sources | Medium |
| Translation or language bias | Misses non-English needs | Medium | Treat as a stated gap; add Indian-language sampling only with reliable translation | Medium |
| Review manipulation or incentivized feedback | Distorts trust and sentiment findings | Medium | Flag suspicious patterns; do not infer prevalence from allegations | Medium |
| Changing app versions or policies | Mixes old and current experiences | Medium | Record date, app version when available, and change context | Low/Medium |
| Personal data in reviews | Privacy or compliance exposure | Low/Medium | Redact names, order IDs, phone numbers, addresses, and screenshots with identifiers | Low |
| Copyright or terms violations | Legal/reputational risk | Low/Medium | Store short excerpts/paraphrases, cite sources, and avoid bulk republication | Low |
| Business impact is inferred from public anecdotes | Overconfident prioritization | High | Use confidence labels and validate with product analytics/interviews | Medium |

## Quality controls

- Keep source URL, source type, publication date, access date, platform, and product for every record.
- Record the exact text only when needed for coding; otherwise use a faithful, short paraphrase.
- Redact personal identifiers before analysis.
- Apply the coding framework consistently and document changes in an audit trail.
- Sample low-, mid-, and high-star reviews instead of reading only the most visible reviews.
- Keep product feedback separate from marketplace, seller, courier, payment-partner, and policy context.
- Report sample prevalence as `coded items with theme / coded items reviewed`, not as a claim about all users.
- Label evidence as observed, interpreted, or recommended.
- Maintain a “source unavailable” log instead of substituting an unverified source.

## Stop conditions

Pause and request a scope decision if:

- Amazon India cannot provide enough accessible public feedback for a defensible analysis;
- sampling becomes dominated by one source or one single incident;
- the research would require bypassing authentication or access controls;
- a proposed data source would expose personal or sensitive information;
- the available sources no longer represent the Amazon India shopping journey.

## Open questions for the reviewer

1. Should the study remain India-only, or should Amazon’s global app be considered as contextual evidence?
2. Should the analysis cover all categories, or prioritize electronics and high-value purchases where trust and returns may be more consequential?
3. Is the proposed 12-month window appropriate, or should it be shortened to the latest six months?
