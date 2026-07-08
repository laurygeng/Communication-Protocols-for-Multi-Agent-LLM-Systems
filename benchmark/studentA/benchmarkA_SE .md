# Task: SE-01

## Metadata

Task ID: SE-01  
Category: Software Engineering  
Difficulty: Medium  
Author: Student A  
Tool Requirement: Prohibited  

## Prompt

Build a simplified local bilingual web application called **金钱卦 / Coin Oracle** using HTML, CSS, and JavaScript.

The application should be a six-line coin reading tool. It must support both Chinese-speaking and English-speaking users. The full user interface should be Chinese-English bilingual.

The app must support two modes:

1. Automatic mode  
   The system simulates three coins for each line, repeats this process six times, and generates six lines from bottom to top.

2. Manual mode  
   The user can enter six line values manually. Each line value must be one of: 6, 7, 8, or 9.

Use the following coin rules:

- Heads = 3
- Tails = 2
- 6 = old yin, changing line, broken line changes to solid
- 7 = young yang, stable line, solid line
- 8 = young yin, stable line, broken line
- 9 = old yang, changing line, solid line changes to broken

The bottom three lines form the lower trigram. The top three lines form the upper trigram. The application must use the provided 64-hexagram reference table to identify the starting image and changed image.

For each reading, the app must display:

- Hexagram number
- Chinese name
- Pinyin
- Simple image-based English name
- Classic English name as a secondary note
- Starting Image / 本卦
- Changed Image / 变卦
- Changing Lines / 变爻

The English should be simple, image-rich, and easy for English-speaking users to understand. It may have a gentle old-scroll feeling, but it must avoid difficult archaic grammar.

The app must also generate copyable DeepSeek interpretation prompts in both Chinese and English. The app itself must not call DeepSeek or any external AI API.

## Required Output Format

Use the following format:

1. Short instruction explaining how to run the file
2. One complete code block containing the full `index.html`

The generated application must satisfy these output requirements:

- One self-contained `index.html` file
- Internal CSS and JavaScript allowed
- No package installation
- No backend
- No external API calls
- No API key
- Runs by opening `index.html` in a normal web browser

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Provides a complete working local web application.
2. Includes a user question input.
3. Includes automatic casting mode.
4. Includes manual input mode for six line values.
5. Automatic casting simulates three coins per line instead of directly randomizing 6, 7, 8, and 9.
6. Counts heads as 3 and tails as 2.
7. Generates exactly six lines.
8. Preserves bottom-to-top line generation logic.
9. Correctly treats 6 as old yin and a changing line.
10. Correctly treats 7 as young yang and a stable line.
11. Correctly treats 8 as young yin and a stable line.
12. Correctly treats 9 as old yang and a changing line.
13. Treats only 6 and 9 as changing lines.
14. Creates the changed pattern by flipping only changing lines.
15. Calculates the lower trigram from the bottom three lines.
16. Calculates the upper trigram from the top three lines.
17. Uses the provided 64-hexagram reference table.
18. Displays Chinese name, pinyin, and simple image-based English name.
19. Uses Chinese-English bilingual UI labels.
20. Includes a short final bilingual reading note based on the calculated result.
21. Uses simple image-rich English with a gentle old-scroll feeling.
22. Generates a structured Chinese DeepSeek interpretation prompt.
23. Generates a structured English DeepSeek interpretation prompt.
24. English DeepSeek prompt asks for simple, image-rich explanation.
25. Provides visible copy buttons for prompt content.
26. Includes local history or a simple saved-reading area.
27. Includes an entertainment and self-reflection disclaimer.
28. Does not include Tarot cards or unrelated divination systems.
29. Does not call any external AI API and does not include an API key.
30. Does not fabricate advanced divination fields that the application does not actually calculate.

## Required Evidence

No external citation is required. The task should be solved from the given task prompt and reference material.

The submitted answer must provide enough evidence for evaluators to inspect:

- Complete source code of the web application
- Automatic three-coin simulation logic
- Manual input logic
- 64-hexagram lookup logic
- Starting Image and Changed Image result display
- Changing-line logic
- Chinese and English DeepSeek prompts
- Disclaimer text

Reference material:

- `task/hexagram_reference_table.md`

## Scoring Rubric

Accuracy: The application must correctly implement coin rules, line mapping, changing-line logic, upper/lower trigram logic, and 64-hexagram lookup.

Completeness: The application must include all required user-facing features, including automatic mode, manual mode, bilingual result display, final reading note, prompt export, copy buttons, saved readings, and disclaimer.

Helpfulness: The interface and prompts must be clear, usable, bilingual, and understandable for users who do not know Chinese metaphysical terminology.

Hallucination Penalty: Penalize fabricated hexagram names, unsupported advanced divination fields, fake calculations, hidden API calls, hidden API keys, or claims about features that are not actually implemented.

## Expected Failure Risks

- Directly randomizing 6, 7, 8, and 9 instead of simulating three coins.
- Reversing bottom-to-top line order.
- Confusing stable lines and changing lines.
- Mapping 6, 7, 8, and 9 incorrectly.
- Flipping all lines instead of only changing lines.
- Reversing upper and lower trigrams.
- Using incorrect 64-hexagram mappings.
- Ignoring the simple image-based English names.
- Producing English that is too academic, too literal, or too difficult.
- Omitting the Chinese DeepSeek prompt.
- Omitting the English DeepSeek prompt.
- Omitting manual input mode.
- Omitting copy buttons.
- Calling an external API.
- Including an API key.
- Adding Tarot or unrelated divination systems.
- Fabricating advanced fields that the app does not calculate.
