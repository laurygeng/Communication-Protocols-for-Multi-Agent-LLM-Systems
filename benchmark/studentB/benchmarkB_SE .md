# Task: SE-02

## Metadata

- Task ID: SE-02
- Category: Software Engineering
- Difficulty: Hard
- Author: Zhiqi Hu
- Tool Requirement: Prohibited

## Prompt

Design a high-level architecture for a multi-tenant AI support-ticket triage system.

Scenario: A SaaS company receives about 10,000 support tickets per day across 20 enterprise tenants. The system must classify each ticket by issue type and urgency, redact personal data before any third-party model call, route high-risk tickets to human review, preserve audit logs for compliance review, and allow each tenant to customize routing rules. The target p95 classification latency is 2 seconds per ticket during normal load. If the AI component is unavailable or uncertain, the system must fail safely rather than dropping tickets.

Produce an architecture proposal that balances scalability, privacy, reliability, observability, implementation complexity, and cost. You do not need to write production code.

## Required Output Format

Use the following format:
1. Assumptions and non-goals
2. Component diagram described in text
3. End-to-end data flow
4. Key services and responsibilities table
5. Privacy and compliance safeguards
6. Reliability and failure-handling plan
7. Latency and throughput reasoning
8. Testing and rollout plan
9. Major risks and mitigations
10. Final recommendation

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Proposes a coherent architecture with clear components such as ingestion, queueing, redaction, classification, rules engine, human review, audit logging, and monitoring.
2. Explains an end-to-end data flow that preserves tenant separation and avoids dropping tickets.
3. Addresses privacy by placing PII detection/redaction before third-party model calls and preserving auditability.
4. Includes a realistic reliability plan with retries, fallbacks, uncertainty thresholds, dead-letter handling, and human escalation.
5. Provides throughput and latency reasoning for 10,000 tickets per day and the 2-second p95 target.
6. Balances competing goals: scalability, privacy, reliability, observability, cost, and implementation complexity.
7. Includes a concrete testing and phased rollout plan, including tenant-specific configuration validation.

## Required Evidence

No external evidence is allowed. The answer should use reasoning from the scenario. Simple calculations or estimates are required for throughput and latency assumptions. Do not cite vendors, laws, or private data sources.

## Scoring Rubric

- Accuracy: Judge whether the architecture is technically plausible and respects the scenario constraints.
- Completeness: Judge whether all required sections and constraints are covered, especially redaction, tenant isolation, fail-safe routing, audit logs, and latency reasoning.
- Helpfulness: Judge whether the proposal is actionable enough for an engineering team to refine into a design document.
- Hallucination Penalty: Penalize unsupported claims about specific cloud products, laws, model performance, or exact costs that are not provided in the prompt.

## Expected Failure Risks

- Designing only the AI classifier while ignoring routing, audit, and human review.
- Sending unredacted data to a third-party model.
- Missing fail-safe behavior when the model is unavailable or uncertain.
- Providing no latency or throughput reasoning.
- Ignoring multi-tenant isolation and tenant-specific rules.

## Notes

This is a hard software engineering task because it contains competing constraints and requires architectural synthesis, risk management, and verification planning.
