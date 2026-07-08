# Task: SE-05

## Metadata

- Task ID: SE-05
- Category: Software Engineering
- Difficulty: Medium
- Author: Student E
- Tool Requirement: Prohibited

## Prompt

In an e-commerce system, placing an order needs to trigger several downstream operations: deducting inventory, sending an SMS notification, and generating a shipping label. Compare two architectural approaches for triggering these operations: (1) synchronous REST calls from the order service directly to each downstream service, and (2) an asynchronous message queue (e.g., Kafka), where the order service publishes an event and each downstream service consumes it independently. Compare them in terms of coupling, fault tolerance, latency, and consistency guarantees. Then recommend which approach is better suited for this scenario, and justify your answer.

## Required Output Format

Use the following format:

1. Short explanation of the synchronous REST approach
2. Short explanation of the asynchronous message queue approach
3. Comparison table
4. Recommendation paragraph
5. Potential risks or failure modes of each approach

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Correctly explains that the synchronous approach requires the order service to directly call each downstream service's API and typically wait for responses before completing the order-placement workflow.
2. Correctly explains that the asynchronous approach has the order service publish an event to a topic, with each downstream service consuming it independently as a separate consumer group.
3. Compares coupling (tight vs. loose), fault tolerance and failure isolation, latency (dependent on the slowest downstream service vs. decoupled), and consistency guarantees (immediate vs. eventual consistency).
4. Identifies at least one concrete risk for each approach — e.g., cascading failure for the synchronous approach, or duplicate message delivery requiring idempotent consumers for the asynchronous approach.
5. Gives a justified recommendation for the order-placement scenario (a hybrid approach — synchronous inventory reservation to avoid overselling, combined with asynchronous notification and shipping — is an acceptable and often preferred answer).

## Required Evidence

No external citation required. The task is a conceptual system-design question and should be answered from general software engineering knowledge.

## Scoring Rubric

- Accuracy: The mechanism explanation for both approaches must be technically correct.
- Completeness: The answer must cover all required comparison dimensions (coupling, fault tolerance, latency, consistency).
- Helpfulness: The recommendation must be clear, actionable, and grounded in the specific scenario described.
- Hallucination Penalty: Penalize invented claims about specific performance numbers or benchmarks that are not provided in the prompt.

## Expected Failure Risks

- Treating the two approaches as strictly mutually exclusive instead of recognizing that a hybrid pattern is common in practice.
- Failing to mention idempotency or duplicate-message handling as a risk of the asynchronous approach.
- Confusing "asynchronous" with "unreliable," incorrectly assuming messages can be silently lost.
- Failing to distinguish between core order correctness operations, such as inventory reservation, and non-critical side effects, such as SMS notification.