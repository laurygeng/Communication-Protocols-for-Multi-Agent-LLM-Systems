# Task: LR-03

## Metadata
- **Task ID:** LR-03
- **Category:** Literature Review (Paper Extraction & Synthesis)
- **Difficulty:** Medium
- **Author:** Minjie Geng
- **Tool Requirement:** Required 

## Prompt
Select exactly three highly cited or recent academic papers on the topic of Parameter-Efficient Fine-Tuning (PEFT) for Large Language Models (e.g., LoRA, Prefix-Tuning, Adapters).

1. Provide a brief 1–2 paragraph introduction summarizing why PEFT is necessary for modern LLMs.
2. Extract the core contributions of each paper and present them in a single, comprehensive comparison matrix. The matrix MUST contain exactly the following columns:

- **Paper Title & Year**
- **Core Method**
- **Key Innovation**
- **Main Limitation**

3. Synthesize the information from the Main Limitation column. Based only on the flaws you extracted from these three specific papers, identify one overarching Research Gap in the current PEFT ecosystem and suggest a concrete direction for future research to solve it.

## Required Output Format
Use the following strict structure:

1. Introduction to PEFT
2. Paper Extraction Matrix
3. Synthesized Research Gap & Future Direction
4. References (including DOI or ArXiv IDs)

## Ground Truth / Evaluation Criteria
The answer should satisfy the following criteria:

- Correctly selects exactly 3 real academic papers related to PEFT.
- The comparison matrix includes exactly the 4 requested columns.
- The Core Method accurately reflects the technical implementation (e.g., for LoRA, it must mention low-rank matrix decomposition).
- The Key Innovation correctly identifies the novel contribution of that specific paper.
- The Main Limitation / Flaw is factually grounded in the paper's actual limitations or known community consensus (not a generic AI complaint).
- Synthesis Check: The identified "Research Gap" must logically connect to at least two of the flaws listed in the matrix.
- Includes a properly formatted reference list with verifiable identifiers (DOI/ArXiv).

## Scoring Rubric
- Each protocol output must be evaluated against the following multi-dimensional criteria matrix:

1. Quality Metrics (0.0 - 1.0 Scale)

- **Accuracy:** Evaluated based on the strict factual correctness of the extracted Core Method, Key Innovation, and Main Limitation. Any technical mischaracterization drops this score linearly.
- **Completeness:** Measures the explicit coverage of all 4 requested layout sections and the 4 required columns in the extraction matrix. Missing entries or truncated analysis directly reduces this metric.
- **Helpfulness:** Assesses whether the synthesized Research Gap is actionable and provides concrete value for future study design, rather than spinning generic academic platitudes.
- **Hallucination Rate:** Calculated precisely as:

$$
	ext{Hallucination Rate} = \frac{\text{Unsupported Factual Claims}}{\text{Total Factual Claims}}
$$

Any fictional paper title, fabricated author name, falsified publication year, or non-existent DOI/ArXiv ID will penalize this score exponentially.

- **Overall Quality Score:** A weighted aggregate of the primary quality dimensions:

$$
	ext{Overall Quality Score} = 0.4 \times \text{Accuracy} + 0.3 \times \text{Completeness} + 0.2 \times \text{Helpfulness} + 0.1 \times (1 - \text{Hallucination Rate})
$$

2. Efficiency & Resource Metrics (Log-derived)

- **Runtime:** Total wall-clock execution time (seconds) taken by the multi-agent system to complete the search, parsing, and synthesis tasks.
- **Cost:** Tracked via total input/output token usage or estimated API financial expenditure across all participating agents.
- **Tool Usage:** Absolute count of external tool calls (specifically Search and Document Retriever APIs). Since `Tool Requirement: Required` is specified, a Tool Usage = 0 indicates failure, whereas excessive redundant calls reflect poor routing optimization.

3. Multi-Agent Communication & Consensus Metrics

- **Message Count:** Total number of discrete inter-agent messages exchanged during the literature review drafting, peer-reviewing, and synthesis phases.
- **Communication Density:** Calculated as $\frac{\text{Total Messages}}{\text{Number of Active Agents}}$. High density without an equivalent jump in Quality Score penalizes coordination efficiency.
- **Agreement Rate:** Binary or fractional metric checking whether the Researcher Agent, Reviewer Agent, and Judge Agent successfully reached a formal consensus on the final extracted flaws and reference list validity.
- **Critique Acceptance Rate:** Calculated as:

$$
	ext{Critique Acceptance Rate} = \frac{\text{Accepted Critiques}}{\text{Total Critiques Raised}}
$$

Measures the collaborative efficiency between the Reviewer Agent's feedback and the Researcher Agent's subsequent revisions of the paper matrix.

4. ROI / Optimization Metrics

- **Quality-Cost Ratio:** The ultimate optimization frontier for protocol comparison:

$$
	ext{Quality-Cost Ratio} = \frac{\text{Overall Quality Score}}{\text{Total Token / API Cost}}
$$

## Expected Failure Risks
- The AI summarizes the abstract instead of actively extracting the specific innovation and flaw.
- The AI hallucinates a flaw that doesn't exist in the paper just to make the final "Research Gap" synthesis easier to write.
- The final Research Gap is completely disconnected from the table (e.g., the table discusses memory issues, but the gap talks about ethical bias).
- The AI fails to provide verifiable DOI or ArXiv IDs for the papers.
