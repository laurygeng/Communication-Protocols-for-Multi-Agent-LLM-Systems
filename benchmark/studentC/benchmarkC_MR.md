# Task: MR-03

## Metadata
- **Task ID:** MR-03
- **Category:** Market Research (Competitive Analysis & Strategic Sourcing)
- **Difficulty:** Hard
- **Author:** Minjie Geng
- **Tool Requirement:** Required

## Prompt
You are a Principal Market Research Analyst for a mid-sized US-based Video Production Agency (75 full-time employees, plus hundreds of rotating freelance editors). You are evaluating enterprise cloud storage and collaboration platforms to replace their aging local NAS servers.

Conduct a competitive analysis of Dropbox (Advanced Plan), Box (Enterprise Plan), and Microsoft OneDrive for Business (Plan 2).

Your recommendation must navigate the following complex and competing constraints:

- **The Massive File Bottleneck:** The team routinely edits and syncs 8K raw video files. Single video files frequently exceed 100 GB to 150 GB. True block-level sync (delta sync) is mandatory to avoid re-uploading entire massive files for a 5MB metadata or color-grade change.
- **The External Collaborator Tax:** Freelancers must be able to securely upload massive raw footage files directly to the agency's cloud via shared links without the agency needing to purchase a paid SaaS seat for every freelancer.
- **The Strict Budget Ceiling:** The maximum annual software licensing cost for the 75 internal employees is capped at $25,000 per year. (You must research current public annual pricing per user to calculate this).
- **The Security Requirement:** They need robust link sharing with expiration dates, password protection, and granular access controls.

## Required Output Format
Use the following strict structure:

1.  Executive Summary & The Video Production Dilemma (Highlighting the conflict between massive media files, licensing costs, and cloud sync limitations).
2.  Comprehensive Comparison Matrix (Using the exact column headers specified below).
3.  Trend Identification (Explain the industry shift from "Local NAS" to "Hybrid Cloud Video Workflows" in 2-3 sentences).
4.  Final Strategic Recommendation (Explicitly recommend one platform, or a "No-Go". You must justify how your choice mathematically and technically passes the file size and budget constraints).
5.  Source List.

### Required Comparison Matrix
The matrix must include exactly the following columns:
| Platform & Tier | Estimated Annual Cost (75 Users) | Max Single File Upload Limit | Block-Level (Delta) Sync Support | External Free Upload Capabilities |

The response should be approximately 800–1,200 words.

## Ground Truth / Evaluation Criteria
The answer should satisfy the following criteria:

- **Financial Accuracy & TCO Modeling:**
    - Dropbox Advanced: ~$24/user/month = ~$21,600/year (Fits the $25k budget).
    - Box Enterprise: ~$35/user/month = ~$31,500/year (Breaches the budget).
    - OneDrive Plan 2: ~$10/user/month = ~$9,000/year (Fits the budget).
- **The "Single File Limit" Trap (Crucial Verification):**
    - The AI must identify that Box Enterprise has a strict single file upload limit (typically 50GB), which completely disqualifies it for a company working with 100GB-150GB 8K video files.
    - OneDrive allows up to 250GB. Dropbox allows up to 2TB (via desktop app).
- **Technical Sync Capabilities:** Identifies that while all claim some form of differential sync, Dropbox is historically the industry leader for handling massive binary files (like video) via block-level delta and LAN sync.
- **External Uploads:** Recognizes features like Dropbox "File Requests" or Box "File Request" that allow external uploads without consuming paid licenses.
- **Final Recommendation:** Must definitively recommend Dropbox Advanced. Box fails on both budget and file size limits. OneDrive passes budget but struggles with massive video file delta-sync performance compared to Dropbox.

## Required Evidence
Must use current, public pricing and technical specification data from the official websites of Dropbox, Box, and Microsoft.

Specifically, the AI must cite the official "Maximum Single File Size Limit" documentation for each platform.

## Scoring Rubric
Each protocol output must be evaluated using the standardized multi-agent metrics matrix.

- **Accuracy:** Must accurately report the exact file size limits and pricing. Claiming "Box has unlimited file sizes" results in a severe hallucination penalty.
- **Completeness:** Must include the 5 required sections and exact matrix columns.
- **Strategic Synthesis:** The recommendation must logically eliminate Box based on the mathematically proven budget breach and the technical file-limit breach.
- **Coordination & Instruction Following:** Strict adherence to constraints.

## Expected Failure Risks (Multi-Agent Collapse Points)
- **The File Size Hallucination:** A drafting agent assumes "Enterprise Cloud = Unlimited" and falsely claims Box or OneDrive can upload 500GB files, completely missing the technical hard limits that kill the deal for video agencies.
- **The Budget Silo Failure:** The "Financial Agent" calculates Box costs but forgets to tell the "Strategy Agent" that $31,500 exceeds the $25,000 cap, resulting in a contradictory final recommendation.