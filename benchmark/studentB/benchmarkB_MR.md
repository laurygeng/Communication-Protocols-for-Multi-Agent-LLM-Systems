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

Use current public sources and cite factual product, pricing, platform-support, privacy, consent, and data-retention claims. If a detail is not publicly clear, say it is unknown rather than guessing.

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

1. Compares at least four current AI meeting-assistant options.
2. Includes at least one platform-integrated option and at least one standalone option.
3. Verifies Zoom support where claimed and avoids claiming support when it is not sourced.
4. Verifies Google Meet support where claimed and avoids claiming support when it is not sourced.
5. Addresses searchable transcripts for each option or clearly states when unclear.
6. Addresses action-item extraction for each option or clearly states when unclear.
7. Addresses speaker identification for each option or clearly states when unclear.
8. Addresses note/export options for each option or clearly states when unclear.
9. Uses current public sources for capabilities, preferably official product or documentation pages.
10. Uses current public sources for pricing or plan availability where available.
11. Addresses privacy, consent, recording/transcription notice, and data-retention risks relevant to a university research lab.
12. Distinguishes verified facts from assumptions, unknowns, or details that require institutional/vendor confirmation.
13. Provides a comparison matrix with all required columns.
14. Includes a short discussion of market trends or differentiators that is supported by evidence or clearly labeled as synthesis.
15. Provides a justified recommendation for a 12-member, budget-sensitive lab using Zoom and Google Meet.
16. Explains tradeoffs among cost, ease of use, feature coverage, platform integration, privacy, and administration.
17. Includes risks, assumptions, and verification notes.
18. Includes a source list and cites factual product/pricing/privacy claims inline or in the matrix.
19. Avoids fabricated, outdated, or unsupported product, pricing, integration, compliance, privacy, or retention claims.
20. Follows all required output sections.

### Task Type

Current market research; external public evidence is mandatory.

### Must Have

- Compare at least four currently available AI meeting-assistant options.
- Include at least one platform-integrated option and at least one standalone option.
- Address the lab scenario: 12 members, Zoom and Google Meet, searchable transcripts, action-item extraction, speaker identification, export, budget sensitivity, privacy, consent, and data retention.
- Use current public sources to verify product capabilities and pricing or plan availability where available.
- Cite sources for features, integrations, pricing, privacy, consent, and data-retention claims.
- Clearly label unknown or unclear pricing/policy details instead of guessing.
- Provide a recommendation for the lab with tradeoffs, not just a winner.

### Must Not Have

- Do not fabricate prices, plan names, feature availability, integrations, data-retention policies, or compliance claims.
- Do not use outdated information as current without checking the publication/update context.
- Do not ignore consent and privacy risks for recording/transcription in a university lab.
- Do not recommend a product solely because it is popular without connecting it to the lab's requirements.

### Source Requirements

- **Minimum Options:** 4
- **Minimum Source Types:** Prefer official product, pricing, documentation, security/privacy, and support pages. Reputable reviews may supplement but should not replace official sources for pricing or policy claims.
- **Citation Requirement:** Every factual product capability, platform support, pricing/plan, privacy, or retention statement must have a citation or be labeled unknown/unverified.

### Acceptable Variations

- The exact products compared may vary as long as they are current and include both integrated and standalone options.
- Pricing may be summarized as public plan availability or starting tier if exact per-seat pricing is unclear.
- A recommendation may favor an integrated option, standalone option, or mixed approach if the tradeoffs are justified.

### Critical Fail Conditions

- No current public sources are cited.
- Fewer than four tools are compared.
- No integrated or no standalone option is included.
- The answer fabricates pricing or privacy/data-retention claims.

## Required Evidence

External evidence is required. Use current public sources such as official product pages, pricing pages, documentation, help-center articles, security/privacy pages, data-retention documentation, or reputable review sources. Official sources should be preferred for pricing, supported platforms, privacy, and retention. Claims about features, integrations, pricing, privacy policies, consent, compliance, or data retention must be cited. If pricing, feature availability, or policy details are not publicly clear, the answer must say so rather than infer or guess.

## Scoring Rubric

- **Scoring Method:** Score each evaluation criterion independently: 1 = fully satisfied, 0.5 = partially satisfied or present but underspecified, 0 = absent, incorrect, contradicted, or unsupported. Sum weighted criteria, then apply any hard-fail caps and hallucination penalties.
- **Score Bands:**
  - **Excellent:** 90-100% after caps: satisfies nearly all criteria, respects all hard constraints, and is specific enough to be used as a reference answer.
  - **Good:** 75-89% after caps: mostly correct and complete, with only minor omissions or weak specificity.
  - **Acceptable:** 60-74% after caps: covers the main task but has notable gaps, weak thresholds, weak evidence, or limited actionability.
  - **Poor:** 40-59% after caps: substantial omissions, vague reasoning, missing required sections, or multiple unsupported claims.
  - **Fail:** Below 40% after caps, or any critical contradiction/fabrication that makes the answer unusable.
- **Accuracy:** Judge whether product claims, pricing/plan notes, integrations, privacy statements, and retention/consent risks are current, source-supported, and not overstated.
- **Completeness:** Judge whether all lab requirements, required matrix columns, source list, recommendation, and verification notes are present.
- **Helpfulness:** Reward answers that are concrete, decision-oriented, prioritized, and directly usable by the stated audience. Penalize generic advice that could apply to any scenario.
- **Grounding And Evidence:** For tool-required tasks, every factual product, paper, pricing, policy, benchmark, or empirical claim must be tied to a credible public source. For tool-prohibited tasks, answers must not cite external sources or invent outside facts; they should reason only from the prompt and standard conceptual knowledge.
- **Hallucination Penalty:** Penalize fabricated prices, outdated information presented as current, unsupported feature or integration claims, unverified compliance/security assertions, and recommendations that ignore privacy or budget constraints.
- **Hard Fail Rules:**
  - Cap score at 50% if fewer than four products are compared.
  - Cap score at 60% if either integrated or standalone options are missing.
  - Cap score at 50% if no public sources are cited.
  - Cap score at 40% if pricing or privacy claims are fabricated or materially unsupported.
  - Cap score at 70% if privacy, consent, and data retention are mostly ignored.

## Expected Failure Risks

- Using outdated pricing or feature information.
- Ignoring privacy, consent, or data-retention concerns.
- Comparing only popular standalone tools and omitting an integrated option.
- Making unsupported claims about compliance or security.
- Failing to verify Zoom and Google Meet support separately.
- Guessing data-retention policies when public documentation is unclear.
- Choosing the cheapest option without discussing required features and institutional risks.

## Notes

This task should be graded harshly for current-source grounding. Market research with unsupported prices or policies should not score well even if the recommendation sounds plausible.
