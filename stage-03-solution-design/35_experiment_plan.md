# Stage 3 — Experiment Plan

**Solution direction:** Delivered-but-not-received exception timeline and recovery hub
**Status:** Awaiting approval

## Validation objective

Determine whether a unified exception timeline and recovery hub improves customer comprehension, reduces effort, and creates confidence in the next action without increasing incorrect recovery decisions.

## Experiment sequence

| Experiment | Question | Method | Decision |
|---|---|---|---|
| E1 — Concept comprehension | Do customers understand the status, owner, and next action? | 8–10 moderated prototype sessions | Revise language and hierarchy |
| E2 — Recovery choice | Can customers choose the correct recovery path? | 8–10 task-based sessions with delivery/refund scenarios | Keep, simplify, or add human escalation |
| E3 — Agent alignment | Can support agents use the same case state? | 5–7 agent walkthroughs | Confirm operational feasibility |
| E4 — Historical simulation | Would the proposed state have changed prior outcomes? | Replay anonymized exception cases | Estimate addressable volume |
| E5 — Controlled pilot | Does the experience increase confirmed resolution within SLA without unsafe recovery or support burden? | Limited rollout with treatment/control or pre/post comparison | Scale, iterate, or stop |

## E1/E2 usability test

### Participants

- Frequent Amazon India shoppers
- Mix of Prime and non-Prime
- Mix of high-value, remote-area, and time-sensitive purchase experience
- Include participants who have experienced a delivered-but-not-received exception; use refund scenarios only to test explanation of a policy-validated outcome.

### Tasks

1. Report non-receipt from an order marked delivered and explain what happens next.
2. Decide whether to continue investigation, request an eligible recovery, or contact human support.
3. Find who owns the case.
4. Find the next update date.
5. Explain what will happen to the money or replacement.

### Success criteria

- 80% identify the current state correctly.
- 80% identify the next action without facilitator help.
- 75% find owner/queue and next update time.
- 75% choose an eligible recovery path.
- Average perceived confidence improves versus the current-state concept.

## E3 agent walkthrough

Validate:

- event visibility;
- case ownership;
- policy explanation;
- escalation;
- customer-facing versus internal state;
- handling-time impact.

## E4 historical simulation

Use anonymized cases across:

- delivered but not received;
- stale or conflicting delivery evidence;
- recovery eligibility changes between display and confirmation;
- high-risk case requiring human escalation;
- duplicate case or duplicate action retry.

Measure:

- whether the proposed state can be generated;
- which events conflict;
- which cases need human review;
- which recovery actions are policy-safe.

## E5 pilot metrics

### Primary

- Confirmed resolution within promised SLA

### Secondary

- Repeat contacts per exception case
- Time to confirmed resolution
- Recovery completion rate
- First-contact resolution
- Transfer count
- Post-resolution CSAT
- “I understood what would happen next” agreement
- Case reopen rate

### Guardrails

- Incorrect recovery decisions
- False final outcome
- Duplicate financial action
- Source conflict rate
- False-positive exception cases
- Support handle time
- SLA breaches
- Notification opt-outs

## Test instrumentation

- exception_viewed
- timeline_expanded
- recovery_option_viewed
- recovery_option_selected
- case_owner_viewed
- next_update_viewed
- support_contact_started
- case_reopened
- refund_status_viewed
- recovery_completed
- recovery_feedback_submitted

## Decision rules

- **Advance:** usability thresholds pass, no critical safety/policy issue, and pilot shows improved confirmed-resolution-within-SLA signal.
- **Iterate:** customers understand the concept but struggle with recovery choice, ownership, or refund detail.
- **Pause:** event accuracy is unreliable, recovery decisions are unsafe, or customer effort increases.

## Stage 3 approval required

1. Approve Concept A and the exception timeline/recovery hub.
2. Approve E1–E4 before build.
3. Approve the pilot metrics and decision rules.
4. Approve proceeding to Stage 4 PRD and delivery planning after validation.
