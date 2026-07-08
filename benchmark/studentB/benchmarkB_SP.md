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

Do not invent university policies or completed pilot results. Clearly label assumptions, keep the plan within the $5,000 budget, and restrict assistant answers to instructor-approved materials.

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

1. Creates a coherent 12-week roadmap with phases, tasks, owners, deliverables, and milestones.
2. Roadmap covers all 12 weeks and includes clear dependencies or sequencing.
3. Addresses the two-course, approximately 300-student scope.
4. Assigns work realistically to one part-time faculty sponsor, two student developers, and one teaching assistant.
5. Provides a realistic $5,000 budget allocation that totals exactly $5,000 or clearly accounts for the full budget.
6. Restricts assistant answers to instructor-approved course materials and explains ingestion/approval boundaries.
7. Includes hallucination safeguards such as citations to course materials, retrieval-only scope, refusal behavior, confidence thresholds, or human review.
8. Includes privacy safeguards for student data, logs, access control, data minimization, and retention assumptions without making unsupported legal claims.
9. Includes academic-integrity safeguards for homework/exam questions, policy-sensitive answers, and inappropriate answer generation.
10. Defines escalation to human staff for uncertainty, missing material, sensitive issues, disputes, or academic-integrity cases.
11. Includes a stakeholder map with relevant project roles and affected users.
12. Includes a risk register with mitigations for hallucination, privacy, academic integrity, adoption, support burden, and scope creep.
13. Defines measurable success metrics such as answer groundedness, citation accuracy, unresolved/escalated questions, student satisfaction, TA workload, adoption, latency, and safety incidents.
14. Includes a data collection plan explaining how metrics will be gathered without over-collecting private data.
15. Includes governance rules for content updates, approvals, escalation ownership, monitoring, and incident review.
16. Provides go/no-go criteria for expansion after 12 weeks with thresholds for expand, revise/extend, or stop.
17. Avoids inventing university policies, approvals, completed results, external laws, or exact performance claims.
18. Balances usefulness, safety, privacy, academic integrity, limited budget, and team capacity.
19. Follows all ten required output sections.
20. Ends with a final recommendation consistent with the evidence and decision gates rather than assuming expansion is automatic.

### Task Type

Strategic planning under resource constraints; external evidence is prohibited.

### Must Have

- Plan must support exactly the scenario: two undergraduate courses, about 300 students, one part-time faculty sponsor, two student developers, one teaching assistant, and a $5,000 pilot budget.
- Assistant must answer only from instructor-approved course materials.
- Plan must include hallucination safeguards, privacy safeguards, academic-integrity safeguards, and escalation to human staff.
- Include a coherent 12-week roadmap with phases, tasks, owners, deliverables, and milestones/decision gates.
- Include stakeholder map covering faculty sponsor, student developers, TA, instructors/students, and department decision-makers.
- Resource and budget allocation must be realistic and total exactly $5,000 or clearly account for the full budget.
- Risk register must include hallucination, privacy, academic integrity, adoption, support burden, and scope creep.
- Success metrics must be measurable and include data collection methods.
- Governance and escalation process must specify when the assistant refuses, cites materials, or routes to humans.
- Go/no-go decision criteria must distinguish expansion, revision/extension, and stopping after 12 weeks.

### Must Not Have

- Do not invent university policies, legal guarantees, institutional approvals, completed pilot results, or exact performance data not provided.
- Do not allow answers outside instructor-approved materials.
- Do not ignore human escalation for uncertain, sensitive, or academic-integrity-related questions.
- Do not allocate resources beyond the small team and $5,000 budget.

### Quantitative Checks

- Roadmap must cover 12 weeks.
- Budget should total exactly $5,000 if itemized; if reserve/contingency is included, it must still sum to $5,000.
- The user population is about 300 students across two courses.

### Acceptable Variations

- The roadmap may group weeks into phases if every week is covered and milestones are clear.
- Budget categories may vary, but they must be plausible for a small pilot and not depend on unprovided funding.
- Success thresholds may vary if measurable and linked to expansion decisions.

### Critical Fail Conditions

- The plan does not restrict answers to instructor-approved course materials.
- The plan lacks hallucination, privacy, academic-integrity, or escalation safeguards.
- The roadmap is not 12 weeks or has no owners/deliverables.
- Budget allocation is missing, unrealistic, or not tied to the $5,000 constraint.

## Required Evidence

No external evidence is allowed. The plan should be based only on the scenario constraints and internal reasoning. Any quantitative assumptions about budget, staffing, usage, or success thresholds must be explicitly stated and plausible. Do not cite vendors, laws, university policies, or institutional procedures unless provided in the prompt. The answer must not invent completed pilot results.

## Scoring Rubric

- **Scoring Method:** Score each evaluation criterion independently: 1 = fully satisfied, 0.5 = partially satisfied or present but underspecified, 0 = absent, incorrect, contradicted, or unsupported. Sum weighted criteria, then apply any hard-fail caps and hallucination penalties.
- **Score Bands:**
  - **Excellent:** 90-100% after caps: satisfies nearly all criteria, respects all hard constraints, and is specific enough to be used as a reference answer.
  - **Good:** 75-89% after caps: mostly correct and complete, with only minor omissions or weak specificity.
  - **Acceptable:** 60-74% after caps: covers the main task but has notable gaps, weak thresholds, weak evidence, or limited actionability.
  - **Poor:** 40-59% after caps: substantial omissions, vague reasoning, missing required sections, or multiple unsupported claims.
  - **Fail:** Below 40% after caps, or any critical contradiction/fabrication that makes the answer unusable.
- **Accuracy:** Judge whether the plan is internally consistent and respects the two-course scope, approved-material restriction, small team, $5,000 budget, 12-week timeline, and required safeguards.
- **Completeness:** Judge whether all planning sections, roadmap, owners, budget, risks, metrics, governance, escalation, and decision criteria are present and specific.
- **Helpfulness:** Reward answers that are concrete, decision-oriented, prioritized, and directly usable by the stated audience. Penalize generic advice that could apply to any scenario.
- **Grounding And Evidence:** For tool-required tasks, every factual product, paper, pricing, policy, benchmark, or empirical claim must be tied to a credible public source. For tool-prohibited tasks, answers must not cite external sources or invent outside facts; they should reason only from the prompt and standard conceptual knowledge.
- **Hallucination Penalty:** Penalize invented university policies, unsupported legal/compliance claims, unrealistic staffing, unrealistic budget allocations, fabricated pilot results, or expansion decisions not tied to measurable thresholds.
- **Hard Fail Rules:**
  - Cap score at 50% if the plan does not restrict answers to instructor-approved course materials.
  - Cap score at 60% if hallucination, privacy, academic-integrity, or escalation safeguards are missing.
  - Cap score at 70% if the roadmap does not cover 12 weeks with owners and deliverables.
  - Cap score at 70% if the budget is missing or does not account for the $5,000 constraint.
  - Cap score at 70% if go/no-go criteria are missing or assume expansion automatically.

## Expected Failure Risks

- Creating a generic launch plan that ignores the course-QA context.
- Failing to include safeguards for hallucination, privacy, or academic integrity.
- Allocating resources unrealistically for the small team and budget.
- Missing measurable success metrics or expansion decision gates.
- Allowing answers beyond instructor-approved course materials.
- Ignoring escalation to human staff.
- Inventing university policies or completed pilot outcomes.
- Assuming expansion without a go/no-go framework.

## Notes

This task should be graded for constraint discipline. A strategic plan that sounds polished but ignores approved-material scope or escalation should not score highly.
