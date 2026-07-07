# Task: LR-04
## Metadata
- Task ID: LR-04
- Category: Literature Review
- Difficulty: Medium
- Author: Haofan Hou
- Tool Requirement: Required
## Prompt

Write a short literature review on communication methods in multi-agent LLM systems.

First, briefly summarize the purpose of communication in multi-agent LLM systems and the main research problems addressed in this field.

Then, review and compare the following three categories of communication methods:

1. Direct or message-passing communication
2. Shared-workspace communication, such as shared memory or blackboard systems
3. Discussion-based communication, such as group discussion, debate, or iterative critique

For the purpose of this review, treat these as high-level communication patterns. A real multi-agent system may combine more than one pattern.

For each category, describe its general approach, provide at least one example from the literature, and summarize its main strengths and limitations.

Finally, identify one specific unresolved issue or research gap that is supported by limitations discussed in at least two of the reviewed sources. Briefly explain why the gap is important and what future research could investigate.
## Required Output Format
Use the following structure:

1. Field overview
2. Direct or message-passing communication
3. Shared-workspace communication
4. Discussion-based communication
5. Comparison table
6. Research gap and future research direction
7. Conclusion
8. References

The comparison table must include:

| Method Category | General Approach | Literature Example | Main Strength | Main Limitation |

The response should be approximately 500-800 words.
## Ground Truth / Evaluation Criteria
The answer should satisfy the following criteria:

1. Clearly summarizes the purpose and major research concerns of communication in multi-agent LLM systems.
2. Correctly describes all three required categories of communication methods.
3. Includes at least one relevant literature example for each category.
4. Compares the methods using their general approaches, strengths, and limitations.
5. Identifies one specific and plausible research gap.
6. Connects the research gap to limitations or unresolved issues found in the reviewed literature.
7. Suggests a reasonable future research direction related to the identified gap.
8. Uses the required structure, comparison table, in-text citations, and reference list.
## Required Evidence

The answer must cite at least three reliable sources.

At least two sources must be academic papers, conference papers, journal articles, or research preprints.

Official technical reports may be used as additional sources.

Examples, factual claims, and research limitations should be supported by appropriate citations.
## Scoring Rubric
- Accuracy: The descriptions of the research field, communication methods, and cited studies must be correct.
- Completeness: The answer must cover the field overview, all three method categories, their comparison, one research gap, and one future direction.
- Helpfulness: The review should clearly organize the literature and help the reader understand major approaches and unresolved issues.
- Hallucination Penalty: Penalize fabricated papers, incorrect citations, unsupported descriptions of research findings, or research gaps that are not connected to the reviewed literature.
## Expected Failure Risks
- Turning the literature review into a purely technical architecture analysis.
- Listing papers without synthesizing or comparing their findings.
- Confusing individual protocols with broader categories of communication methods.
- Inventing papers, authors, experimental results, or publication details.
- Presenting a vague limitation as a research gap without supporting evidence.
- Suggesting a future direction that is unrelated to the identified gap.
## Notes
The task evaluates literature summarization, method comparison, and research-gap identification. It does not require the system to design or recommend a complete communication architecture.
