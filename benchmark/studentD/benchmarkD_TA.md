
# Task: TA-04

## Metadata

- Task ID: TA-04
- Category: Technical Analysis
- Difficulty: Medium
- Author: Haofan Hou
- Tool Requirement: Prohibited

## Prompt

A system must answer questions based on a collection of long technical documents. The documents may exceed the language model's context-window limit.

Analyze and compare the following three technical approaches:

1. Full-context prompting: place as much document content as possible directly into the model prompt.
2. Retrieval-augmented generation: divide documents into chunks, retrieve relevant chunks for each question, and provide them to the model.
3. Hierarchical summarization: summarize document sections first, combine the section summaries into higher-level summaries, and use the summaries to answer questions.

Compare the three approaches in terms of:

- Information coverage
- Answer accuracy and grounding
- Context-window usage
- Computational cost
- Implementation complexity
- Main failure risks

Then recommend the most suitable approach for a system that must answer detailed questions about a large collection of technical manuals. Justify the recommendation and identify one situation in which the recommended approach may perform poorly.
Use qualitative technical reasoning. Do not invent numerical performance results.

## Required Output Format

Use the following structure:

1. Brief explanation of full-context prompting
2. Brief explanation of retrieval-augmented generation
3. Brief explanation of hierarchical summarization
4. Comparison table
5. Final recommendation
6. Limitation of the recommended approach

The comparison table must use the following columns:

| Approach | Information Coverage | Grounding | Context Usage | Cost | Implementation Complexity | Main Failure Risk |

The response should be approximately 500–700 words.

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Correctly explains that full-context prompting places document content directly into the model context and is limited by the available context window.
2. Correctly explains that retrieval-augmented generation retrieves selected document chunks that are relevant to the question.
3. Correctly explains that hierarchical summarization progressively compresses information from sections into higher-level summaries.
4. Compares all three approaches across the six required dimensions.
5. Recognizes that full-context prompting may omit content or become costly when documents are very long.
6. Recognizes that retrieval-augmented generation depends on retrieval and chunking quality and may miss relevant information.
7. Recognizes that hierarchical summarization may lose important details during repeated compression.
8. Gives a justified recommendation for the technical-manual question-answering scenario.
9. Identifies one realistic situation in which the recommended approach may perform poorly.
10. Follows the required structure and comparison-table format.

## Required Evidence

No external citations are required.

The task is conceptual and should be answered using technical reasoning based on the three approaches described in the prompt.

The answer may use brief hypothetical examples, but it must not claim specific measured improvements in accuracy, latency, token usage, or cost unless those values are explicitly presented as illustrative assumptions.

## Scoring Rubric

- Accuracy: The three approaches, their mechanisms, and their typical failure risks must be explained correctly.
- Completeness: The answer must cover all three approaches, all six comparison dimensions, a recommendation, and one limitation.
- Helpfulness: The comparison should clearly support a practical architecture decision for the stated scenario.
- Hallucination Penalty: Penalize fabricated benchmark results, unsupported numerical performance claims, or references to experiments not provided in the prompt.

## Expected Failure Risks

- Confusing retrieval-augmented generation with document summarization.
- Claiming that retrieval always finds every relevant passage.
- Ignoring information loss in hierarchical summarization.
- Recommending an approach without connecting it to the technical-manual scenario.
- Discussing only advantages while omitting tradeoffs and failure risks.
- Inventing numerical accuracy, latency, token, or cost results.

## Notes

The task evaluates technical explanation, architecture comparison, tradeoff analysis, and design recommendation.

The task does not prescribe how many agents are used, what roles they have, or how they communicate. Every experimental protocol must receive the same prompt and tool restrictions.

