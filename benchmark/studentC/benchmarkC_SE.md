# Task: SE-06

## Metadata
- **Task ID:** SE-03
- **Category:** Software Engineering (System Design)
- **Difficulty:** Easy
- **Author:** Minjie Geng
- **Tool Requirement:** Prohibited

## Prompt
You are a backend architect for a large e-commerce platform. Due to a surge in traffic, your core relational database (MySQL) is facing immense read and write pressure. The team has decided to introduce Redis as a distributed cache.

Please analyze and compare the following three classic cache and database synchronization strategies:

- Cache-Aside
- Write-Through
- Write-Behind / Write-Back

Compare these three strategies across the following dimensions:

- Read Latency
- Write Latency
- Data Consistency Risk
- Implementation Complexity
- Data Loss Risk on Crash

After completing the comparison, please analyze the following two different business scenarios and recommend the most suitable caching strategy for each, justifying your choice:

**Scenario A: "User Profile Page".** The frequency of users updating their avatars or nicknames is extremely low, but the read frequency is extremely high. The data can tolerate a latency of a few hundred milliseconds.

**Scenario B: "Flash Sale Likes/Comments".** The concurrent write volume is terrifyingly high, and the database absolutely cannot handle direct writes. Even if a few scattered likes from the last few seconds are lost in an extreme crash, it is tolerable, but the system must absolutely not crash.

## Required Output Format
Use the following structure:

1.  Brief explanation of the operational mechanisms for the three caching strategies.
2.  Strategy comparison matrix.
3.  Scenario A (User Profile) analysis and recommendation.
4.  Scenario B (Flash Sale Likes) analysis and recommendation.

The comparison table must use the following exact column names:
| Strategy | Read Latency | Write Latency | Consistency Risk | Complexity | Data Loss Risk |

The response should be approximately 600–800 words.

## Ground Truth / Evaluation Criteria
The answer should satisfy the following criteria:

- Correctly explains Cache-Aside (application layer is responsible for reading/writing both cache and DB), Write-Through (application layer only writes to the cache, and the cache component synchronously writes to the DB), and Write-Behind (application layer only writes to the cache, and the cache component asynchronously/in batches writes to the DB).
- The comparison table must contain exactly the 6 required columns.
- Accurately identifies that Write-Through has high write latency but excellent consistency; Write-Behind has extremely fast writes but will lead to data loss if the system crashes before asynchronous flushing to the DB.
- **Scenario A Recommendation:** Must recommend Cache-Aside or Write-Through, pointing out that this scenario is a typical "read-heavy, write-light" case, and Cache-Aside's on-demand loading and low complexity are the best fit.
- **Scenario B Recommendation:** Must recommend Write-Behind (Write-Back). Explicitly states that only asynchronous batch flushing can withstand the extreme concurrent writes of a flash sale, and the business tolerance for "losing a small number of likes" perfectly offsets the fatal flaw of this strategy (data loss on crash).
- Must not confuse the synchronous/asynchronous mechanisms of Write-Through and Write-Behind.

## Required Evidence
No external citations are required. The task is based on classic caching architecture consensus in computer science. Fabricated performance benchmark data must not be invented (e.g., claiming QPS precisely increased by 5000).

## Scoring Rubric
The output must be evaluated using the standardized multi-agent metrics matrix.

1.  **Quality Metrics**
    - **Accuracy:** The workflow explanation of the caching strategies must be completely correct. If Write-Behind is explained as "synchronously writing to the database," this item scores a direct zero.
    - **Completeness:** Must include the 4 requested output sections and exactly matching table column names.
    - **Helpfulness:** The scenario analysis must logically bind technical characteristics with business requirements (e.g., read-heavy/write-light, tolerance for data loss) rather than just providing a conclusion.
    - **Hallucination Rate:** Hallucination Rate = Unsupported Technical Claims / Total Claims. If specific internal architectural details of a major tech company (like Amazon or Alibaba) are fabricated as supporting evidence, it will be penalized as a hallucination.
    - **Overall Quality Score:** A weighted score combining the above dimensions.
2.  **Efficiency & Resource Metrics**
    - **Runtime / Cost:** The time and Token count spent generating the architectural analysis.
    - **Quality-Cost Ratio:** Overall Quality Score / Cost.
    - **Tool Usage:** Tool usage is strictly prohibited; a call count > 0 results in an immediate Fail.
3.  **Multi-Agent Coordination Metrics**
    - **Message Count & Communication Density:** Evaluates task-splitting efficiency among multi-agents when assigning concept explanation, table generation, and scenario application tasks.
    - **Agreement Rate:** Assesses whether the reviewer agent identified vulnerabilities recommended by the drafting agent in Scenario B (high concurrent writes). If the drafting agent recommends the slow Write-Through and the reviewer agent fails to correct it, the consensus quality is low.

## Expected Failure Risks
- **Concept Confusion:** Confusing the logic of Cache-Aside updates (e.g., delete cache first, then update DB) with Write-Through.
- **Ignoring Business Tradeoffs:** In Scenario B, the AI suffers from "data purity obsession" and is afraid to recommend Write-Behind because it might lose data. Instead, it recommends an absolutely consistent solution, which causes the system to crash under flash sale concurrency (lacks the real business tradeoff ability of an architect).
- **Format Violations:** Forgetting to use the specified English table headers or arbitrarily adding/removing table columns.