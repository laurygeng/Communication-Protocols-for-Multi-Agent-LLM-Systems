# Task: TA-02

## Metadata

- Task ID: TA-02
- Category: Technical Analysis
- Difficulty: Easy
- Author: Zhiqi Hu
- Tool Requirement: Prohibited

## Prompt

Explain the difference between BM25 keyword search and dense embedding semantic search for an internal FAQ search system.

Compare them in terms of matching behavior, handling of synonyms, exact phrase or identifier lookup, data and infrastructure needs, latency, and common failure modes. Then recommend whether the FAQ system should use BM25, dense embeddings, or a hybrid approach for a small company with 500 FAQ documents.

Do not use external sources or cite vendors. Do not invent measured performance numbers.

## Required Output Format

Use the following format:
1. Short definition of BM25 keyword search
2. Short definition of dense embedding semantic search
3. Comparison table
4. Recommendation paragraph
5. Two likely failure risks and mitigations

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Correctly explains BM25 as a lexical keyword-matching method based on term frequency, inverse document frequency, document-length normalization, or relevance scoring.
2. Correctly explains dense embedding search as vector-based semantic retrieval using learned representations and similarity search.
3. Contrasts lexical matching with semantic matching in plain, accurate terms.
4. Explains that BM25 handles exact words, rare terms, phrases, identifiers, product codes, and error IDs better than dense search in many FAQ settings.
5. Explains that dense embeddings can retrieve paraphrases and synonyms even when exact keywords differ.
6. Notes that dense embeddings can miss or blur exact identifiers, numbers, rare proper nouns, or negation-sensitive distinctions.
7. Compares data and infrastructure needs, including indexes, embedding generation, vector storage/search, and update workflows.
8. Compares latency and operational complexity without inventing unsupported numeric benchmarks.
9. Includes common BM25 failure modes such as vocabulary mismatch, synonym mismatch, and keyword stuffing/noisy matches.
10. Includes common dense-search failure modes such as semantic false positives, stale embeddings, poor exact lookup, and threshold tuning issues.
11. Provides a justified recommendation tied directly to the small-company, 500-document FAQ scenario.
12. Recommends BM25-first or hybrid in a nuanced way, rather than claiming one method is universally superior.
13. Includes at least two likely failure risks with practical mitigations.
14. Follows the required five-section output format including a comparison table.
15. Does not use external citations, vendor claims, invented performance numbers, or unsupported product-specific assertions.

### Task Type

Conceptual technical comparison; external evidence is prohibited.

### Must Have

- BM25 must be described as lexical keyword search using term frequency, inverse document frequency, and document-length normalization or equivalent relevance scoring.
- Dense embedding search must be described as semantic/vector retrieval using learned representations and similarity search.
- BM25 should be strong for exact words, phrases, error codes, product IDs, rare terms, and transparent keyword matching.
- Dense embeddings should be strong for synonyms, paraphrases, and conceptually similar questions, but weaker for exact identifiers unless combined with lexical search or metadata filters.
- The comparison must cover matching behavior, synonyms, exact phrase/identifier lookup, data and infrastructure needs, latency, and common failure modes.
- For a small company with 500 FAQ documents, the recommended answer should usually favor a lightweight hybrid approach or a BM25-first approach with embeddings added where semantic mismatch is common; dense-only should require strong justification.
- Include at least two realistic failure risks and practical mitigations.

### Must Not Have

- Do not cite public sources or claim to have used web search.
- Do not invent specific accuracy, latency, or cost numbers not given in the prompt.
- Do not say dense embeddings are always better than BM25.
- Do not say BM25 understands synonyms semantically unless synonyms are manually expanded or appear lexically.

### Quantitative Checks

- The scenario size is 500 FAQ documents; recommendations must be plausible for that small corpus.
- No invented benchmark percentages or milliseconds should appear unless clearly labeled as illustrative and not factual.

### Acceptable Variations

- A BM25-first recommendation is acceptable if it explains simplicity, exact lookup needs, and how to add embeddings later.
- A hybrid recommendation is acceptable if it explains the added complexity and when it is worth it for semantic matching.

### Critical Fail Conditions

- BM25 and dense embeddings are confused or reversed.
- The recommendation ignores the 500-document FAQ context.
- The answer relies on external sources despite the prohibited tool requirement.

## Required Evidence

No external evidence is allowed. The task must be answered using conceptual knowledge and reasoning from the prompt. Do not cite public sources, vendors, benchmark numbers, pricing, or web search. Any numeric examples must be clearly illustrative rather than claimed as measured performance.

## Scoring Rubric

- **Scoring Method:** Score each evaluation criterion independently: 1 = fully satisfied, 0.5 = partially satisfied or present but underspecified, 0 = absent, incorrect, contradicted, or unsupported. Sum weighted criteria, then apply any hard-fail caps and hallucination penalties.
- **Score Bands:**
  - **Excellent:** 90-100% after caps: satisfies nearly all criteria, respects all hard constraints, and is specific enough to be used as a reference answer.
  - **Good:** 75-89% after caps: mostly correct and complete, with only minor omissions or weak specificity.
  - **Acceptable:** 60-74% after caps: covers the main task but has notable gaps, weak thresholds, weak evidence, or limited actionability.
  - **Poor:** 40-59% after caps: substantial omissions, vague reasoning, missing required sections, or multiple unsupported claims.
  - **Fail:** Below 40% after caps, or any critical contradiction/fabrication that makes the answer unusable.
- **Accuracy:** Judge whether BM25 and dense embedding search are correctly distinguished and whether their strengths, weaknesses, and failure modes are technically accurate.
- **Completeness:** Judge whether all required comparison dimensions, recommendation, risks, mitigations, and required sections are included.
- **Helpfulness:** Reward answers that are concrete, decision-oriented, prioritized, and directly usable by the stated audience. Penalize generic advice that could apply to any scenario.
- **Grounding And Evidence:** For tool-required tasks, every factual product, paper, pricing, policy, benchmark, or empirical claim must be tied to a credible public source. For tool-prohibited tasks, answers must not cite external sources or invent outside facts; they should reason only from the prompt and standard conceptual knowledge.
- **Hallucination Penalty:** Penalize invented performance numbers, unsupported claims about specific products, claims that dense search is always better, or claims that BM25 semantically understands synonyms by itself.
- **Hard Fail Rules:**
  - Cap score at 50% if BM25 and dense search are materially confused or reversed.
  - Cap score at 70% if no recommendation is tied to the 500-document scenario.
  - Cap score at 70% if the comparison table omits two or more required dimensions.
  - Cap score at 60% if external citations or vendor claims are used despite the prohibited evidence requirement.

## Expected Failure Risks

- Overstating dense embeddings as always better.
- Ignoring exact-match use cases such as product codes or error IDs.
- Giving a recommendation without linking it to the 500-document FAQ context.
- Failing to mention operational complexity for embeddings and vector search.
- Inventing latency or accuracy numbers.
- Using external citations despite the no-evidence requirement.

## Notes

This task is easy, but it should still be graded for precision. Dense-only answers should not receive high scores unless they address exact lookup risks and small-corpus simplicity.
