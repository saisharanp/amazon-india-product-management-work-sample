# Stage 5 — Validation Protocol

**Product:** Amazon India
**Feature:** Unified exception resolution — delivered but not received
**Status:** Field-ready protocol; no live study has been claimed

## 1. Validation objectives

1. Determine whether customers understand the current exception state, owner, and next action.
2. Determine whether customers can choose an eligible recovery path without unnecessary support intervention.
3. Determine whether agents can use the same case state and explain the same promise.
4. Determine whether historical cases can be represented safely by the proposed state model.
5. Define the evidence required before a controlled pilot and before scale.

## 2. Research questions

| ID | Question | Method | Pass threshold |
|---|---|---|---|
| Q1 | Can customers explain what happened? | E1 moderated prototype task | 80% correct current-state explanation |
| Q2 | Can customers find who acts next and when? | E1 task completion | 75% find owner and next-update time |
| Q3 | Can customers choose an eligible recovery? | E2 task with delivery/refund scenarios | 75% choose the safe path |
| Q4 | Can agents resolve using the shared case state? | E3 agent walkthrough | No P0 workflow or parity issue |
| Q5 | Can the state model represent prior incidents? | E4 historical replay | 90% of cases represented without unsafe fallback |
| Q6 | Does the pilot improve outcomes? | E5 controlled pilot | Primary metric improves without guardrail breach |

## 3. Participants and sample

### Customer research

- 8–10 frequent Amazon India shoppers for E1.
- 8–10 additional shoppers for E2, including prior delivery or refund exception experience.
- Mix Prime/non-Prime, high-value, time-sensitive, and remote-area delivery contexts.

### Agent research

- 5–7 support agents or trained proxies for E3.
- Include a mix of delivery-support and general-support workflows.

### Historical replay

- Use anonymized or synthetic cases for E4 during portfolio review.
- Real production replay requires approved access controls, privacy review, and a defined sampling frame.

## 4. Customer tasks

1. Find out why the order is not arriving even though it is marked delivered.
2. Identify the current state and who owns the next action.
3. Find the next update time.
4. Choose whether to wait, request replacement, or request refund.
5. Explain what will happen to the money or replacement.
6. Re-open the case after an outcome and describe what you expect next.

## 5. Data collection

Capture task success, time on task, facilitator intervention, selected option, confidence rating, comprehension statement, accessibility observations, and open-text confusion points. For any future pilot, link product events with `case_id` and cohort while excluding payment credentials and unnecessary personal information.

## 6. Analysis plan

- Compare comprehension and recovery-choice success against the stated thresholds.
- Code confusion by state, owner, timeline, recovery copy, and refund/replacement timing.
- Compare baseline and proposed-experience arms on repeat contacts, resolution hours, understanding, incorrect recovery, and SLA breach.
- Segment by Prime status, order value band, region, event conflict, and human escalation.
- Review guardrails before interpreting primary metrics.

## 7. Decision rules

- **Advance to controlled pilot:** Q1–Q5 thresholds pass, no critical policy/accessibility issue exists, and the operating team can support the cohort.
- **Iterate:** customers understand the problem but struggle with recovery selection, refund timing, or ownership.
- **Pause:** event accuracy is unreliable, recovery is unsafe, support cannot see the same case state, or any critical guardrail is breached.
- **Do not scale from this pack:** the synthetic replay demonstrates analysis mechanics only; scale requires real pilot evidence.

## 8. Ethics and data handling

Do not use real customer text, addresses, payment details, or case identifiers in a portfolio artifact. Real research requires consent, approved recruitment, secure storage, privacy review, and an incident escalation path.
