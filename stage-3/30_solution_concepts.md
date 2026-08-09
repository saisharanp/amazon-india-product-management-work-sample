# Stage 3 — Solution Concepts

**Product:** Amazon India  
**Approved opportunity:** Unified exception resolution  
**Concept focus:** Delivery, support ownership, recovery choice, and refund/replacement status  
**Status:** Awaiting approval

## Design principles

1. **One truth for the customer:** show the current state, what is known, and what is still being investigated.
2. **One accountable next step:** customers should not have to guess who acts next.
3. **Recovery before explanation:** surface the practical path to delivery, replacement, or refund.
4. **Progressive detail:** keep the first view simple; expose evidence and policy detail when needed.
5. **Accessible under stress:** use plain language, strong hierarchy, status text plus color, and screen-reader-friendly labels.
6. **Operationally honest:** never promise a date or outcome that the underlying system cannot support.

## Concept A — Exception timeline and recovery hub

### Experience

The order page changes into an exception hub when a delivery, return, or refund issue is detected. The customer sees:

- Current status and confidence
- Timeline of key events
- Case owner or responsible queue
- Next update time
- Recovery choices
- Refund/replacement status
- Contact and escalation actions

### MVP scope

- Customer-visible event timeline
- Plain-language exception state
- Single case ID and owner/queue
- Next update SLA
- Recovery choice: refund, replacement, or continue delivery investigation
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

**Recommend Concept A — Exception timeline and recovery hub**, with the first MVP flow focused on one high-severity exception type. It provides the clearest customer value while creating a practical boundary for later support tooling and proactive detection.

## Proposed MVP flow

1. Customer opens an affected order.
2. Amazon displays the exception state in plain language.
3. Customer sees what happened, what is known, and what happens next.
4. Customer chooses recovery if eligible.
5. A case ID, owner/queue, and next update time are shown.
6. Customer receives status updates until the case is resolved.

## Out of scope for MVP

- Rebuilding delivery-event infrastructure
- Predicting every possible exception
- Full seller-quality remediation
- New refund policy
- Full support-agent console replacement
- Marketplace-wide search redesign

## Approval required

1. Approve Concept A as the solution direction.
2. Confirm the first MVP exception type for prototyping.
3. Approve proceeding to PRD and delivery planning after validation.
