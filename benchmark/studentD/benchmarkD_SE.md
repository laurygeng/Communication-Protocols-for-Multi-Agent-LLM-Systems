
# Task: SE-04

## Metadata

- Task ID: SE-04
- Category: Software Engineering
- Difficulty: Medium
- Author: Haofan Hou
- Tool Requirement: Prohibited

## Prompt

Design the backend software architecture for a document-processing and search service.

The service must allow users to upload PDF, TXT, and Markdown files. After a file is uploaded, the system should:

1. Validate the file type and size.
2. Store the original file and its metadata.
3. Extract the document text.
4. Divide the text into searchable sections.
5. Create a searchable index.
6. Allow users to search the processed documents.
7. Report the processing status of each uploaded file.

The design must also support the following requirements:

- Files may be processed asynchronously.
- A failed processing step should be retryable.
- Repeated uploads of the same file should not create unnecessary duplicate records.
- New document formats should be easy to add later.
- The design should remain understandable and maintainable for a small development team.

Produce a software design that explains the system components, data flow, API interface, data model, code organization, error-handling strategy, and testing plan.

Provide a software design rather than a complete runnable application. Short pseudocode, interface definitions, data structures, or code examples may be included where they help clarify the design.

## Required Output Format

Use the following structure:

1. System overview
2. Main components and responsibilities
3. End-to-end processing workflow
4. REST API design
5. Data model
6. Suggested project structure
7. Error handling, retry, and duplicate prevention
8. Testing plan
9. Design tradeoff

Include the following two tables.

### Component Table

| Component | Main Responsibility | Input | Output |
|---|---|---|---|

### API Table

| Method | Endpoint | Purpose | Main Request Data | Main Response Data |
|---|---|---|---|---|

The response should be approximately 700–900 words.

## Ground Truth / Evaluation Criteria

The answer should satisfy the following criteria:

1. Separates file validation, storage, text extraction, text chunking, indexing, and search into clear responsibilities.
2. Describes a complete workflow from file upload to searchable document content.
3. Includes a mechanism for tracking processing states, such as uploaded, processing, completed, and failed.
4. Provides suitable API operations for file upload, processing-status retrieval, document search, and document retrieval or deletion.
5. Defines a data model that includes document identity, file metadata, processing status, and error information.
6. Includes a reasonable strategy for detecting or preventing unnecessary duplicate uploads.
7. Explains how failed processing steps can be retried without incorrectly repeating completed work.
8. Uses modular interfaces or components so that additional document formats can be added later.
9. Provides a clear and realistic project or folder structure.
10. Includes unit, integration, and end-to-end testing considerations.
11. Identifies at least one meaningful design tradeoff and explains its consequences.
12. Follows the required structure and includes both required tables.

## Required Evidence

No external citations are required.

The task should be answered using software engineering reasoning based on the requirements in the prompt.

The answer may include short pseudocode, interface definitions, data structures, example JSON objects, or code snippets to clarify the proposed design.

The answer must not claim that the proposed system has been implemented, empirically tested, or proven to achieve specific performance results.

## Scoring Rubric

- Accuracy: The proposed architecture, API design, workflow, data model, and failure-handling strategy must be technically reasonable and internally consistent.
- Completeness: The answer must cover all required system stages, APIs, processing states, duplicate prevention, retry handling, extensibility, code organization, testing, and one design tradeoff.
- Helpfulness: The design should be clear and specific enough that a small development team could use it as an implementation plan.
- Hallucination Penalty: Penalize unsupported claims about guaranteed performance, scalability, security certification, tested reliability, or implementation results.

## Expected Failure Risks

- Producing only a high-level architecture without explaining component responsibilities or data flow.
- Combining validation, extraction, indexing, and search into one poorly separated module.
- Omitting processing-status tracking for asynchronous work.
- Retrying the entire pipeline without considering idempotency or previously completed steps.
- Suggesting duplicate detection without explaining which identifier, checksum, or file property would be used.
- Providing vague API endpoints without describing the main request and response data.
- Ignoring extensibility for additional document formats.
- Listing tests without distinguishing unit, integration, and end-to-end testing.
- Providing excessive implementation code while neglecting the requested architecture and design reasoning.
- Overengineering the system with unnecessary services for a small development team.

## Notes

This task evaluates system design, modular architecture, implementation planning, failure handling, and test planning.
