# Task: TA-05

## Metadata

- Task ID: TA-05
- Category: Technical Analysis
- Difficulty: Medium
- Author: Student E
- Tool Requirement: Prohibited

## Prompt

Explain the difference between the ReAct (Reasoning and Acting in Language Models) approach and the Reflexion (Language Agents with Verbal Reinforcement Learning) approach to building LLM agents. Compare them in terms of their core mechanism, when and how they are triggered during task execution, how they use memory, and how the two approaches relate to each other (i.e., whether they can be combined). Then recommend which approach — or combination — is better suited for a long-horizon task that may require multiple attempts to succeed, and justify your answer.

## Required Output Format

Use the following format:

1. Short explanation of ReAct
2. Short explanation of Reflexion
3. Comparison table
4. Recommendation paragraph
5. Potential limitations of each approach

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Correctly explains that ReAct interleaves reasoning ("thought") steps with actions and observations within a single task-solving trajectory.
2. Correctly explains that Reflexion adds a verbal self-reflection step after a failed or completed attempt, storing the reflection in memory to inform future attempts across episodes.
3. Compares core mechanism, trigger point, and memory usage (within-episode reasoning trace vs. cross-episode reflective memory).
4. Recognizes that the two approaches are complementary rather than mutually exclusive (e.g., Reflexion can wrap around a ReAct-style actor).
5. Identifies at least one limitation for each approach.
6. Gives a justified recommendation for a long-horizon, multi-attempt task.

## Required Evidence

No external citation required. The task is conceptual and should be answered from the definitions and concepts included in the prompt and general understanding of LLM agent techniques.

## Scoring Rubric

- Accuracy: The explanation of both approaches must be technically correct.
- Completeness: The answer must include the five required output sections and cover core mechanism, trigger point, memory usage, complementarity, limitations, and recommendation.
- Helpfulness: The recommendation must be clear and actionable.
- Hallucination Penalty: Penalize claims about specific benchmark numbers or empirical results that are not provided in the prompt.

## Expected Failure Risks

- Confusing ReAct's "thought" step with Reflexion's "reflection" step — both involve generating reasoning text, but operate at different timescales and granularities.
- Treating the two approaches as mutually exclusive instead of recognizing they can be combined.
- Ignoring the memory difference between within-episode reasoning (ReAct) and cross-episode reflective memory (Reflexion).
- Giving a recommendation without connecting it to the long-horizon, multi-attempt nature of the task.