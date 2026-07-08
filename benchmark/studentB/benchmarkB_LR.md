# Task: LR-02

## Metadata

- Task ID: LR-02
- Category: Literature Review
- Difficulty: Medium
- Author: Zhiqi Hu
- Tool Requirement: Required

## Prompt

Write a concise literature review on retrieval-augmented generation (RAG) for reducing hallucinations in domain-specific question answering systems.

Your review should compare at least three methodological families, such as retrieval/indexing improvements, reranking or context selection, citation-grounded generation, answer verification, or evaluation/guardrail methods. Focus on how these methods affect factuality, evidence grounding, latency, and implementation complexity.

Use public scholarly sources. Include at least four sources published in or after 2020, and clearly separate established findings from open research gaps. End with three research gaps or future directions that would be useful for a team building a RAG-based QA assistant.

## Required Output Format

Use the following format:
1. Title
2. One-paragraph executive summary
3. Source table with columns: Source, Year, Method / Focus, Key Contribution, Limitation
4. Literature review organized by method family
5. Tradeoff analysis covering factuality, grounding, latency, and implementation complexity
6. Research gaps / future directions
7. Short conclusion

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Accurately defines RAG and explains why hallucination reduction matters in domain-specific QA.
2. Compares at least three relevant methodological families rather than summarizing only one technique.
3. Uses at least four credible public scholarly sources from 2020 or later and identifies each source's contribution.
4. Analyzes tradeoffs among factuality, evidence grounding, latency, and implementation complexity.
5. Identifies at least three realistic research gaps or future directions supported by the review.
6. Clearly distinguishes sourced claims from the author's synthesis and avoids overstating results.

## Required Evidence

External evidence is required. The answer must cite at least four credible public scholarly sources, preferably peer-reviewed papers, arXiv papers, or conference/workshop papers from 2020 onward. Claims about benchmark performance, model capabilities, or empirical findings must be tied to a cited source. A source table is required.

## Scoring Rubric

- Accuracy: Judge whether the descriptions of RAG methods, hallucination risks, and tradeoffs are technically correct and source-supported.
- Completeness: Judge whether all required sections are present and all evaluation criteria are covered.
- Helpfulness: Judge whether the review gives a clear, useful synthesis for a team deciding what RAG improvements to explore next.
- Hallucination Penalty: Penalize fabricated papers, incorrect citations, unsupported empirical claims, or claims that a method eliminates hallucinations completely without evidence.

## Expected Failure Risks

- Listing papers without comparing methods.
- Using outdated or weak sources.
- Making unsupported benchmark or performance claims.
- Ignoring latency and implementation tradeoffs.

## Notes

This is a medium literature review task because it requires evidence gathering, comparison, and synthesis, but the scope is limited to one research theme.
