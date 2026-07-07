# Task: TA-Example
## Metadata
- Task ID: TA-Example
- Category: Technical Analysis
- Difficulty: Medium
- Author: Example Author
- Tool Requirement: Prohibited
## Prompt
Explain the difference between a sequential handoff multi-agent workflow and a shared-blackboard multi-
agent workflow. Compare them in terms of information flow, coordination cost, failure risks, and
suitability for complex knowledge-work tasks. Then recommend which workflow is better for a
research report writing task and justify your answer.
## Required Output Format
Use the following format:
1. Short explanation of sequential handoff
2. Short explanation of shared blackboard
3. Comparison table
4. Recommendation paragraph
5. Potential failure risks
## Ground Truth / Evaluation Criteria
The answer should satisfy the following criteria:
1. Correctly explains that sequential handoff passes outputs forward through an ordered chain.
2. Correctly explains that shared blackboard allows agents to contribute to and read from a shared
workspace.
3. Compares information flow, coordination cost, failure risks, and task suitability.
4. Identifies at least one failure risk for each workflow.
5. Gives a justified recommendation for research report writing.
## Required Evidence
No external citation required. The task is conceptual and should be answered from the given concepts.
## Scoring Rubric
- Accuracy: The explanation of both workflows must be technically correct.
- Completeness: The answer must cover all required comparison dimensions.
- Helpfulness: The recommendation must be clear and actionable.
- Hallucination Penalty: Penalize claims about tools, model performance, or empirical results that are
not provided in the prompt.
## Expected Failure Risks
- Confusing shared blackboard with group chat.
- Ignoring failure risks.
- Giving a recommendation without justification.
