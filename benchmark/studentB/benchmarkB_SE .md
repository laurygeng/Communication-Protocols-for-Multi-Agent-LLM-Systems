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

Do not cite vendors, laws, exact costs, or model-performance numbers not provided in the scenario. Clearly label any assumption.

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

1. Proposes a coherent architecture with ingestion, queueing/buffering, redaction, classification, rules/routing, human review, audit logging, monitoring, and storage/configuration components.
2. Explains an end-to-end data flow from ticket intake through classification, routing, review, logging, and final handoff.
3. Preserves tenant separation in data storage, configurations, routing rules, logs, metrics, and access controls.
4. Places PII detection/redaction before any third-party model call and explains how redaction quality is checked.
5. Classifies both issue type and urgency and connects outputs to routing decisions.
6. Routes high-risk, sensitive, ambiguous, or low-confidence tickets to human review.
7. Includes fail-safe behavior for AI unavailability, model timeout, low confidence, redaction failure, and rules-engine failure.
8. Includes retries, timeouts, backpressure, dead-letter queues or equivalent handling without dropping tickets.
9. Preserves audit logs for compliance review while minimizing sensitive data exposure.
10. Allows tenant-specific routing rules and includes validation, versioning, rollback, or approval for configuration changes.
11. Provides simple throughput reasoning for 10,000 tickets/day and acknowledges peak/burst traffic rather than relying only on daily average.
12. Provides latency reasoning for the 2-second p95 target, including approximate latency budget, timeouts, and fast fallback path.
13. Addresses observability with metrics, traces/logs, alerts, quality monitoring, and auditability.
14. Balances scalability, privacy, reliability, observability, implementation complexity, and cost in architectural tradeoffs.
15. Includes a concrete testing plan covering unit/integration tests, redaction tests, rules tests, tenant-isolation tests, load tests, and failure injection.
16. Includes a phased rollout plan with limited tenants, shadow mode or human-in-the-loop validation, and rollback criteria.
17. Identifies major risks and mitigations, including privacy leakage, misrouting, latency spikes, tenant misconfiguration, model drift, and support burden.
18. Follows the required ten-section output format.
19. Avoids unsupported vendor, law, certification, exact-cost, or exact-model-performance claims.
20. Provides a final recommendation that is actionable for an engineering team and consistent with all stated constraints.

### Task Type

Architecture design under stated constraints; external evidence is prohibited.

### Must Have

- Include coherent components for ingestion/API, tenant isolation, queueing or buffering, PII detection/redaction, AI classification, routing/rules engine, human review, audit logging, configuration management, monitoring/observability, and storage.
- Redact personal data before any third-party model call; this ordering is mandatory.
- Preserve tenant separation across data, configuration, logs, and routing rules.
- Classify by issue type and urgency and route high-risk or uncertain tickets to human review.
- Fail safely when the AI component is unavailable or uncertain; tickets must not be dropped.
- Retain audit logs sufficient for compliance review without exposing unnecessary sensitive data.
- Allow tenant-specific routing rules while validating changes safely.
- Reason about 10,000 tickets/day across 20 tenants and the p95 2-second target using simple calculations or capacity assumptions.
- Balance scalability, privacy, reliability, observability, implementation complexity, and cost.
- Include testing and phased rollout, including tenant-specific configuration validation.

### Must Not Have

- Do not send unredacted PII to a third-party model.
- Do not drop tickets when queues, classifiers, or external model calls fail.
- Do not assume exact cloud products, laws, compliance certifications, model performance, or dollar costs not stated in the prompt.
- Do not ignore multi-tenant isolation or tenant-specific routing rules.

### Quantitative Checks

- 10,000 tickets/day is approximately 0.116 tickets/second on average; the answer should mention that peak load may be much higher and design for bursts rather than average only.
- p95 classification latency target is 2 seconds per ticket during normal load; the design should include latency budget, async boundaries, timeouts, or fallback routing.

### Acceptable Variations

- The component diagram may be textual or ASCII-style as long as components and data flow are clear.
- The architecture may be synchronous, asynchronous, or hybrid if it explains how latency and fail-safe behavior are preserved.
- The classifier may be third-party, in-house, or hybrid, but PII redaction before third-party calls is non-negotiable.

### Critical Fail Conditions

- PII is sent to a third-party model before redaction.
- The architecture has no fail-safe path for AI unavailability or uncertainty.
- The answer ignores tenant isolation.
- The answer provides no throughput or latency reasoning.

## Required Evidence

No external evidence is allowed. The answer should use only the scenario and standard architecture reasoning. Simple calculations are required for throughput and latency. Do not cite vendors, laws, benchmarks, compliance certifications, exact costs, or private data sources unless the prompt explicitly provides them.

## Scoring Rubric

- **Scoring Method:** Score each evaluation criterion independently: 1 = fully satisfied, 0.5 = partially satisfied or present but underspecified, 0 = absent, incorrect, contradicted, or unsupported. Sum weighted criteria, then apply any hard-fail caps and hallucination penalties.
- **Score Bands:**
  - **Excellent:** 90-100% after caps: satisfies nearly all criteria, respects all hard constraints, and is specific enough to be used as a reference answer.
  - **Good:** 75-89% after caps: mostly correct and complete, with only minor omissions or weak specificity.
  - **Acceptable:** 60-74% after caps: covers the main task but has notable gaps, weak thresholds, weak evidence, or limited actionability.
  - **Poor:** 40-59% after caps: substantial omissions, vague reasoning, missing required sections, or multiple unsupported claims.
  - **Fail:** Below 40% after caps, or any critical contradiction/fabrication that makes the answer unusable.
- **Accuracy:** Judge whether the architecture is technically plausible, internally consistent, and respects redaction-before-model, tenant isolation, fail-safe routing, auditability, and latency constraints.
- **Completeness:** Judge whether all required sections and all scenario constraints are covered, especially privacy ordering, fail-safe handling, tenant-specific rules, throughput, and p95 latency reasoning.
- **Helpfulness:** Reward answers that are concrete, decision-oriented, prioritized, and directly usable by the stated audience. Penalize generic advice that could apply to any scenario.
- **Grounding And Evidence:** For tool-required tasks, every factual product, paper, pricing, policy, benchmark, or empirical claim must be tied to a credible public source. For tool-prohibited tasks, answers must not cite external sources or invent outside facts; they should reason only from the prompt and standard conceptual knowledge.
- **Hallucination Penalty:** Penalize unsupported claims about named cloud products, legal compliance, exact model accuracy, exact costs, or guaranteed 2-second performance without reasoning. Penalize any design that silently drops tickets or bypasses redaction.
- **Hard Fail Rules:**
  - Cap score at 40% if unredacted PII is sent to a third-party model.
  - Cap score at 50% if there is no fail-safe path when AI is unavailable or uncertain.
  - Cap score at 60% if tenant isolation is missing or superficial.
  - Cap score at 70% if throughput and latency reasoning are absent.
  - Cap score at 70% if audit logging or human review is missing.

## Expected Failure Risks

- Designing only the AI classifier while ignoring routing, audit, and human review.
- Sending unredacted data to a third-party model.
- Missing fail-safe behavior when the model is unavailable or uncertain.
- Providing no latency or throughput reasoning.
- Ignoring multi-tenant isolation and tenant-specific rules.
- Assuming average daily traffic is enough to satisfy p95 latency.
- Omitting redaction validation and failure handling.
- Making unsupported compliance or vendor-performance claims.

## Notes

This hard architecture task should be graded for ordering and failure behavior, not only for listing plausible components.
