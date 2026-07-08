# Task: SP-02

## Metadata

- Task ID: SP-02
- Category: Strategic Planning
- Difficulty: Medium
- Author: Zhiqi Hu
- Tool Requirement: Prohibited

## Prompt

Create a 12-week strategic launch plan for a pilot AI course-QA assistant at a university department.

Scenario: The pilot will support two undergraduate courses with about 300 total students. The team has one part-time faculty sponsor, two student developers, one teaching assistant, and a $5,000 pilot budget. The assistant can answer questions only from instructor-approved course materials and must include safeguards for hallucination, privacy, academic-integrity concerns, and escalation to human staff.

The plan should define phases, milestones, owners, success metrics, risks, and decision gates for whether to expand the pilot after 12 weeks.

## Required Output Format

Use the following format:
1. Executive summary
2. Goals and non-goals
3. Stakeholder map
4. 12-week roadmap table with phases, tasks, owners, and deliverables
5. Resource and budget allocation
6. Risk register with mitigations
7. Success metrics and data collection plan
8. Governance and escalation process
9. Go / no-go decision criteria for expansion
10. Final recommendation

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Creates a coherent 12-week roadmap with phases, owners, deliverables, and milestones.
2. Addresses all scenario constraints: two courses, 300 students, limited team, $5,000 budget, approved course materials, safeguards, and human escalation.
3. Includes a realistic resource and budget allocation consistent with the scenario.
4. Identifies major risks including hallucination, privacy, academic integrity, adoption, support burden, and scope creep.
5. Defines measurable success metrics and a data collection plan.
6. Provides clear go / no-go decision criteria for expansion after the pilot.

## Required Evidence

No external evidence is allowed. The plan should be based only on the scenario constraints and internal reasoning. Any quantitative assumptions about budget or staffing should be explicitly stated and kept plausible.

## Scoring Rubric

- Accuracy: Judge whether the plan is internally consistent and respects the pilot constraints.
- Completeness: Judge whether all required planning sections and evaluation criteria are covered.
- Helpfulness: Judge whether the plan is actionable for a university department running a limited pilot.
- Hallucination Penalty: Penalize invented university policies, unrealistic budget claims, or unsupported legal/compliance assertions.

## Expected Failure Risks

- Creating a generic launch plan that ignores the course-QA context.
- Failing to include safeguards for hallucination, privacy, or academic integrity.
- Allocating resources unrealistically for the small team and budget.
- Missing measurable success metrics or expansion decision gates.

## Notes

This is a medium strategic planning task because it requires structured planning and risk management under clear constraints.
