# Task: LR-05

## Metadata

- Task ID: LR-05
- Title: Comparative Literature Review and Ranking of Seven Agent-System Papers
- Category: Literature Review
- Difficulty: Hard
- Author: Student E
- Tool Requirement: Required

## Prompt

Using the seven provided papers and current online citation data, write a comparative literature review of the following works:

1. ReAct: Synergizing Reasoning and Acting in Language Models
2. Reflexion: Language Agents with Verbal Reinforcement Learning
3. Toolformer: Language Models Can Teach Themselves to Use Tools
4. Voyager: An Open-Ended Embodied Agent with Large Language Models
5. AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation
6. CAMEL: Communicative Agents for Mind Exploration of Large Scale Language Model Society
7. MetaGPT: Meta Programming for Multi-Agent Collaborative Framework

Use the provided local PDFs as the primary sources for each paper's research problem, mechanism, contribution, evaluation, strengths, limitations, and cross-paper relationships.

For each paper, summarize the main research problem, core mechanism or system design, principal contribution, evaluation setting, one important strength, and one important limitation. The review must synthesize the papers rather than present seven isolated summaries.

Then analyze relationships among the papers. Use the following relationship types where appropriate:
- Direct extension
- Mechanism reuse or methodological adoption
- Framework inclusion or integration
- Conceptual similarity or complementary direction
- No clear direct dependency

Do not describe one paper as directly building on another unless the provided papers support a direct methodological dependency or explicit extension. A citation in related work alone is not sufficient evidence of direct influence.

Identify one specific unresolved research gap supported by limitations or open problems from at least two of the seven papers. Explain why the gap matters, why the reviewed papers do not fully solve it, and propose one feasible future research direction.

Rank all seven papers from strongest to weakest using the following four criteria:
- Novelty: originality of the paper's central contribution at the time of publication
- Generality: applicability beyond a narrow task, environment, or system configuration
- Empirical Rigor: strength, breadth, and appropriateness of the evaluation evidence presented in the paper
- Scholarly Influence: current external citation impact plus evidence of methodological adoption or extension

For Scholarly Influence, retrieve current citation data for all seven papers from Semantic Scholar using one common retrieval date. For each paper, report the total citation count, publication year, and citations per year, calculated as total citations divided by the number of years since publication. Use a minimum denominator of 1 year for papers published less than one year before the retrieval date. Use the canonical record that matches the paper title and authors. Do not mix citation counts from different platforms. If Semantic Scholar is unavailable for any paper, use OpenAlex for all seven papers and clearly state the substitution.

Evaluate Scholarly Influence using three factors:
- Total citation count
- Citations per year
- Evidence from the reviewed papers or other reliable academic sources that later work directly adopted, extended, or integrated the paper's method

Citation count alone must not determine the influence score. Distinguish broad citation visibility from direct methodological influence, and acknowledge that citation counts change over time and may disadvantage newer papers.

Score every paper from 1 to 5 on each criterion. Use equal weights of 25% per criterion unless you explicitly propose different weights before scoring and justify them. Calculate a weighted score for each paper and use the scores to produce an overall ranking. If the final ordering differs from the numerical weighted scores, explain every deviation.

Also discuss at least two meaningful conflicts among the criteria, such as a paper being highly novel but less general, or highly cited but empirically narrow. The ranking must be comparative and evidence-based; there is no required predetermined winner.

Include the following tables:
1. Seven-Paper Summary Table with columns: Paper, Research Problem, Core Mechanism, Main Contribution, Evaluation Setting, Strength, Limitation.
2. Cross-Paper Relationship Table with columns: Source Paper, Related Paper, Relationship Type, Evidence or Rationale.
3. Citation Data Table with columns: Paper, Publication Year, Total Citations, Citations per Year, Citation Source, Retrieval Date.
4. Four-Criterion Scoring Matrix with columns: Paper, Novelty, Generality, Empirical Rigor, Scholarly Influence, Weighted Score.
5. Overall Ranking Table with columns: Rank, Paper, Weighted Score, Main Reason for Position.

Use in-text citations for claims derived from the provided papers and online sources. Include all seven papers and the citation-data source in the References section. The response should be approximately 1,600-2,000 words.

## Required Output Format

- Type: markdown
- Required sections:
  1. Scope, Sources, and Ranking Method
  2. Seven-Paper Summary Table
  3. Comparative Synthesis
  4. Cross-Paper Relationship Analysis
  5. Research Gap and Future Research Direction
  6. Citation Data Table
  7. Four-Criterion Scoring Matrix
  8. Overall Ranking
  9. Criterion-Conflict and Citation-Limitation Analysis
  10. Conclusion
  11. References

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. **Requirement Coverage:** Full credit requires all eleven required sections; coverage of all seven papers; all five required tables with the specified columns; one research gap supported by at least two papers; one future direction; citation data for all seven papers; scores for all seven papers on all four criteria; a weighted score and complete ranking; at least two criterion conflicts; and a References section containing all seven papers plus the citation-data source.
2. **Seven Paper Summary Accuracy:** Full credit requires technically accurate descriptions of the research problem, mechanism or system design, contribution, evaluation setting, strength, and limitation for each paper. Each paper contributes approximately one seventh of this criterion. Major mechanism attribution errors, invented experiments, or assigning one paper's contribution to another receive little or no credit for the affected paper.
3. **Cross Paper Relationship Accuracy:** Full credit requires careful use of the allowed relationship types and evidence-based distinctions among direct extension, mechanism reuse, framework integration, conceptual similarity, and no clear dependency. A related-work citation alone must not be treated as direct methodological influence.
4. **Research Gap Quality:** Full credit requires one specific and nontrivial unresolved gap supported by limitations or open problems from at least two reviewed papers; an explanation of why the gap matters; evidence that the seven papers do not already fully solve it; and one feasible future research direction that directly addresses it.
5. **Citation Data Accuracy And Consistency:** Full credit requires current citation counts for all seven papers from one consistent platform, a common retrieval date, correct publication years, and correct citations-per-year calculations. The answer must use canonical records matching title and authors, must not mix platforms, and must clearly document any switch from Semantic Scholar to OpenAlex. Missing, duplicated, mismatched, or fabricated records substantially reduce this score.
6. **Scholarly Influence Reasoning:** Full credit requires influence judgments that combine total citations, citations per year, and evidence of direct methodological adoption or extension. Citation count alone must not determine the score. The response must distinguish broad citation visibility from direct influence and acknowledge temporal bias against newer papers.
7. **Ranking Method Consistency:** Full credit requires explicit weights, 1-5 scores for every paper on novelty, generality, empirical rigor, and scholarly influence, correct weighted-score calculations, and an overall ranking consistent with those scores. Alternative weights require justification before scoring. Any deviation from the numerical order must be explained.
8. **Criterion Conflict Reasoning:** Full credit requires at least two meaningful conflicts among ranking criteria and explains how they affect the ordering, including at least one discussion of citation-based influence versus another criterion or of the age bias inherent in citation counts.
9. **Source And Citation Integrity:** Full credit requires claims to be traceable to the seven provided papers and the specified online citation source, with corresponding in-text citations and reference entries. Fabricated papers, authors, venues, experiments, citation counts, dependencies, or source records are critical failures.
10. **Clarity And Format:** Full credit requires clear organization, comparative synthesis, readable Markdown, internally consistent tables and calculations, and approximately 1,600-2,000 words. Major omissions or contradictions between prose, tables, and calculations reduce this score.

## Required Evidence

Use the seven provided local PDFs as the primary sources for paper content. Use Semantic Scholar for current citation counts for all seven papers with one common retrieval date. If Semantic Scholar is unavailable for any paper, use OpenAlex for all seven papers and document the substitution. Do not mix citation-count platforms.

## Input Files

- `react.pdf`
- `reflexion.pdf`
- `toolformer.pdf`
- `voyager.pdf`
- `autogen.pdf`
- `camel.pdf`
- `metagpt.pdf`

## Scoring Rubric

- **Requirement Coverage (0.10):** Full credit requires all eleven required sections; coverage of all seven papers; all five required tables with the specified columns; one research gap supported by at least two papers; one future direction; citation data for all seven papers; scores for all seven papers on all four criteria; a weighted score and complete ranking; at least two criterion conflicts; and a References section containing all seven papers plus the citation-data source.
- **Seven Paper Summary Accuracy (0.18):** Full credit requires technically accurate descriptions of the research problem, mechanism or system design, contribution, evaluation setting, strength, and limitation for each paper. Each paper contributes approximately one seventh of this criterion. Major mechanism attribution errors, invented experiments, or assigning one paper's contribution to another receive little or no credit for the affected paper.
- **Cross Paper Relationship Accuracy (0.12):** Full credit requires careful use of the allowed relationship types and evidence-based distinctions among direct extension, mechanism reuse, framework integration, conceptual similarity, and no clear dependency. A related-work citation alone must not be treated as direct methodological influence.
- **Research Gap Quality (0.12):** Full credit requires one specific and nontrivial unresolved gap supported by limitations or open problems from at least two reviewed papers; an explanation of why the gap matters; evidence that the seven papers do not already fully solve it; and one feasible future research direction that directly addresses it.
- **Citation Data Accuracy And Consistency (0.15):** Full credit requires current citation counts for all seven papers from one consistent platform, a common retrieval date, correct publication years, and correct citations-per-year calculations. The answer must use canonical records matching title and authors, must not mix platforms, and must clearly document any switch from Semantic Scholar to OpenAlex. Missing, duplicated, mismatched, or fabricated records substantially reduce this score.
- **Scholarly Influence Reasoning (0.10):** Full credit requires influence judgments that combine total citations, citations per year, and evidence of direct methodological adoption or extension. Citation count alone must not determine the score. The response must distinguish broad citation visibility from direct influence and acknowledge temporal bias against newer papers.
- **Ranking Method Consistency (0.13):** Full credit requires explicit weights, 1-5 scores for every paper on novelty, generality, empirical rigor, and scholarly influence, correct weighted-score calculations, and an overall ranking consistent with those scores. Alternative weights require justification before scoring. Any deviation from the numerical order must be explained.
- **Criterion Conflict Reasoning (0.05):** Full credit requires at least two meaningful conflicts among ranking criteria and explains how they affect the ordering, including at least one discussion of citation-based influence versus another criterion or of the age bias inherent in citation counts.
- **Source And Citation Integrity (0.03):** Full credit requires claims to be traceable to the seven provided papers and the specified online citation source, with corresponding in-text citations and reference entries. Fabricated papers, authors, venues, experiments, citation counts, dependencies, or source records are critical failures.
- **Clarity And Format (0.02):** Full credit requires clear organization, comparative synthesis, readable Markdown, internally consistent tables and calculations, and approximately 1,600-2,000 words. Major omissions or contradictions between prose, tables, and calculations reduce this score.

## Expected Failure Risks

- Using citation count alone as the scholarly-influence score.
- Mixing citation counts from Semantic Scholar, OpenAlex, Google Scholar, or other platforms.
- Matching a citation count to the wrong or duplicate paper record.
- Failing to normalize citation impact by publication age.
- Treating a related-work citation as direct methodological influence.
- Misattributing one paper's mechanism, contribution, or experiment to another.
- Producing a ranking inconsistent with the scoring matrix without explanation.
- Giving a generic research gap not supported by at least two papers.

## Notes


