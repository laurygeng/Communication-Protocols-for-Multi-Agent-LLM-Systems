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

Do not fabricate citations, paper details, or benchmark results. If a claim is synthesis rather than a sourced finding, label it clearly.

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

1. Defines RAG accurately as retrieval plus generation conditioned on external/domain evidence.
2. Explains why hallucination reduction matters specifically for domain-specific QA, including factuality, trust, and evidence traceability.
3. Uses at least four credible public scholarly sources from 2020 or later.
4. Identifies each source's year, method/focus, contribution, and limitation in the required source table.
5. Cites sources for empirical, benchmark, capability, and limitation claims rather than making unsupported assertions.
6. Compares at least three methodological families instead of merely listing papers.
7. Covers retrieval/indexing or corpus construction improvements and explains their effect on grounding and recall.
8. Covers reranking or context selection and explains precision/latency/context-window tradeoffs.
9. Covers citation-grounded generation, answer verification, guardrails, or evaluation methods and explains how they detect or reduce unsupported answers.
10. Analyzes factuality tradeoffs with appropriate caution and without claiming perfect hallucination elimination.
11. Analyzes evidence grounding, including whether answers are tied to retrieved passages or citations.
12. Analyzes latency costs from retrieval, reranking, verification, or multi-stage pipelines.
13. Analyzes implementation complexity, including indexing, maintenance, evaluation, or model orchestration burden.
14. Clearly separates established findings from the author's synthesis, assumptions, or open gaps.
15. Provides at least three realistic research gaps or future directions useful for a RAG QA assistant team.
16. Follows the required seven-section output format.
17. Avoids fabricated papers, incorrect citations, fabricated performance numbers, and overclaimed empirical results.
18. Keeps the review concise while still giving enough detail for method comparison and decision-making.

### Task Type

Evidence-based literature review; external public scholarly evidence is mandatory.

### Must Have

- Define RAG as combining retrieval of external/domain-specific evidence with generation conditioned on that evidence.
- Explain hallucination reduction as an improvement in factuality and evidence grounding, not as a guarantee that hallucinations disappear.
- Use at least four credible public scholarly sources published in or after 2020; each source must be identifiable and cited where used.
- Compare at least three methodological families, such as retrieval/indexing, reranking/context selection, citation-grounded generation, answer verification, and evaluation/guardrails.
- Discuss factuality, evidence grounding, latency, and implementation complexity for each major family or in a dedicated tradeoff section.
- Separate established findings from open research gaps or future directions.
- End with at least three realistic research gaps or future directions for a team building a RAG QA assistant.

### Must Not Have

- Do not fabricate paper titles, authors, venues, years, DOIs, or benchmark numbers.
- Do not claim that RAG, citations, reranking, or verification eliminates hallucinations completely.
- Do not rely mainly on blogs, vendor marketing pages, or uncited general claims when the prompt asks for scholarly sources.
- Do not present source claims and the author's synthesis as if they have the same evidentiary status.

### Source Requirements

- **Minimum Sources:** 4
- **Source Type:** Public scholarly sources such as peer-reviewed papers, arXiv papers, conference/workshop papers, or scholarly surveys.
- **Date Requirement:** At least four sources must be from 2020 or later.
- **Citation Requirement:** Claims about empirical findings, benchmark behavior, method capabilities, or limitations must be cited inline or in a clear source table.

### Acceptable Variations

- The exact set of papers may vary if they are credible and relevant.
- The review may group methods differently, but at least three distinct method families must be compared.
- A concise review is acceptable, but it must still include the required table and tradeoff analysis.

### Critical Fail Conditions

- No external scholarly sources are cited.
- Fewer than four post-2020 scholarly sources are used.
- The answer fabricates citations or unsupported benchmark results.
- The answer covers only generic RAG benefits without comparing method families.

## Required Evidence

External evidence is required. The answer must cite at least four credible public scholarly sources published in or after 2020. Acceptable sources include peer-reviewed papers, arXiv papers, conference/workshop papers, or scholarly surveys. Claims about benchmark performance, empirical findings, model capabilities, or limitations must be tied to specific cited sources. The source table is mandatory. If a factual claim cannot be verified from the cited sources, it must be labeled as synthesis, assumption, or open question rather than presented as established fact.

## Scoring Rubric

- **Scoring Method:** Score each evaluation criterion independently: 1 = fully satisfied, 0.5 = partially satisfied or present but underspecified, 0 = absent, incorrect, contradicted, or unsupported. Sum weighted criteria, then apply any hard-fail caps and hallucination penalties.
- **Score Bands:**
  - **Excellent:** 90-100% after caps: satisfies nearly all criteria, respects all hard constraints, and is specific enough to be used as a reference answer.
  - **Good:** 75-89% after caps: mostly correct and complete, with only minor omissions or weak specificity.
  - **Acceptable:** 60-74% after caps: covers the main task but has notable gaps, weak thresholds, weak evidence, or limited actionability.
  - **Poor:** 40-59% after caps: substantial omissions, vague reasoning, missing required sections, or multiple unsupported claims.
  - **Fail:** Below 40% after caps, or any critical contradiction/fabrication that makes the answer unusable.
- **Accuracy:** Judge whether RAG, retrieval, reranking/context selection, citation grounding, verification, evaluation, and hallucination risks are technically described correctly and supported by cited scholarly evidence.
- **Completeness:** Judge whether all required sections, source table fields, at least three method families, four tradeoff dimensions, and three research gaps are present.
- **Helpfulness:** Reward answers that are concrete, decision-oriented, prioritized, and directly usable by the stated audience. Penalize generic advice that could apply to any scenario.
- **Grounding And Evidence:** For tool-required tasks, every factual product, paper, pricing, policy, benchmark, or empirical claim must be tied to a credible public source. For tool-prohibited tasks, answers must not cite external sources or invent outside facts; they should reason only from the prompt and standard conceptual knowledge.
- **Hallucination Penalty:** Apply severe penalties for fabricated citations, incorrect paper details, unsupported benchmark numbers, or claims that any method eliminates hallucinations. A fabricated citation should normally cap the score at 40% even if the prose is otherwise plausible.
- **Hard Fail Rules:**
  - Cap score at 50% if fewer than four credible post-2020 scholarly sources are used.
  - Cap score at 60% if the answer does not compare at least three methodological families.
  - Cap score at 40% if citations are mostly fabricated, unverifiable, or unrelated.
  - Cap score at 70% if the required source table is missing even when sources are cited.

## Expected Failure Risks

- Listing papers without comparing methodological families.
- Using outdated, weak, or non-scholarly sources to satisfy a scholarly-source requirement.
- Making unsupported benchmark or performance claims.
- Ignoring latency and implementation tradeoffs.
- Conflating retrieval quality with generation correctness.
- Treating citations as proof even when the cited passage does not support the generated answer.
- Failing to distinguish established findings from open research gaps.
- Claiming that RAG eliminates hallucination rather than reducing risk.

## Notes

This task should be graded strictly for source grounding. A polished but weakly cited review should not receive a high score.
