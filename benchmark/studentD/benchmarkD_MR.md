
# Task: MR-04

## Metadata

- Task ID: MR-04
- Category: Market Research
- Difficulty: Easy
- Author: Haofan Hou
- Tool Requirement: Required

## Prompt

Compare Slack and Microsoft Teams as communication and collaboration products for a small remote company.

Use current information from the official product websites to compare the two products in terms of:

1. Primary target users
2. Core communication features
3. Collaboration and integration features
4. Main strength
5. Main limitation

Based on the comparison, recommend one product for a small remote company that needs daily messaging, file sharing, video meetings, and basic integration with other workplace tools.

Support the recommendation with evidence from the reviewed sources.

## Required Output Format

Use the following structure:

1. Brief market overview
2. Product comparison table
3. Recommendation paragraph
4. Source list

The comparison table must use the following columns:

| Product | Target Users | Core Communication Features | Collaboration and Integrations | Main Strength | Main Limitation |
|---|---|---|---|---|---|

The response should be approximately 400–600 words.

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Correctly identifies Slack and Microsoft Teams as workplace communication and collaboration products.
2. Describes the primary target users of both products.
3. Summarizes the main messaging, file-sharing, meeting, and integration capabilities of both products.
4. Identifies at least one reasonable strength and one reasonable limitation for each product.
5. Clearly compares the two products rather than describing them separately without analysis.
6. Recommends one product for the stated small remote company.
7. Supports the recommendation with relevant comparison evidence.
8. Uses the required table, recommendation paragraph, and source list.

## Required Evidence

The answer must use current public information from official Slack and Microsoft sources.

At least two sources are required, including at least one official source for each product.

Claims about product features, integrations, availability, or plan limitations must be supported by the cited sources.

Exact pricing is not required.

## Scoring Rubric

- Accuracy: Product features, target users, strengths, and limitations must be described correctly and supported by official sources.
- Completeness: The answer must compare both products across all five required areas and provide a recommendation.
- Helpfulness: The comparison should make it easy for a small remote company to understand which product better fits its needs.
- Hallucination Penalty: Penalize fabricated features, unsupported product claims, outdated information presented as current, or citations that do not support the claims.

## Expected Failure Risks

- Listing product features without directly comparing the two products.
- Using outdated or unofficial information.
- Claiming that a feature is available without checking whether it depends on a particular plan.
- Giving a recommendation without connecting it to messaging, file sharing, meetings, and integrations.
- Presenting personal preference as market evidence.
- Inventing product capabilities, limitations, or pricing information.

## Notes

This task evaluates basic product comparison, current-source retrieval, and evidence-based recommendation.

