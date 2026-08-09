# Stage 3 — Solution Concepts

**Product:** Amazon India  
**Approved opportunity:** Delivered-but-not-received resolution layer
**Concept focus:** Truthful state, support ownership, safe escalation, and policy-validated recovery
**Status:** Awaiting approval

## Design principles

1. **One truth for the customer:** show the current state, what is known, and what is still being investigated.
2. **One accountable next step:** customers should not have to guess who acts next.
3. **Explanation before recovery:** make the current state and owner clear before showing a policy-validated recovery path.
4. **Progressive detail:** keep the first view simple; expose evidence and policy detail when needed.
5. **Accessible under stress:** use plain language, strong hierarchy, status text plus color, and screen-reader-friendly labels.
6. **Operationally honest:** never promise a date or outcome that the underlying system cannot support; use an investigation state when sources conflict.

## Concept A — Exception timeline and recovery hub

### Experience

The order page changes into an exception hub when an eligible delivered-but-not-received report is submitted. The customer sees:

- Current status and confidence
- Timeline of key events
- Case owner or responsible queue
- Next update time
- Policy-validated recovery choices or a human-review path
- Refund/replacement status
- Contact and escalation actions

### MVP scope

- Customer-visible event timeline
- Plain-language exception state
- Single case ID and owner/queue
- Next update SLA
- Recovery choice only after policy eligibility is confirmed; no independent automated financial action in the first pilot
- Push/in-app update when the state changes

### Expected benefit

Reduce repeated contacts and uncertainty by giving customers a shared view of the issue and the next action.

### Risks

- Cross-system event reconciliation
- Status conflicts exposed to customers
- Complex edge-case policy handling

## Concept B — Guided recovery wizard

### Experience

The customer answers a short set of questions—received or not, item condition, urgency, preferred outcome—and receives the eligible recovery path.

### MVP scope

- Guided issue classification
- Recovery recommendation
- Refund/replacement selection
- Case creation and confirmation
- Follow-up status page

### Expected benefit

Reduce navigation and policy confusion, especially for non-receipt and damaged-order cases.

### Risks

- Wizard may feel like deflection from human support
- Incorrect classification could create a bad recovery path
- Less transparent than a timeline for complex cases

## Concept C — Proactive exception concierge

### Experience

Amazon detects a likely fulfilment exception and contacts the customer before they report it. The message explains the risk, provides options, and assigns a case owner.

### MVP scope

- Proactive notification for selected exception patterns
- Delivery/refund options
- One-tap confirmation
- Escalation for high-value or deadline-sensitive orders

### Expected benefit

Prevent surprise and reduce inbound contacts before the customer becomes frustrated.

### Risks

- False positives create unnecessary anxiety
- Requires reliable predictive signals
- May increase notification fatigue

## Concept D — Support case command center

### Experience

The customer receives a case page that shows the owner, evidence, contact history, policy decision, and next escalation point. The primary investment is shared agent tooling, with a lighter customer-facing view.

### MVP scope

- Structured case record
- Shared event and contact history
- Agent ownership and SLA
- Customer-facing case status

### Expected benefit

Reduce conflicting answers and repeated explanations across support channels.

### Risks

- Can become an internal operations project
- Customer value may remain invisible
- Requires significant support-system integration

## Recommended concept

**Recommend Concept A — Exception timeline and recovery hub**, with the first MVP strictly focused on delivered-but-not-received reports. It provides the clearest customer value while creating a practical boundary for later support tooling, proactive detection, and adjacent exception types.

## Proposed MVP flow

1. Customer opens an order marked delivered and reports non-receipt.
2. Amazon creates or retrieves one case and displays a truthful investigation state.
3. Customer sees what happened, what is known, who owns the next action, and the next update time.
4. Customer receives a policy-validated recovery choice or human escalation path.
5. The case records the outcome and updates the customer until confirmed resolution.

## Out of scope for MVP

- Rebuilding delivery-event infrastructure
- Independent automated refund or replacement execution
- Predicting every possible exception
- Full seller-quality remediation
- New refund policy
- Full support-agent console replacement
- Marketplace-wide search redesign

## Approval required

1. Approve Concept A as the solution direction.
2. Confirm the first MVP exception type for prototyping.
3. Approve proceeding to PRD and delivery planning after validation.
