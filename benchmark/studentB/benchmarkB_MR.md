# Task: MR-02

## Metadata

- Task ID: MR-02
- Category: Market Research
- Difficulty: Medium
- Author: Zhiqi Hu
- Tool Requirement: Required

## Prompt

Conduct a current market comparison of AI meeting-assistant tools for a small university research lab.

Scenario: The lab has 12 members, uses Zoom and Google Meet, wants searchable meeting transcripts, action-item extraction, speaker identification, and easy export of notes. The lab is budget-sensitive and must consider privacy, consent, and data-retention risks.

Compare at least four currently available AI meeting-assistant options, including at least one platform-integrated option and at least one standalone option. Use public sources to verify current product capabilities and pricing or plan availability where available. End with a recommendation for the lab and explain the main tradeoffs.

## Required Output Format

Use the following format:
1. Brief market context
2. Comparison matrix with columns: Product, Standalone or Integrated, Supported Meeting Platforms, Key Features, Public Pricing / Plan Notes, Privacy or Data-Retention Notes, Best Fit, Limitations
3. Short discussion of market trends or differentiators
4. Recommendation for the 12-member lab
5. Risks, assumptions, and verification notes
6. Source list

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Compares at least four current AI meeting-assistant options and includes both standalone and platform-integrated tools.
2. Uses current public sources for product capabilities and pricing or plan availability where available.
3. Addresses the lab's stated requirements: Zoom, Google Meet, transcripts, action items, speaker identification, export, budget, privacy, consent, and data retention.
4. Distinguishes verified facts from assumptions or unknowns.
5. Provides a justified recommendation with tradeoffs rather than selecting a product based only on one feature.
6. Includes a source list and cites sources for factual product or pricing claims.

## Required Evidence

External evidence is required. The answer must use current public sources such as official product pages, pricing pages, documentation, or reputable review sources. Claims about features, integrations, pricing, privacy policies, or data-retention practices must be cited. If pricing or a policy is not publicly clear, the answer should say so instead of guessing.

## Scoring Rubric

- Accuracy: Judge whether product claims, pricing notes, and integration claims are current and source-supported.
- Completeness: Judge whether all lab requirements and required output sections are covered.
- Helpfulness: Judge whether the recommendation is practical for a small university research lab and clearly explains tradeoffs.
- Hallucination Penalty: Penalize fabricated prices, unsupported feature claims, outdated information presented as current, or unverified privacy claims.

## Expected Failure Risks

- Using outdated pricing or feature information.
- Ignoring privacy, consent, or data-retention concerns.
- Comparing only popular tools and omitting an integrated option.
- Making unsupported claims about compliance or security.

## Notes

This is a medium market research task because it requires current evidence, comparison, and recommendation, but the market segment and buyer scenario are constrained.
