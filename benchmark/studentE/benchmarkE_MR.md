# Task: MR-05

## Metadata

- Task ID: MR-05
- Category: Market Research
- Difficulty: Medium
- Author: Student E
- Tool Requirement: Required

## Prompt

Compare the current pricing plans and core features of two project-management SaaS tools: Notion and Asana. Then recommend which one a 5-person startup team should adopt, considering cost, core collaboration needs, and ease of onboarding. You must look up current pricing information rather than relying on potentially outdated knowledge, since SaaS pricing changes frequently.

## Required Output Format

Use the following format:

1. Short overview of Notion's current pricing tiers and core features
2. Short overview of Asana's current pricing tiers and core features
3. Comparison table
4. Recommendation paragraph, including the chosen plan for each tool and an estimated monthly cost for a 5-person team under those plans
5. Sources used for the pricing information, including retrieval date

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Correctly reports Notion's current pricing tiers, matching publicly available pricing information retrieved via tool use.
2. Correctly reports Asana's current pricing tiers, matching publicly available pricing information retrieved via tool use.
3. Compares core features relevant to a small team's collaboration needs (e.g., task management, docs/wiki, integrations).
4. Provides a concrete monthly cost estimate for a 5-person team under each tool's pricing plan, and clearly states the billing assumption used, such as monthly billing or annual billing converted to a monthly amount.
5. Gives a justified recommendation grounded in the cost and feature comparison, explains why the selected plan is appropriate for a 5-person startup team, and does not recommend a tool solely because it has the cheapest or free tier.
6. Cites the sources used for the pricing information.
7. Grounds any claim about ease of onboarding in specific, checkable product characteristics (e.g., interface complexity, initial setup steps, learning curve), rather than an unsupported assertion.

## Required Evidence

The answer must cite current, publicly available pricing sources, preferably the official Notion and Asana pricing pages. Because pricing changes over time, the answer must reflect information retrieved via web search rather than memorized training data.

## Notes

Expected tool: web search (general search engine, used to retrieve the official
Notion and Asana pricing pages). No other tool type is required for this task.

## Scoring Rubric

- Accuracy: Pricing and feature claims must match the actual current information retrieved, not outdated or invented figures.
- Completeness: The answer must cover all required comparison dimensions and provide a 5-person cost estimate for each tool.
- Helpfulness: The recommendation must be clear, actionable, and grounded in the stated team size and needs.
- Hallucination Penalty: Heavily penalize any pricing, feature, or onboarding- difficulty claim that is not backed by retrieved evidence or specific, checkable product characteristics — this is the primary hallucination risk for this task.


## Expected Failure Risks

- Relying on memorized (potentially outdated) pricing instead of actually using a tool to verify current information.
- Citing a price without noting the source or retrieval date, making the claim unverifiable.
- Recommending a tool based on general brand reputation rather than the concrete pricing and feature facts requested.
- Recommending a tool solely because it has the cheapest or free tier, without explaining whether that plan meets the team's collaboration and onboarding needs.
- Asserting that one tool is easier or harder to onboard without grounding the claim in specific, checkable product characteristics.