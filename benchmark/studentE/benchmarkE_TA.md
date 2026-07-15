# Task: TA-05

## Metadata

- Task ID: TA-05
- Title: Comparing ReAct and Reflexion for Long-Horizon Agent Tasks
- Category: Technical Analysis
- Difficulty: Medium
- Author: Student E
- Tool Requirement: Prohibited

## Prompt

Using only the two provided papers, compare ReAct and Reflexion as approaches for improving the behavior of language-model agents.

Provided papers:
1. ReAct: Synergizing Reasoning and Acting in Language Models
2. Reflexion: Language Agents with Verbal Reinforcement Learning

Explain and compare the two approaches in terms of:
- Core mechanism
- When reasoning or reflection is triggered
- Timescale of improvement
- Memory or context usage
- Use of observations, feedback, or evaluation signals
- Main strength
- Main limitation
- How the two approaches may be combined

Your analysis must clearly distinguish temporary within-attempt context or reasoning history in ReAct from persistent cross-attempt reflective memory in Reflexion.

For ReAct, explain how reasoning traces and actions are interleaved during one task attempt and how observations from the environment influence the next reasoning or action step.

For Reflexion, explain how an agent evaluates the outcome of an attempt and generates verbal feedback or reflection when improvement is needed, especially after failure or inadequate performance. Clarify that Reflexion improves later attempts through stored verbal reflections rather than by updating the language model's weights.

Then analyze a long-horizon task that may involve both many steps within one attempt and multiple attempts after failure. Recommend whether ReAct, Reflexion, or a combination of both is most suitable. Justify the recommendation with at least three technical reasons and identify one limitation or implementation risk of the recommended approach.

Include a comparison table with the columns: Dimension, ReAct, Reflexion, Relationship or Practical Impact. The table should contain at least the following rows: Core Mechanism, Trigger or Timing, Timescale, Memory Usage, Feedback Usage, Main Strength, Main Limitation, and Combination Potential.

Use only the two provided papers as the primary evidence. Do not use web search, external sources, or claims that are not supported by the papers. The response should be approximately 600-800 words.

## Required Output Format

- Type: markdown
- Required sections:
  1. ReAct Mechanism
  2. Reflexion Mechanism
  3. Comparison Table
  4. Key Distinctions
  5. How ReAct and Reflexion Can Be Combined
  6. Recommendation for a Long-Horizon Task
  7. Limitation of the Recommended Approach

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. **Requirement Coverage:** Full credit requires all seven required sections; analysis of both ReAct and Reflexion; coverage of all eight comparison dimensions; a complete comparison table using all four specified columns and at least the eight required rows; one explanation of how the methods can be combined; one clear recommendation; at least three supporting reasons; and one limitation or risk. Reduce proportionally for each missing section or required element.
2. **React Technical Accuracy:** Full credit requires a technically correct explanation that ReAct interleaves language-model reasoning traces with actions and environment observations during a task attempt. The answer should explain that observations influence subsequent reasoning and actions and that the reasoning history is typically maintained in temporary within-attempt context or a scratchpad. It must not claim that ReAct inherently performs model-weight updates, automatically creates persistent cross-attempt memory, or requires a separate long-term memory module.
3. **Reflexion Technical Accuracy:** Full credit requires a technically correct explanation that Reflexion uses outcome signals, evaluator feedback, or task results to generate verbal reflections that can guide later attempts. The response must distinguish this cross-attempt reflective memory from ordinary within-attempt reasoning and clarify that the method does not improve behavior by updating the base model's weights. It should not imply that reflection is necessarily generated after every successful attempt or that Reflexion is simply a longer chain of thought.
4. **Comparison And Distinction Quality:** Full credit requires a direct and technically meaningful comparison of core mechanism, trigger or timing, timescale, memory usage, feedback usage, strengths, limitations, and combination potential. The answer must clearly distinguish improvement within one attempt from improvement across multiple attempts. The table and prose should explain practical consequences rather than merely repeat definitions.
5. **Complementarity And Combination Reasoning:** Full credit requires a plausible explanation of how Reflexion can use a ReAct-style actor or how ReAct can manage step-by-step interaction within an attempt while Reflexion stores higher-level lessons for later attempts. The response should explain the division of roles and information flow between the two mechanisms. Simply stating that they can be combined without describing how receives little or no credit.
6. **Recommendation And Limitation Analysis:** Full credit requires one clear recommendation for a task involving both many within-attempt steps and possible repeated attempts. The recommendation must be supported by at least three technical reasons tied to execution, feedback, memory, or error recovery and must identify one realistic limitation or implementation risk, such as poor-quality reflections, context growth, memory contamination, evaluator errors, added cost, or repeated propagation of incorrect lessons. A recommendation based only on general preference receives no more than half credit.
7. **Clarity And Evidence Integrity:** Full credit requires clear organization, consistent terminology, readable Markdown, the required table, and approximately 600-800 words. Claims should be traceable to the two provided papers. Deduct for fabricated experimental results, unsupported numerical comparisons, external citations, confusion between thought and reflection, or claims that either approach guarantees success.

## Required Evidence

Use only the provided local input files as the primary evidence. Do not use web search or external sources.

## Input Files

- `react.pdf`
- `reflexion.pdf`

## Scoring Rubric

- **Requirement Coverage (0.15):** Full credit requires all seven required sections; analysis of both ReAct and Reflexion; coverage of all eight comparison dimensions; a complete comparison table using all four specified columns and at least the eight required rows; one explanation of how the methods can be combined; one clear recommendation; at least three supporting reasons; and one limitation or risk. Reduce proportionally for each missing section or required element.
- **React Technical Accuracy (0.15):** Full credit requires a technically correct explanation that ReAct interleaves language-model reasoning traces with actions and environment observations during a task attempt. The answer should explain that observations influence subsequent reasoning and actions and that the reasoning history is typically maintained in temporary within-attempt context or a scratchpad. It must not claim that ReAct inherently performs model-weight updates, automatically creates persistent cross-attempt memory, or requires a separate long-term memory module.
- **Reflexion Technical Accuracy (0.15):** Full credit requires a technically correct explanation that Reflexion uses outcome signals, evaluator feedback, or task results to generate verbal reflections that can guide later attempts. The response must distinguish this cross-attempt reflective memory from ordinary within-attempt reasoning and clarify that the method does not improve behavior by updating the base model's weights. It should not imply that reflection is necessarily generated after every successful attempt or that Reflexion is simply a longer chain of thought.
- **Comparison And Distinction Quality (0.20):** Full credit requires a direct and technically meaningful comparison of core mechanism, trigger or timing, timescale, memory usage, feedback usage, strengths, limitations, and combination potential. The answer must clearly distinguish improvement within one attempt from improvement across multiple attempts. The table and prose should explain practical consequences rather than merely repeat definitions.
- **Complementarity And Combination Reasoning (0.10):** Full credit requires a plausible explanation of how Reflexion can use a ReAct-style actor or how ReAct can manage step-by-step interaction within an attempt while Reflexion stores higher-level lessons for later attempts. The response should explain the division of roles and information flow between the two mechanisms. Simply stating that they can be combined without describing how receives little or no credit.
- **Recommendation And Limitation Analysis (0.20):** Full credit requires one clear recommendation for a task involving both many within-attempt steps and possible repeated attempts. The recommendation must be supported by at least three technical reasons tied to execution, feedback, memory, or error recovery and must identify one realistic limitation or implementation risk, such as poor-quality reflections, context growth, memory contamination, evaluator errors, added cost, or repeated propagation of incorrect lessons. A recommendation based only on general preference receives no more than half credit.
- **Clarity And Evidence Integrity (0.05):** Full credit requires clear organization, consistent terminology, readable Markdown, the required table, and approximately 600-800 words. Claims should be traceable to the two provided papers. Deduct for fabricated experimental results, unsupported numerical comparisons, external citations, confusion between thought and reflection, or claims that either approach guarantees success.

## Expected Failure Risks

- Confusing ReAct's within-attempt reasoning history with persistent cross-attempt memory.
- Claiming Reflexion updates the language model's weights.
- Treating Reflexion as merely a longer chain of thought.
- Saying ReAct and Reflexion can be combined without explaining the information flow.
- Using claims or evidence outside the two provided papers.

## Notes

