# Task: EC-05

## Metadata

- Task ID: EC-05
- Title: Explaining Communication Protocols in Multi-Agent LLM Systems
- Category: Educational Content
- Difficulty: Easy
- Author: Student E
- Tool Requirement: Prohibited

## Prompt

Explain what a communication protocol is in a multi-agent LLM system to a beginner who already understands what an AI agent is but has never studied multi-agent communication.

The explanation must describe what a communication protocol controls and why it is needed when multiple AI agents work together.

Use the following structure:
1. Plain-Language Definition
2. Two Things a Communication Protocol Controls
3. Why Communication Protocols Are Important
4. Real-World Analogy

In the second section, identify exactly two elements that a communication protocol may control. Valid examples include which agent communicates, when an agent communicates, what information is shared, which agents can see a message, the order of communication, or when the interaction ends.

In the third section, explain at least one coordination problem that a communication protocol can help reduce, such as duplicated work, missing information, conflicting actions, or unclear responsibilities.

In the final section, use one simple real-world analogy, such as a classroom group project, workplace team, restaurant staff, or sports team, and clearly connect the analogy to communication among AI agents.

Keep the response between 120 and 200 words. Use beginner-friendly language. Do not use external sources, web search, citations, statistics, or unsupported claims about the performance of specific systems.

## Required Output Format

- Type: markdown
- Required sections:
  1. Plain-Language Definition
  2. Two Things a Communication Protocol Controls
  3. Why Communication Protocols Are Important
  4. Real-World Analogy

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. **Requirement Coverage:** Full credit requires all four required sections, exactly two clearly identified protocol-controlled elements, at least one coordination problem, and one real-world analogy. Reduce proportionally for each missing section or required element. If the answer provides fewer than two controlled elements or omits the analogy, this criterion should receive no more than half credit.
2. **Definition Accuracy:** Full credit requires a technically correct plain-language definition explaining that a communication protocol is a set of rules or an organized structure that determines how multiple AI agents exchange information and coordinate their work. The answer must not describe the protocol as an AI model, an individual agent, a physical network connection, or merely a software tool. Minor wording differences are acceptable when the core meaning is preserved.
3. **Control Elements Accuracy:** Full credit requires exactly two valid and distinct controlled elements. Acceptable elements include speaker or agent selection, communication timing, message order, information content, message visibility, maximum communication rounds, or termination conditions. Each element must be briefly explained rather than only named. Repeated or overlapping elements count as one. Invalid examples, such as model training data or hardware speed, should not receive credit.
4. **Importance And Coordination Reasoning:** Full credit requires a clear explanation of why communication rules are needed when several agents work together and correctly connects the protocol to at least one coordination problem, such as duplicated work, lost or missing information, conflicting actions, unclear responsibilities, role confusion, or premature completion. The response should explain the connection, not merely list a problem.
5. **Analogy Quality:** Full credit requires one simple, relevant real-world analogy and an explicit mapping between the analogy and a multi-agent system. For example, team members may represent agents and meeting rules or assigned speaking order may represent the communication protocol. An analogy that is present but not explained receives partial credit. An unrelated analogy receives no credit.
6. **Beginner Accessibility:** Full credit requires clear, beginner-friendly wording, short or moderately sized sentences, and minimal technical jargon. Any necessary technical term should be explained in context. Reduce the score for dense academic language, unexplained terminology, or examples that assume prior knowledge of specific multi-agent frameworks.
7. **Format And Length Compliance:** Full credit requires readable Markdown using the four specified section headings and a total response length between 120 and 200 words. A response outside the word range or with minor heading differences receives partial credit. A response that ignores the requested structure receives little or no credit.
8. **Evidence Integrity:** Full credit requires a conceptual answer with no external citations, web-derived facts, invented statistics, fabricated empirical comparisons, or unsupported claims about named systems. Mentioning a specific framework is unnecessary. Any invented performance number or false factual claim should substantially reduce this score.

## Required Evidence

No external evidence or citations are required. Answer from the prompt, provided constraints, and internal reasoning only.

## Input Files

- None

## Scoring Rubric

- **Requirement Coverage (0.20):** Full credit requires all four required sections, exactly two clearly identified protocol-controlled elements, at least one coordination problem, and one real-world analogy. Reduce proportionally for each missing section or required element. If the answer provides fewer than two controlled elements or omits the analogy, this criterion should receive no more than half credit.
- **Definition Accuracy (0.20):** Full credit requires a technically correct plain-language definition explaining that a communication protocol is a set of rules or an organized structure that determines how multiple AI agents exchange information and coordinate their work. The answer must not describe the protocol as an AI model, an individual agent, a physical network connection, or merely a software tool. Minor wording differences are acceptable when the core meaning is preserved.
- **Control Elements Accuracy (0.15):** Full credit requires exactly two valid and distinct controlled elements. Acceptable elements include speaker or agent selection, communication timing, message order, information content, message visibility, maximum communication rounds, or termination conditions. Each element must be briefly explained rather than only named. Repeated or overlapping elements count as one. Invalid examples, such as model training data or hardware speed, should not receive credit.
- **Importance And Coordination Reasoning (0.15):** Full credit requires a clear explanation of why communication rules are needed when several agents work together and correctly connects the protocol to at least one coordination problem, such as duplicated work, lost or missing information, conflicting actions, unclear responsibilities, role confusion, or premature completion. The response should explain the connection, not merely list a problem.
- **Analogy Quality (0.10):** Full credit requires one simple, relevant real-world analogy and an explicit mapping between the analogy and a multi-agent system. For example, team members may represent agents and meeting rules or assigned speaking order may represent the communication protocol. An analogy that is present but not explained receives partial credit. An unrelated analogy receives no credit.
- **Beginner Accessibility (0.10):** Full credit requires clear, beginner-friendly wording, short or moderately sized sentences, and minimal technical jargon. Any necessary technical term should be explained in context. Reduce the score for dense academic language, unexplained terminology, or examples that assume prior knowledge of specific multi-agent frameworks.
- **Format And Length Compliance (0.05):** Full credit requires readable Markdown using the four specified section headings and a total response length between 120 and 200 words. A response outside the word range or with minor heading differences receives partial credit. A response that ignores the requested structure receives little or no credit.
- **Evidence Integrity (0.05):** Full credit requires a conceptual answer with no external citations, web-derived facts, invented statistics, fabricated empirical comparisons, or unsupported claims about named systems. Mentioning a specific framework is unnecessary. Any invented performance number or false factual claim should substantially reduce this score.

## Expected Failure Risks

- Misdefining a communication protocol as an AI model, agent, or software tool.
- Failing to provide exactly two distinct controlled elements.
- Listing a coordination problem without explaining how the protocol reduces it.
- Using an analogy without mapping its parts to agents and communication rules.
- Ignoring the required structure or word limit.

## Notes

