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

## Required Output Format

Use the following format:
1. Short definition of BM25 keyword search
2. Short definition of dense embedding semantic search
3. Comparison table
4. Recommendation paragraph
5. Two likely failure risks and mitigations

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Correctly explains that BM25 is a lexical keyword-matching method based on term frequency and document relevance scoring.
2. Correctly explains that dense embedding search retrieves semantically similar content using vector representations.
3. Compares the required dimensions: matching behavior, synonyms, exact identifiers, infrastructure, latency, and failure modes.
4. Gives a justified recommendation for the 500-document FAQ scenario.
5. Identifies at least two realistic failure risks and practical mitigations.

## Required Evidence

No external evidence is allowed. The task should be answered using conceptual knowledge and reasoning from the prompt. Do not cite public sources or use web search.

## Scoring Rubric

- Accuracy: Judge whether BM25 and dense embedding search are explained correctly and not confused with each other.
- Completeness: Judge whether all comparison dimensions and required output sections are included.
- Helpfulness: Judge whether the recommendation is clear, practical, and tied to the small FAQ scenario.
- Hallucination Penalty: Penalize invented performance numbers, unsupported claims about specific products, or claims requiring external evidence.

## Expected Failure Risks

- Overstating dense embeddings as always better.
- Ignoring exact-match use cases such as product codes or error IDs.
- Giving a recommendation without linking it to the 500-document FAQ context.

## Notes

This is an easy technical analysis task because it has a narrow scope and an obvious comparison-and-recommendation structure.
