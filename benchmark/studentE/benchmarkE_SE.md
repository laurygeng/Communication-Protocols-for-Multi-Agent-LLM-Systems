# Task: SE-05

## Metadata

- Task ID: SE-05
- Title: Synchronous REST vs. Asynchronous Messaging for Order Fulfillment
- Category: Software Engineering
- Difficulty: Medium
- Author: Student E
- Tool Requirement: Prohibited

## Prompt

A small e-commerce system must process a newly placed order by coordinating three downstream actions:
1. Reserve or deduct inventory.
2. Send an order-confirmation SMS message.
3. Request creation of a shipping label.

Compare two backend integration approaches for coordinating these actions:

1. Synchronous REST orchestration: the order service directly calls the inventory, SMS, and shipping services through synchronous REST APIs and waits for their responses.
2. Asynchronous messaging: the order service publishes an order-created event to a message broker, and each downstream service subscribes to or consumes the event independently, using separate subscriptions or consumer groups where applicable.

Analyze both approaches in terms of:
- Request flow and coupling
- User-facing latency
- Failure isolation and cascading failures
- Retry behavior
- Duplicate delivery and idempotency
- Data consistency and completion visibility
- Implementation and operational complexity

Explain the likely behavior of each design when one downstream service is slow or unavailable. Distinguish synchronous confirmation and potentially stronger immediate coordination from eventual consistency and delayed completion. Do not claim that synchronous REST automatically guarantees strong consistency across services.

Then recommend a suitable architecture for this order-processing scenario. A hybrid design is allowed and may be appropriate. For example, inventory reservation may use a correctness-focused synchronous or transactional mechanism while SMS and shipping-label creation are handled asynchronously. A fully asynchronous recommendation may also be justified if it adequately addresses overselling, message ordering, idempotency, retries, and failure recovery.

Include a comparison table with the columns: Dimension, Synchronous REST, Asynchronous Messaging, Practical Impact.

The response should be approximately 600-800 words. No external citations are required. Use qualitative reasoning and do not invent benchmark results, latency measurements, throughput figures, or reliability percentages.

## Required Output Format

- Type: markdown
- Required sections:
  1. Synchronous REST Approach
  2. Asynchronous Messaging Approach
  3. Comparison Table
  4. Failure and Consistency Analysis
  5. Recommended Architecture
  6. Key Implementation Safeguards

## Evaluation Rubric

### Requirement Coverage — Weight: 0.15

Full credit requires all six required sections; analysis of both integration approaches; coverage of all seven comparison dimensions; discussion of slow or unavailable downstream services; one clear recommendation; and a complete comparison table using all four specified columns. Reduce proportionally for missing sections, dimensions, failure analysis, recommendation, or table content.

### Synchronous Rest Accuracy — Weight: 0.15

Full credit requires a correct explanation that synchronous REST uses direct request-response calls and creates runtime coupling between the order service and downstream services. The answer should recognize that waiting for multiple services can increase user-facing latency and that a slow or failed dependency can cause partial failure or cascading failure. It must not claim that synchronous REST automatically provides distributed strong consistency or atomic completion across all services.

### Asynchronous Messaging Accuracy — Weight: 0.15

Full credit requires a correct explanation that the order service publishes an event and downstream services consume it independently through subscriptions or consumer groups where applicable. The answer should explain reduced runtime coupling, failure isolation, delayed processing, eventual consistency, and the need for broker, consumer, monitoring, and retry infrastructure. It must not assume that asynchronous delivery is automatically exactly once.

### Comparison Quality — Weight: 0.20

Full credit requires direct and technically meaningful comparison across request flow and coupling, user-facing latency, failure isolation, retries, duplicate delivery and idempotency, consistency and completion visibility, and implementation or operational complexity. The comparison table and prose should explain practical consequences for the order scenario rather than listing generic advantages and disadvantages.

### Reliability And Consistency Reasoning — Weight: 0.15

Full credit requires concrete reasoning about cascading failures, partial completion, retry policies, duplicate messages, idempotent consumers or operations, eventual consistency, message ordering where relevant, and failed-message recovery such as dead-letter handling or equivalent mechanisms. The response should explain how order status or step status can make incomplete processing visible. Merely naming these concepts without connecting them to the scenario receives partial credit.

### Recommendation Quality — Weight: 0.15

Full credit requires one clear architecture recommendation tailored to inventory, SMS, and shipping-label creation, supported by at least three scenario-specific reasons. A hybrid recommendation should clearly state which actions are synchronous or transactional and which are asynchronous. A fully asynchronous recommendation can receive full credit only if it credibly addresses overselling, ordering, idempotency, retries, and consistency. The answer must acknowledge at least one tradeoff or limitation of the recommended design.

### Clarity And Evidence Integrity — Weight: 0.05

Full credit requires clear organization, consistent terminology, readable Markdown, the required comparison table, and approximately 600-800 words. Deduct for contradictions, unsupported guarantees, invented performance numbers, claims of exactly-once delivery without qualification, or assertions that the proposed architecture has already been implemented or tested.

## Required Evidence

No external evidence or citations are required. Answer from the prompt, provided constraints, and internal reasoning only.

## Input Files

- None

## Expected Failure Risks

- Claiming synchronous REST automatically guarantees distributed strong consistency.
- Assuming asynchronous messaging provides exactly-once delivery by default.
- Ignoring duplicate delivery, idempotency, ordering, retries, or failed-message recovery.
- Giving a generic recommendation that is not tied to inventory, SMS, and shipping-label requirements.
- Failing to explain partial completion or cascading-failure behavior.
