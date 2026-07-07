
# Task: EC-04

## Metadata

- Task ID: EC-04
- Category: Educational Content
- Difficulty: Hard
- Author: Haofan Hou
- Tool Requirement: Prohibited

## Prompt

Design a 75-minute lesson that teaches precision, recall, F1 score, and decision-threshold tradeoffs in binary classification.

The lesson is intended for a mixed-background audience:

- Some learners understand basic percentages but have no machine-learning experience.
- Some learners already know the definition of a confusion matrix but have difficulty applying the metrics to real decisions.

The lesson must use the following two scenarios:

1. A spam-email filter, where incorrectly blocking a legitimate email is costly.
2. A fraud-detection system, where failing to detect a fraudulent transaction is costly.

Use the following confusion matrix as the main worked example:

|                    | Predicted Positive | Predicted Negative |
|--------------------|-------------------:|-------------------:|
| Actual Positive    | 36                 | 9                  |
| Actual Negative    | 12                 | 43                 |

The lesson must help learners:

- Distinguish true positives, false positives, true negatives, and false negatives.
- Calculate precision, recall, and F1 score from the provided confusion matrix.
- Explain why precision and recall may conflict.
- Understand how changing a decision threshold can affect false positives and false negatives.
- Decide whether precision or recall should receive greater emphasis in each of the two scenarios.
- Recognize that F1 score is useful but does not automatically determine the best real-world decision.

The lesson should balance conceptual explanation, calculation practice, application, misconception correction, and assessment.

## Required Output Format

Use the following structure:

1. Audience analysis
2. Learning objectives
3. 75-minute lesson schedule
4. Concept explanations
5. Worked confusion-matrix example
6. Scenario-based comparison
7. Guided learner activity
8. Common misconceptions and corrections
9. Differentiation strategy
10. Formative assessment
11. Final quiz with answer key
12. Instructor contingency plan
13. Lesson-design rationale

### Lesson Schedule Table

Include a table with the following columns:

| Time | Activity | Instructor Action | Learner Action | Learning Objective |

The schedule must total exactly 75 minutes.

### Worked Example

Show the calculations for:

- Precision
- Recall
- F1 score

Round final numerical answers to three decimal places.

### Scenario Comparison Table

Include a table with the following columns:

| Scenario | More Costly Error | Metric to Emphasize | Explanation | Possible Tradeoff |

### Final Quiz

Create five questions:

- One terminology question
- One calculation question
- One scenario-based application question
- One threshold-tradeoff question
- One question about the limitations of F1 score

Provide an answer key and a brief explanation for each answer.

The response should be approximately 1,000–1,400 words.

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Correctly identifies:
   - True positives as 36
   - False negatives as 9
   - False positives as 12
   - True negatives as 43

2. Correctly calculates precision:

   Precision = 36 / (36 + 12) = 0.750

3. Correctly calculates recall:

   Recall = 36 / (36 + 9) = 0.800

4. Correctly calculates F1 score:

   F1 = 2 × (0.750 × 0.800) / (0.750 + 0.800) ≈ 0.774

5. Clearly explains that precision focuses on the reliability of positive predictions.

6. Clearly explains that recall focuses on the proportion of actual positive cases that are successfully detected.

7. Explains that lowering a positive-class decision threshold generally increases the number of predicted positives, which may increase recall while also increasing false positives.

8. Explains that raising the threshold generally reduces the number of predicted positives, which may improve precision in some situations while increasing false negatives.

9. Correctly connects the spam-filter scenario with concern about false positives, because legitimate emails may be incorrectly blocked.

10. Correctly connects the fraud-detection scenario with concern about false negatives, because fraudulent transactions may be missed.

11. Explains that the preferred metric depends on the relative consequences of different errors rather than on one metric always being superior.

12. Explains at least one limitation of F1 score, such as:
    - It does not include true negatives.
    - It assumes precision and recall deserve equal weight.
    - It does not directly represent the real-world cost of different errors.

13. Provides learning objectives that are observable and assessable.

14. Produces a lesson schedule that totals exactly 75 minutes.

15. Includes activities suitable for both beginner and more experienced learners.

16. Includes at least four realistic misconceptions and specific corrections.

17. Includes both formative assessment and a five-question final quiz with accurate answers.

18. Provides a practical contingency plan for limited time, calculation difficulties, or differences in learner progress.

19. Explains how the lesson design supports conceptual understanding, numerical calculation, and real-world application.

20. Follows all required output structures and tables.

## Required Evidence

No external citations are required.

All numerical information required for the calculations is provided in the prompt.

The answer should use established definitions of confusion-matrix terms, precision, recall, F1 score, and decision thresholds.

Any additional numerical examples must be clearly labeled as hypothetical and must be internally consistent.

## Scoring Rubric

- Accuracy: Definitions, calculations, threshold explanations, scenario interpretations, and quiz answers must be correct.
- Completeness: The response must include all lesson components, both required tables, the worked example, misconception corrections, differentiation, assessments, contingency planning, and design rationale.
- Helpfulness: The lesson should be practical for an instructor to deliver and understandable for learners with different levels of prior knowledge.
- Hallucination Penalty: Penalize incorrect formulas, inconsistent calculations, invented empirical results, unsupported claims that one metric is always best, or contradictions between the lesson content and answer key.

## Expected Failure Risks

- Confusing precision with recall.
- Reversing false positives and false negatives.
- Calculating F1 score incorrectly.
- Treating accuracy and F1 score as interchangeable.
- Claiming that a lower threshold always improves overall system performance.
- Recommending the same metric for both scenarios without discussing error consequences.
- Presenting F1 score as the automatic solution to every classification problem.
- Creating learning objectives that cannot be assessed.
- Producing lesson activities that are too advanced for beginners or too basic for experienced learners.
- Listing misconceptions without explaining how the instructor should correct them.
- Producing a schedule that does not total 75 minutes.
- Writing quiz questions that do not match the lesson objectives.
- Providing an answer key that conflicts with the worked example.
- Omitting a realistic plan for time pressure or uneven learner progress.

## Notes

This task evaluates educational planning, conceptual explanation, mathematical accuracy, audience adaptation, misconception correction, assessment design, and instructional decision-making.
