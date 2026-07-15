# Task: SP-05

## Metadata

- Task ID: SP-05
- Title: In-House Development vs. Outsourcing for a Three-Month Mobile-App MVP
- Category: Strategic Planning
- Difficulty: Medium
- Author: Student E
- Tool Requirement: Prohibited

## Prompt

A startup must launch a functional mobile-app MVP for both iOS and Android within three months.

Current situation and constraints:
- The startup currently has no mobile developer.
- One technical co-founder can spend up to five hours per week reviewing architecture, code quality, and project progress.
- The company may either hire one full-time mobile developer or outsource the project to an external development agency.
- No additional full-time engineering hires are allowed during the three-month development period.
- The MVP must support user registration and login, a basic user profile, one core product workflow, simple notifications, and basic analytics.
- The app will require bug fixes, operating-system updates, and continued feature development for at least one year after launch.
- The startup values meeting the three-month deadline, but it also wants reasonable quality control, maintainable code, and retention of product knowledge.

Compare the following two primary strategies:
1. Hire one full-time mobile developer and build the MVP internally.
2. Outsource the MVP to an external mobile-development agency.

Analyze both strategies in terms of:
- Speed to begin development
- Probability of meeting the three-month deadline
- Access to design, development, testing, and release expertise
- Management and communication overhead
- Quality control and accountability
- Product knowledge retention
- Intellectual-property and code-ownership considerations
- Post-launch maintenance and continuity
- Main execution risks

Use qualitative strategic reasoning only. Do not provide precise salary figures, agency rates, or total project-cost estimates.

Then recommend one primary strategy for the startup. A phased transition is allowed—for example, outsourcing the MVP while preparing for later internal ownership—but the response must still clearly identify either internal hiring or outsourcing as the main strategy for the three-month delivery period.

The recommendation must include a practical transition and knowledge-transfer plan for the first three months after launch. It must also identify at least three safeguards for the chosen strategy, such as milestone reviews, code-repository ownership, documentation requirements, testing standards, acceptance criteria, handover sessions, or backup staffing.

Include a comparison table with the columns: Dimension, In-House Developer, External Agency, Strategic Impact.

The response should be approximately 700-900 words. No external citations or tools are allowed. Do not invent completed project results or claim that either strategy guarantees delivery.

## Required Output Format

- Type: markdown
- Required sections:
  1. Startup Context and Strategic Priorities
  2. In-House Development Strategy
  3. Outsourcing Strategy
  4. Comparison Table
  5. Recommended Primary Strategy
  6. Three-Month Post-Launch Transition Plan
  7. Key Safeguards and Risks

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. **Requirement Coverage:** Full credit requires all seven required sections; analysis of both strategies; coverage of all nine comparison dimensions; a complete comparison table using all four specified columns; one clearly identified primary strategy; a three-month post-launch transition plan; at least three concrete safeguards; and discussion of important risks. Reduce proportionally for each missing element.
2. **In House Strategy Accuracy:** Full credit requires a realistic assessment of hiring one internal mobile developer under the stated constraints. The answer should recognize the benefits of direct control, stronger product-context retention, and easier long-term continuity, while also addressing recruiting delay, single-person dependency, limited cross-functional coverage, and the risk that one developer must handle design, implementation, testing, and release work. Claims that one developer can automatically provide all required expertise or guarantee the deadline should reduce the score.
3. **Outsourcing Strategy Accuracy:** Full credit requires a realistic assessment of outsourcing to an agency. The answer should recognize faster team availability and access to multiple roles, while also addressing vendor-selection time, communication overhead, scope control, quality variability, intellectual-property and repository ownership, knowledge-transfer risk, and post-launch dependency. Claims that an agency automatically guarantees quality or speed should reduce the score.
4. **Tradeoff Comparison Quality:** Full credit requires direct, scenario-specific comparison across speed to start, deadline feasibility, access to expertise, management overhead, quality control, knowledge retention, intellectual property, maintenance continuity, and execution risk. The table and prose must explain the practical consequences of each tradeoff for this startup rather than listing generic advantages and disadvantages.
5. **Timeline And Feasibility Reasoning:** Full credit requires reasoning that is consistent with the three-month delivery window, the absence of an existing mobile developer, the co-founder's five-hour weekly review limit, and the prohibition on additional full-time engineering hires. The response should account for recruiting or vendor-onboarding time, testing, app-store submission, and the limited scope of the MVP. A plan that ignores these constraints or assumes unlimited internal support should receive no more than half credit.
6. **Recommendation And Transition Planning:** Full credit requires one clear primary strategy supported by at least three scenario-relevant reasons and one acknowledged limitation. The three-month post-launch plan must include concrete ownership-transfer or continuity actions, such as repository access, architecture and deployment documentation, backlog transfer, handover sessions, maintenance ownership, and issue-escalation procedures. A phased recommendation is acceptable only when the main delivery strategy remains explicit.
7. **Clarity And Integrity:** Full credit requires clear organization, consistent terminology, readable Markdown, the required comparison table, and approximately 700-900 words. Deduct for precise market salary or agency-rate figures, unsupported guarantees, invented project results, contradictions with the stated constraints, or vague claims that are not tied to the scenario.

## Required Evidence

No external evidence or citations are required. Answer from the prompt, provided constraints, and internal reasoning only.

## Input Files

- None

## Scoring Rubric

- **Requirement Coverage (0.15):** Full credit requires all seven required sections; analysis of both strategies; coverage of all nine comparison dimensions; a complete comparison table using all four specified columns; one clearly identified primary strategy; a three-month post-launch transition plan; at least three concrete safeguards; and discussion of important risks. Reduce proportionally for each missing element.
- **In House Strategy Accuracy (0.15):** Full credit requires a realistic assessment of hiring one internal mobile developer under the stated constraints. The answer should recognize the benefits of direct control, stronger product-context retention, and easier long-term continuity, while also addressing recruiting delay, single-person dependency, limited cross-functional coverage, and the risk that one developer must handle design, implementation, testing, and release work. Claims that one developer can automatically provide all required expertise or guarantee the deadline should reduce the score.
- **Outsourcing Strategy Accuracy (0.15):** Full credit requires a realistic assessment of outsourcing to an agency. The answer should recognize faster team availability and access to multiple roles, while also addressing vendor-selection time, communication overhead, scope control, quality variability, intellectual-property and repository ownership, knowledge-transfer risk, and post-launch dependency. Claims that an agency automatically guarantees quality or speed should reduce the score.
- **Tradeoff Comparison Quality (0.20):** Full credit requires direct, scenario-specific comparison across speed to start, deadline feasibility, access to expertise, management overhead, quality control, knowledge retention, intellectual property, maintenance continuity, and execution risk. The table and prose must explain the practical consequences of each tradeoff for this startup rather than listing generic advantages and disadvantages.
- **Timeline And Feasibility Reasoning (0.15):** Full credit requires reasoning that is consistent with the three-month delivery window, the absence of an existing mobile developer, the co-founder's five-hour weekly review limit, and the prohibition on additional full-time engineering hires. The response should account for recruiting or vendor-onboarding time, testing, app-store submission, and the limited scope of the MVP. A plan that ignores these constraints or assumes unlimited internal support should receive no more than half credit.
- **Recommendation And Transition Planning (0.15):** Full credit requires one clear primary strategy supported by at least three scenario-relevant reasons and one acknowledged limitation. The three-month post-launch plan must include concrete ownership-transfer or continuity actions, such as repository access, architecture and deployment documentation, backlog transfer, handover sessions, maintenance ownership, and issue-escalation procedures. A phased recommendation is acceptable only when the main delivery strategy remains explicit.
- **Clarity And Integrity (0.05):** Full credit requires clear organization, consistent terminology, readable Markdown, the required comparison table, and approximately 700-900 words. Deduct for precise market salary or agency-rate figures, unsupported guarantees, invented project results, contradictions with the stated constraints, or vague claims that are not tied to the scenario.

## Expected Failure Risks

- Ignoring the three-month deadline or the co-founder's five-hour weekly review limit.
- Assuming one developer or an agency automatically guarantees delivery or quality.
- Failing to address repository ownership, documentation, and knowledge transfer.
- Giving a phased plan without identifying the primary delivery strategy.
- Using invented salary, agency-rate, or completed-project figures.

## Notes


