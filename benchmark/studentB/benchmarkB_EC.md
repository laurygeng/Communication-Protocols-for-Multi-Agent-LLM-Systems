# Task: EC-02

## Metadata

- Task ID: EC-02
- Category: Educational Content
- Difficulty: Medium
- Author: Zhiqi Hu
- Tool Requirement: Prohibited

## Prompt

Create a 50-minute introductory lesson plan for teaching dynamic programming using the coin change problem to undergraduate computer science students.

The students already know arrays, loops, and recursion, but many of them confuse greedy algorithms with dynamic programming. The lesson should emphasize when dynamic programming is appropriate, how to define subproblems, how to write the recurrence, and how to build the bottom-up table.

State which coin-change variant you are teaching. Ensure the recurrence, table, activity, and quiz all match that variant. Do not use external sources.

## Required Output Format

Use the following format:
1. Lesson title and target audience
2. Learning objectives
3. Prerequisites
4. 50-minute timeline table
5. Concept explanation with a small worked example
6. Board / slide outline
7. In-class activity
8. Common misconceptions and instructor responses
9. Exit quiz with answers
10. Optional homework prompt

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Defines clear learning objectives focused on dynamic programming, subproblems, recurrence, bottom-up table construction, and greedy-vs-DP distinction.
2. Identifies prerequisites consistent with the prompt: arrays, loops, and recursion.
3. States the coin change variant clearly, such as minimum coins or number of ways.
4. Explains when dynamic programming is appropriate using optimal substructure and overlapping subproblems.
5. Defines subproblems correctly for the chosen coin change variant.
6. Provides a recurrence that matches the chosen variant and handles base cases correctly.
7. Includes a small worked example with internally consistent calculations and table values.
8. Shows how to build the bottom-up table step by step, not just the final answer.
9. Explains why greedy can fail or be insufficient for some coin systems using a concrete example.
10. Provides a 50-minute timeline table whose durations sum to exactly 50 minutes.
11. Includes active learning or in-class activity rather than only lecture.
12. Provides a board or slide outline aligned with the lesson sequence.
13. Includes common misconceptions and concrete instructor responses.
14. Includes an exit quiz with correct answers aligned to the learning objectives.
15. Includes an optional homework prompt that reinforces DP formulation or implementation.
16. Uses language and pacing appropriate for introductory undergraduate CS students.
17. Avoids incorrect recurrences, inconsistent examples, unsupported external claims, or conflation of greedy and DP.
18. Follows all ten required output sections.

### Task Type

Educational design; external evidence is prohibited.

### Must Have

- Target undergraduate CS students who know arrays, loops, and recursion.
- Use the coin change problem as the central worked example.
- State the problem variant clearly, preferably minimum number of coins, because the lesson emphasizes greedy-vs-DP confusion.
- Explain when dynamic programming is appropriate: optimal substructure and overlapping subproblems.
- Define subproblems and a recurrence consistent with the chosen variant.
- Show bottom-up table construction with a small internally consistent worked example.
- Explain why greedy can fail for some coin systems, such as coins [1,3,4] and amount 6 where greedy gives 4+1+1 but optimal is 3+3.
- Provide a realistic 50-minute timeline that includes active learning.
- Include common misconceptions with concrete instructor responses.
- Include an exit quiz with correct answers aligned to the objectives.

### Must Not Have

- Do not confuse the minimum-coin recurrence with the number-of-ways recurrence without explaining the chosen variant.
- Do not claim greedy always fails or that DP is always necessary.
- Do not provide a table or recurrence with inconsistent values.
- Do not cite curriculum standards or external sources.

### Quantitative Checks

- Timeline must total 50 minutes.
- Worked example table values must match the stated recurrence and coin set.
- If using the [1,3,4], amount 6 example for min coins, optimal answer is 2 coins: 3+3, while greedy uses 3 coins: 4+1+1.

### Acceptable Variations

- The lesson may use minimum coins or number of ways if the variant is explicit and the recurrence matches it; however, the greedy failure explanation is expected for minimum coins.
- The timeline may have slight formatting differences, but the durations must sum to 50 minutes and include student activity.
- Pseudocode is optional but helpful if aligned with the recurrence.

### Critical Fail Conditions

- The recurrence is wrong or does not match the stated coin change variant.
- No worked example is included.
- The lesson does not address greedy-vs-DP confusion.
- The timeline is missing or not 50 minutes.

## Required Evidence

No external evidence is allowed. The lesson should be constructed from the prompt and standard CS reasoning. Calculations in the worked example must be internally consistent. The chosen coin change variant must be explicit, and the recurrence, table, activity, quiz answers, and misconceptions must align with that variant.

## Scoring Rubric

- **Scoring Method:** Score each evaluation criterion independently: 1 = fully satisfied, 0.5 = partially satisfied or present but underspecified, 0 = absent, incorrect, contradicted, or unsupported. Sum weighted criteria, then apply any hard-fail caps and hallucination penalties.
- **Score Bands:**
  - **Excellent:** 90-100% after caps: satisfies nearly all criteria, respects all hard constraints, and is specific enough to be used as a reference answer.
  - **Good:** 75-89% after caps: mostly correct and complete, with only minor omissions or weak specificity.
  - **Acceptable:** 60-74% after caps: covers the main task but has notable gaps, weak thresholds, weak evidence, or limited actionability.
  - **Poor:** 40-59% after caps: substantial omissions, vague reasoning, missing required sections, or multiple unsupported claims.
  - **Fail:** Below 40% after caps, or any critical contradiction/fabrication that makes the answer unusable.
- **Accuracy:** Judge whether the dynamic programming concept, coin change recurrence, base cases, bottom-up table, and greedy-failure explanation are mathematically and pedagogically correct.
- **Completeness:** Judge whether all lesson-plan sections, 50-minute timeline, worked example, activity, misconceptions, quiz answers, and homework prompt are included.
- **Helpfulness:** Reward answers that are concrete, decision-oriented, prioritized, and directly usable by the stated audience. Penalize generic advice that could apply to any scenario.
- **Grounding And Evidence:** For tool-required tasks, every factual product, paper, pricing, policy, benchmark, or empirical claim must be tied to a credible public source. For tool-prohibited tasks, answers must not cite external sources or invent outside facts; they should reason only from the prompt and standard conceptual knowledge.
- **Hallucination Penalty:** Penalize incorrect table values, unsupported curriculum claims, conflating minimum-coin and number-of-ways variants, or saying greedy is always wrong/DP is always required.
- **Hard Fail Rules:**
  - Cap score at 50% if the recurrence is incorrect or inconsistent with the chosen variant.
  - Cap score at 60% if no worked example is included.
  - Cap score at 70% if the timeline does not sum to 50 minutes.
  - Cap score at 70% if greedy-vs-DP confusion is not directly addressed.
  - Cap score at 70% if the exit quiz lacks answers.

## Expected Failure Risks

- Providing only a generic lesson plan without a worked coin change example.
- Confusing greedy and dynamic programming strategies.
- Writing a recurrence that does not match the stated problem variant.
- Omitting assessment or active learning.
- Creating a timeline that does not total 50 minutes.
- Giving quiz questions without correct answers.
- Using an inconsistent DP table or base case.

## Notes

This task should be graded on conceptual correctness and teachability. A polished lesson with a wrong recurrence should score poorly.
