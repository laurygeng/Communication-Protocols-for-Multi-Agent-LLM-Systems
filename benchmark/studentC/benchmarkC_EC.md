# Task: EC-03

## Metadata
- **Task ID:** EC-03
- **Category:** Educational Content
- **Difficulty:** Medium
- **Author:** Minjie Geng
- **Tool Requirement:** Prohibited

## Prompt
Design a brief tutorial (approx. 500–700 words) for junior software engineers explaining the differences between Retrieval-Augmented Generation (RAG) and Model Fine-Tuning. Provide a short, practical scenario where a company needs to build an internal knowledge bot based on daily-updated HR policies, and recommend which approach is better.

## Required Output Format
Use the following format:

1. Clear Definitions of RAG and Fine-Tuning.
2. Comparison Matrix (must include exact columns: Approach, Data Freshness, Compute Cost, and Hallucination Mitigation).
3. Scenario Application and Recommendation paragraph.
4. Knowledge Check (a 3-question multiple-choice quiz with an answer key and brief explanations).

## Ground Truth / Evaluation Criteria
The answer should satisfy the following criteria:

- Correctly defines RAG as retrieving external documents to ground the prompt, and Fine-Tuning as updating model weights via training.
- The comparison table includes exactly the requested columns.
- Correctly identifies that RAG offers better "Data Freshness" and lower "Compute Cost" compared to Fine-Tuning.
- Correctly recommends RAG for the HR policy bot because the data updates daily.

## Required Evidence
No external citation required. The task tests pedagogical organization and conceptual accuracy based on established machine learning concepts.

## Scoring Rubric
- **Accuracy:** The definitions of RAG and Fine-Tuning, as well as the quiz answers, must be technically correct.
- **Completeness:** The response must include all 4 formatting sections and the exact table columns.
- **Helpfulness:** The tutorial tone must be suitable for junior software engineers.
- **Hallucination Penalty:** Penalize claims that Fine-Tuning is cheaper than RAG, or recommendations that contradict the scenario's daily-update constraint.

## Expected Failure Risks
- Confusing the use cases (e.g., recommending Fine-Tuning for daily updated facts).
- Failing to use the exact column headers required for the comparison matrix.
- Writing a tutorial that is too academic, ignoring the junior engineer audience.
- Providing a quiz answer key that contradicts the tutorial's text.
