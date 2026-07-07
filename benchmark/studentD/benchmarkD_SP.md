
# Task: SP-04

## Metadata

- Task ID: SP-04
- Category: Strategic Planning
- Difficulty: Hard
- Author: Haofan Hou
- Tool Requirement: Prohibited

## Prompt

Create a 12-week strategy for piloting and deciding whether to launch an AI-powered customer-support assistant for a mid-sized e-commerce company.

The company currently handles approximately 50,000 customer-support requests per month.

Current performance:

- Average first-response time: 18 hours
- Customer satisfaction score: 78%
- Support agents frequently spend time answering repetitive questions
- Refunds, account changes, and payment disputes require human approval

The company wants the pilot to achieve the following goals:

- Reduce average first-response time to 8 hours or less
- Increase customer satisfaction to at least 84%
- Reduce repetitive workload for support agents
- Avoid unsafe or unauthorized actions
- Protect customer and payment-related information

The project has the following constraints:

- Total budget: $180,000
- Total duration: 12 weeks
- A limited pilot must begin by the end of Week 8
- A final launch, revision, or cancellation decision must be made by the end of Week 12
- The system may draft responses and recommend actions, but it may not independently issue refunds, modify accounts, or resolve payment disputes
- Payment-card information must not be included in model inputs
- The project team consists of:
  - 1 Product Manager
  - 1 Machine Learning Engineer
  - 1 Backend Engineer
  - 0.5 Full-Time Data Analyst
  - 0.5 Full-Time Customer Support Lead
  - 0.25 Full-Time Privacy and Legal Specialist
- Eight customer-support agents may participate in testing for no more than two hours per person per week

Develop a practical strategy that balances delivery speed, service quality, employee workload, privacy, safety, and budget.

The plan must also address the following two possible disruptions:

1. At the end of Week 6, the available budget may be reduced by 20%.
2. At the end of Week 9, the pilot may show faster response times but fail to reach the customer-satisfaction target.

## Required Output Format

Use the following structure:

1. Executive summary
2. Strategic objectives and priorities
3. Assumptions and scope boundaries
4. Twelve-week phased roadmap
5. Team responsibilities
6. Budget allocation
7. Pilot design
8. Success metrics and decision thresholds
9. Risk register
10. Disruption-response plans
11. Final decision framework
12. Short conclusion

### Roadmap Table

Include a table with the following columns:

| Phase and Weeks | Main Activities | Deliverables | Responsible Roles | Exit Criteria |

The roadmap must:

- Cover all 12 weeks
- Show important dependencies
- Start the limited pilot no later than the end of Week 8
- Include a final decision by the end of Week 12

### Budget Table

Allocate the full $180,000 budget using the following columns:

| Budget Category | Amount | Purpose | Priority if Budget Is Reduced |

The amounts must total exactly $180,000.

### Success Metrics Table

Include:

| Metric | Baseline | Target | Measurement Method | Go/No-Go Threshold |

The metrics must address:

- Response time
- Customer satisfaction
- Workload reduction
- Response quality
- Safety or unauthorized-action rate
- Privacy compliance
- Pilot adoption or usage

### Risk Register

Include at least six risks using:

| Risk | Likelihood | Impact | Early Warning Sign | Mitigation | Contingency Owner |

The response should be approximately 1,000–1,400 words.

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Defines clear strategic priorities that balance speed, quality, safety, privacy, employee workload, and cost.
2. Establishes realistic scope boundaries for the assistant, including mandatory human approval for refunds, account changes, and payment disputes.
3. Produces a complete 12-week roadmap with clear phases, dependencies, deliverables, and exit criteria.
4. Begins the limited pilot no later than the end of Week 8.
5. Includes a final launch, revision, or cancellation decision by the end of Week 12.
6. Assigns responsibilities that are consistent with the provided team capacity.
7. Does not assign more than two testing hours per week to each participating support agent.
8. Allocates a budget totaling exactly $180,000.
9. Identifies which budget items should be protected, reduced, delayed, or removed if the budget is cut by 20%.
10. Defines measurable pilot metrics for response time, customer satisfaction, workload, quality, safety, privacy, and adoption.
11. Provides clear go/no-go thresholds rather than listing goals without decision rules.
12. Explains how pilot data will be collected and evaluated.
13. Includes at least six relevant risks with early warning signs, mitigation actions, owners, and contingency responses.
14. Addresses privacy risks involving customer and payment-related information.
15. Addresses the possibility of unsafe, incorrect, or unauthorized recommendations.
16. Provides a practical response to the Week 6 budget reduction scenario.
17. Provides a practical response to the Week 9 scenario in which response time improves but customer satisfaction remains below target.
18. Avoids assuming that improved speed alone is sufficient for launch.
19. Includes a decision framework that distinguishes among launch, limited extension or revision, and cancellation.
20. Follows all required structures and tables.

## Required Evidence

No external citations are required.

The plan should be based entirely on the company information, goals, resources, and constraints provided in the prompt.

Budget calculations must be internally consistent.

Any additional assumptions must be clearly labeled and must not contradict the provided constraints.

The answer must not invent completed pilot results or claim that the strategy has already been tested.

## Scoring Rubric

- Accuracy: The roadmap, staffing plan, budget, metrics, dependencies, and risk responses must be internally consistent and respect all stated constraints.
- Completeness: The response must include all required sections, tables, strategic objectives, disruption plans, risks, and final decision rules.
- Helpfulness: The strategy should be specific, practical, prioritized, and usable by the company’s project team.
- Hallucination Penalty: Penalize invented project results, unsupported guarantees, contradictory assumptions, incorrect budget totals, or claims that ignore the stated staffing, privacy, safety, and timeline constraints.

## Expected Failure Risks

- Creating a general roadmap that does not assign specific weeks, owners, deliverables, or exit criteria.
- Failing to start the limited pilot by the end of Week 8.
- Producing a budget that does not total exactly $180,000.
- Assigning more work than the available staff can reasonably complete.
- Exceeding the support-agent testing-time limit.
- Treating response-time improvement as sufficient evidence for launch.
- Ignoring customer satisfaction, response quality, privacy, or safety.
- Allowing the system to perform refunds, account changes, or payment-dispute actions without human approval.
- Providing vague success metrics without measurable thresholds.
- Listing risks without early warning signs, mitigation plans, or responsible owners.
- Responding to the 20% budget reduction by cutting critical privacy or safety work.
- Recommending immediate cancellation when the Week 9 results may support targeted revision.
- Failing to distinguish between launch, extended pilot, revision, and cancellation.
- Inventing pilot outcomes or claiming guaranteed business benefits.

## Notes

This task evaluates strategic prioritization, phased planning, resource allocation, risk management, contingency planning, and evidence-based decision-making.