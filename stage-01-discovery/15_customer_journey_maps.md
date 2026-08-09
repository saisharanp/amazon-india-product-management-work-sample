# Stage 1 — Amazon India Customer Journey Maps

## Current-state journey

| Stage | Customer goal | Current experience signal | Pain point | Severity | Opportunity |
|---|---|---|---|---:|---|
| Discover | Find a relevant product | Broad catalog and convenience are praised | Sorting/filtering may not behave as expected | High | Verify and preserve discovery criteria |
| Evaluate | Decide whether to trust the product/seller | Reviews, ratings, price, and selection are core value signals | Review/seller confidence can remain unresolved | Medium | Surface trustworthy decision evidence |
| Checkout | Complete purchase with preferred payment | Amazon Pay/UPI, COD, cards, EMI, and net banking are available | Payment/order state can become unclear after exceptions | Medium/High | Make payment and order state explicit |
| Await delivery | Know when and how the order will arrive | Tracking and delivery promises are central to the proposition | Status, agent contact, and actual outcome can diverge | Critical | Add confidence-based delivery states |
| Receive | Confirm successful handoff | Delivery is expected to be simple and low effort | “Delivered” can be reported without receipt or clear evidence | Critical | Require verifiable handoff and fast dispute flow |
| Recover | Get delivery, replacement, or refund | Returns and refunds are advertised as easy | Support ownership and refund timing are inconsistent in feedback | High/Critical | Unified exception case timeline |
| Reuse | Decide whether to buy again or retain Prime | Selection and convenience support repeat use | Reliability failures damage loyalty and membership value | High | Measure trust recovery and repeat behavior |

## Exception journey: current state

1. Customer sees a delayed, delivered-but-not-received, damaged, or cancelled status.
2. Customer tries to interpret the status and locate the right contact path.
3. Support may provide a different explanation or ask the customer to wait.
4. Customer repeats the issue across agents or channels.
5. Refund/replacement is initiated, but the expected date or amount may be unclear.
6. Customer checks again, escalates, or publicly posts the complaint.

## Exception journey: desired state

1. Amazon detects an exception and labels it clearly.
2. Customer sees what happened, what is known, and what is still being investigated.
3. One case timeline owns the issue across delivery, support, refund, and replacement.
4. Customer chooses an eligible recovery path.
5. Amazon shows owner, SLA, amount, and expected completion date.
6. Customer confirms resolution and optionally rates the recovery experience.

## Service blueprint

| Customer action | Frontstage experience | Backstage capability required | Evidence/metric |
|---|---|---|---|
| Opens order | Sees accurate status and confidence | Event reconciliation across courier, seller, and order systems | Status accuracy |
| Reports non-receipt | Selects simple issue type | Dispute case created with delivery evidence | Non-receipt rate |
| Requests help | Sees owner and next update time | Case routing and escalation policy | First-contact resolution |
| Chooses refund/replacement | Sees eligibility, amount, and date | Policy engine and inventory/payment integration | Recovery completion time |
| Follows progress | Sees one timeline | Shared state across app and support tools | Repeat-contact rate |
| Closes case | Confirms outcome | Feedback event linked to original incident | Recovery CSAT / retention |

## Journey hypotheses for Stage 2

- Customers value a trustworthy next action more than a detailed explanation of every internal event.
- Visible case ownership will reduce repeat contacts even when the underlying delivery failure cannot be prevented.
- Refund clarity may be a stronger trust lever than nominal refund speed for some segments.
- Bulk and high-value orders require a higher-severity escalation policy.
