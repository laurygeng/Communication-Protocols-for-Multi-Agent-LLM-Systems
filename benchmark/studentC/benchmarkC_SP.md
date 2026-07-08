# Task: SP-03

## Metadata
- **Task ID:** SP-03
- **Category:** Strategic Planning (Product Launch & Roadmap)
- **Difficulty:** Easy
- **Author:** Minjie Geng
- **Tool Requirement:** Prohibited

## Prompt
You are creating a product launch roadmap for a new B2B software application. The company uses a standard 3-phase release strategy: Alpha Release, Beta Release, and General Availability (GA).

First, create a mapping table that assigns the correct Target Audience to each phase. You must choose the audience strictly from the following three options:
[Entire Public Market], [Internal Employees / QA Team], [Selected External Early Adopters].

The table must use exactly these columns:
Release Phase, Target Audience, and Primary Strategic Objective (1 sentence).

Second, answer the following simple scenario in one sentence:
**Scenario:** During the Beta Release, the team discovers a critical security vulnerability that allows unauthorized data access. The Marketing team wants to ignore it and push to General Availability (GA) tomorrow to meet the deadline. As the Strategic Planner, do you approve the push to GA or halt the launch? Provide a brief justification.

## Required Output Format
Use the following strict structure:

1.  Release Roadmap Table (using the exact column headers requested).
2.  Scenario Decision (stating "Approve" or "Halt" with a 1-sentence justification).

## Ground Truth / Evaluation Criteria
The answer should satisfy the following criteria:

- **Table Accuracy - Alpha:** Correctly maps to [Internal Employees / QA Team]. The objective should focus on finding initial bugs and verifying basic functionality in a safe environment.
- **Table Accuracy - Beta:** Correctly maps to [Selected External Early Adopters]. The objective should focus on gathering real-world user feedback and testing system stability under limited load.
- **Table Accuracy - GA:** Correctly maps to [Entire Public Market]. The objective should focus on maximizing user acquisition, revenue, and full public operation.
- **Scenario Resolution:** Correctly decides to **Halt** the launch.
- **Justification:** Explains that a critical security vulnerability poses severe legal, reputational, and privacy risks that outweigh the benefit of meeting a marketing deadline.

## Required Evidence
No external citations are required. The task tests basic, factual knowledge of standard product launch lifecycles and fundamental risk management.

## Scoring Rubric
Each protocol output must be evaluated using the standardized multi-agent metrics matrix.

1.  **Quality Metrics**
    - **Accuracy:** Strict factual correctness in mapping the three predefined audiences to the correct release phases.
    - **Completeness:** Must include the table with exactly 3 columns (containing 3 rows for the phases) and the brief scenario answer.
    - **Helpfulness:** The scenario answer must clearly state the decision (Halt) before justifying it.
    - **Hallucination Rate:** Hallucination Rate = Unsupported Factual Claims / Total Factual Claims. Penalize claims that invent additional release phases (e.g., adding a "Gamma" phase) or invent new audience options not provided in the prompt.
    - **Overall Quality Score:** Weighted aggregate of Accuracy, Completeness, and Helpfulness.
2.  **Efficiency & Resource Metrics**
    - **Runtime / Cost:** Total generation time and token usage. For an Easy task, this should be highly optimized and fast.
    - **Quality-Cost Ratio:** Overall Quality Score / Cost.
    - **Tool Usage:** External tool calls. Since Tool Requirement: Prohibited, any value > 0 constitutes an immediate failure.
3.  **Multi-Agent Coordination Metrics**
    - **Message Count & Communication Density:** Evaluates how efficiently the agents complete a simple classification and decision task.
    - **Agreement Rate:** Checks if peer-review agents reach consensus immediately on the "Halt" decision.
    - **Critique Acceptance Rate:** Expected to be 0 or close to it, as the primary drafting agent should output the standard facts correctly on the first pass.

## Expected Failure Risks
- **Audience Mismatch:** Swapping the audiences for Alpha and Beta (e.g., testing with external users before internal QA is finished).
- **Ignoring Constraints:** Inventing new audience descriptions instead of using the exact three string options provided in the prompt.
- **Poor Prioritization (Scenario):** Approving the launch to GA because "marketing deadlines are strict," failing the most basic strategic risk assessment regarding data security.
- **Formatting Errors:** Failing to use the exact specified English column headers for the matrix.