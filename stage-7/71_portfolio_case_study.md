# Portfolio Case Study — Amazon India Unified Exception Resolution

## Case study headline

**Turning fragmented post-purchase feedback into a measurable, rollback-safe exception-resolution product.**

## Context

Amazon India’s public promise includes selection, tracking, returns, payments, and support. The worksample examined where that promise breaks for customers whose delivery status or recovery outcome does not match reality.

## My product-management approach

I used a traceable lifecycle rather than treating research, design, delivery, and measurement as separate outputs:

1. **Discover:** define the research question, source plan, coding frame, and evidence limitations.
2. **Understand:** code public records, identify themes, build personas and journey maps.
3. **Define:** write problem statements, an opportunity solution tree, JTBD, and a scored recommendation.
4. **Design:** compare concepts, create service blueprint and low-fidelity Figma flows, and expose risks.
5. **Deliver:** convert the selected direction into a PRD, user stories, acceptance criteria, data contract, rollout plan, and GitHub issues.
6. **Validate:** define usability and feasibility tests, replay synthetic cases, and specify pilot metrics.
7. **Launch and measure:** create readiness, alerting, rollback, post-launch review, and scale-decision artifacts.
8. **Handoff:** package the evidence chain for executive review and future real-pilot ownership.

## Key product decision

Focus the MVP on **delivered but not received**, where delivery truth, support ownership, and recovery confidence intersect. The MVP does not rebuild fulfilment or payment systems; it connects authoritative states into a customer-readable case experience.

## Solution

The proposed experience adds an exception banner, unified timeline, recovery options, and resolution-status loop to the order-detail flow. It is designed around `case_id`, source-of-truth rules, policy eligibility, customer-readable states, and a safe fallback to support.

## Frameworks demonstrated

| Decision | Framework |
|---|---|
| What to learn | Research canvas and hypothesis tree |
| What customers experience | Thematic analysis, affinity mapping, personas, journey mapping |
| What to solve | 5 Whys, problem framing, JTBD |
| What to prioritize | Opportunity solution tree, RICE/value-effort/confidence scoring |
| What to build | Design Sprint-style concept selection, service blueprint, PRD, story mapping |
| How to deliver | Dual-track Agile, RACI, dependency mapping, RAID-style risk review |
| How to validate | Usability testing, assumption testing, experiment design, synthetic case replay |
| Whether to launch | Go/no-go gate, phased rollout, guardrails, rollback plan |
| Whether to scale | Cohort analysis, primary metrics, guardrails, operating review |

## Tools demonstrated

| Tool | Usage in this worksample |
|---|---|
| Excel / Google Sheets equivalent | Feedback coding, theme analysis, scoring, pilot and launch scorecards |
| Figma | Editable wireframes and annotated customer flow |
| GitHub Issues | Backlog, ownership, approval queue, validation tasks, and launch execution |
| Markdown / repository | Versioned PRD, research, decision, operating, and handoff documentation |
| CSV | Reproducible feedback sample and synthetic case replay input |

## What success would require in production

The worksample defines the measurement and decision system, but does not supply live Amazon telemetry. A real team would need to establish a baseline, instrument exposure and outcomes, reconcile source conflicts, run a controlled cohort, monitor safety alerts, and obtain cross-functional approval before scale.

## Portfolio takeaway

The strongest signal is not merely “build a better tracking screen.” It is the product-management insight that exception handling is a cross-system trust journey. The proposed MVP makes the state legible, assigns ownership, offers a policy-safe recovery, and makes the outcome measurable.
