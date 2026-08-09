# Stage 4 — User Stories and Acceptance Criteria

**Product:** Amazon India
**Feature:** Unified exception resolution — delivered but not received
**Priorities:** P0 = required for pilot; P1 = required before scale; P2 = later slice

## Customer experience requirements

### UR-01 — Surface the exception (P0)

**Story:** As a customer, I want to see that my delivered order needs investigation from the order page so that I do not have to search for support.

**Acceptance criteria:**

- **Given** a delivered scan exists and no confirmed handoff is available, **when** the customer opens the order, **then** an exception banner appears above the standard order summary.
- **Given** a confirmed delivery exists, **when** the customer opens the order, **then** the exception banner is not shown.
- The banner states what is known, what Amazon is checking, and the next update promise or fallback wording.

### UR-02 — Create one case (P0)

**Story:** As a customer, I want one case ID for my delivery issue so that every channel refers to the same incident.

**Acceptance criteria:**

- **Given** a customer reports non-receipt, **when** the action is submitted, **then** the system creates one `case_id` linked to the order and delivery IDs.
- **Given** the same report is retried, **when** the idempotency key matches, **then** the original case is returned and no duplicate case is created.
- The case creation result is visible to the customer within the defined product SLA or shows a retry-safe error.

### UR-03 — Explain the state (P0)

**Story:** As a customer, I want a plain-language timeline so that I understand what happened and what is still being checked.

**Acceptance criteria:**

- **Given** the case has normalized events, **when** the customer opens the timeline, **then** events are ordered by customer-relevant time and show a label, timestamp, and explanatory detail.
- Raw event codes, internal team names, and conflicting source values are not displayed.
- If event sources disagree, the customer sees the safe normalized state and an honest “still checking” explanation.

### UR-04 — Show accountability (P0)

**Story:** As a customer, I want to know who owns the next action so that I know where responsibility sits.

**Acceptance criteria:**

- **Given** an active owner or queue exists, **when** the timeline is shown, **then** the customer sees a customer-readable owner label and next-update time.
- **Given** no owner or SLA exists, **when** the timeline is shown, **then** the experience shows fallback wording and a support contact action.
- Support agents see the same `case_id`, normalized state, owner, and SLA in their workflow.

### UR-05 — Choose recovery safely (P0)

**Story:** As a customer, I want to choose an eligible recovery path with timing and consequences visible so that I can make a confident decision.

**Acceptance criteria:**

- **Given** recovery eligibility is available, **when** the customer opens options, **then** every displayed option includes outcome, expected date, and amount or delivery timing where applicable.
- **Given** an option is ineligible, **when** the eligibility response is returned, **then** the option is not selectable and the customer receives a plain-language reason or support path.
- **Given** a customer selects an option, **when** the request is submitted, **then** the system confirms the selected outcome before processing.

### UR-06 — Prevent duplicate recovery (P0)

**Story:** As a customer, I want repeated taps or app retries to leave my recovery decision unchanged so that I do not receive duplicate refunds or replacements.

**Acceptance criteria:**

- **Given** a recovery request is already accepted, **when** the same idempotency key is replayed, **then** the original request and status are returned.
- **Given** a different recovery option is selected after acceptance, **when** policy permits a change, **then** the case moves through an explicit change state and audit record.
- **Given** policy does not permit a change, **when** a new option is selected, **then** the customer sees the existing accepted outcome and support path.

### UR-07 — Close the loop (P0)

**Story:** As a customer, I want the final outcome and refund/replacement status to be explicit so that I know whether the issue is actually resolved.

**Acceptance criteria:**

- Refund initiation, settlement, replacement dispatch, and confirmed delivery are represented as distinct statuses.
- A resolved case shows the outcome, amount/date or delivery date, owner, and case reference.
- A case cannot display “resolved” until the defined confirmation event is present.

### UR-08 — Contact support when needed (P0)

**Story:** As a customer with a high-risk or ambiguous case, I want a human escalation path so that automation does not block resolution.

**Acceptance criteria:**

- High-value, deadline-sensitive, repeated-contact, policy-ambiguous, and missed-SLA rules route to support.
- The support action carries the existing `case_id` and does not require the customer to repeat the issue summary.
- Contact initiation is tracked as an event linked to the case.

## Platform and operating requirements

### UR-09 — Notification consistency (P1)

Status-change notifications use the same normalized state, owner, next-update time, and recovery outcome as the order page. A notification cannot claim a final outcome before the case record does.

### UR-10 — Accessibility and localization (P0)

The experience supports screen-reader labels, text equivalents for color states, minimum contrast, keyboard navigation where applicable, and copy that can be localized for Amazon India English and supported local-language surfaces.

### UR-11 — Measurement (P0)

The product emits the Stage 3 event taxonomy with `case_id`, `order_id`, `exception_type`, cohort, timestamp, and surface. No payment credentials, full address, or unnecessary personally identifiable information is emitted.

### UR-12 — Audit and support parity (P0)

Every state change, owner change, eligibility decision, recovery selection, and resolution confirmation is auditable. Customer and agent surfaces use the same canonical case state.

## Negative-case test set

1. Delivery scan is stale but no customer report exists.
2. Delivery and payment systems return conflicting timestamps.
3. Replacement inventory disappears between display and selection.
4. Refund eligibility changes between display and confirmation.
5. Notification is retried after the case is resolved.
6. Customer submits the same report from app and web.
7. SLA expires without an owner update.
8. Customer reopens a case after refund initiation but before settlement.
