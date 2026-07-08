# Task: SP-05

## Metadata

- Task ID: SP-05
- Category: Strategic Planning
- Difficulty: Medium
- Author: Student E
- Tool Requirement: Optional

## Prompt

A startup needs to build a mobile app within 3 months. Compare two resourcing strategies: (1) hiring a full-time in-house developer, and (2) outsourcing to a contract development agency. Compare them in terms of cost, development speed, quality control, and post-launch maintenance or knowledge retention. Then recommend which strategy is better suited for this scenario, and justify your answer.

## Required Output Format

Use the following format:

1. Short explanation of the in-house hiring approach
2. Short explanation of the outsourcing approach
3. Comparison table
4. Recommendation paragraph
5. Potential risks of each approach

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Correctly explains that hiring in-house involves recruiting, onboarding, and paying a full-time salary and benefits, giving direct day-to-day control over the developer's work.
2. Correctly explains that outsourcing involves contracting an external agency or team, typically billed per project or per hour, with less direct day-to-day control.
3. Compares cost structure, development speed (hiring/onboarding time vs. faster ramp-up from an experienced agency), quality control (direct oversight vs. reliance on contract terms and agency reputation), and post-launch maintenance or knowledge retention.
4. Identifies at least one concrete risk for each approach (e.g., in-house: a slow hiring process may blow the 3-month timeline; outsourcing: communication overhead and loss of domain knowledge after the contract ends).
5. Gives a justified recommendation grounded in the specific scenario (3-month timeline, startup context) rather than a generic "it depends."

## Required Evidence

Tool use is optional. If a tool is used, the answer should cite reputable sources
for approximate salary or contracting rate ranges. If no tool is used, the answer
should rely on general, reasonable industry knowledge without presenting invented
precise figures as verified fact.

## Scoring Rubric

- Accuracy: Cost, speed, and quality claims must be technically reasonable and internally consistent, whether or not tool-verified.
- Completeness: The answer must cover cost, development speed, quality control, post-launch maintenance or knowledge retention, concrete risks for both approaches, and provide a clear recommendation.
- Helpfulness: The recommendation must be clear, actionable, and grounded in the 3-month startup scenario.
- Hallucination Penalty: Penalize precise numeric figures (e.g., an exact dollar amount) presented as verified fact when no tool was actually used to retrieve them.

## Expected Failure Risks

- Presenting a fabricated precise number as if it were verified, when no tool was actually used — the key hallucination risk specific to Optional-tool tasks.
- Giving a noncommittal "it depends" answer without a clear recommendation.
- Ignoring the 3-month timeline constraint, which is central to judging which option carries more schedule risk.
- Ignoring post-launch maintenance or knowledge retention after the initial 3-month build.