---
title: "Project Kick-off — Proposal, Architecture & Repository Setup"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

# WEEK 5 WORKLOG

### Week 5 Objectives:

* Kick off the LingoRise project: establish repository guidelines, initial database schema, and AWS service plans.
* Research and develop the integration architecture for the Sepay payment automation gateway.
* Implement AI-driven question bank generation using copied online markdown exam sheets.
* Study and resolve question generator failure modes (JSON truncation, prose commentary, answer anomalies).

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Draft the project proposal, define core AWS stacks (Lambda, API Gateway, S3, Cognito), and initialize the monorepo structure | 18/05/2026 | 18/05/2026 | <https://docs.aws.amazon.com/> |
| Wed | - Read Sepay API docs: analyze how bank transfer alerts are sent, check webhook payload parameters, and study signature verification models | 20/05/2026 | 20/05/2026 | <https://docs.sepay.vn/> |
| Thu | - Write Express route handler `/api/v1/payments/sepay-webhook` to catch callback payloads and extract transaction properties | 21/05/2026 | 21/05/2026 | <https://expressjs.com/> |
| Fri | - **Markdown-to-Exam AI Parser Experiment:** Paste raw markdown exams copied from websites to test AI question generator <br> - Resolve output issues: 1) AI writing prose commentary (fixed with Regex `extractJsonObject()` parser), 2) JSON truncation (fixed by increasing `max_tokens` to 4000+), 3) Answer key mapping anomalies (fixed by enforcing exact substring evidence match and server validations) | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 5 Achievements:

* **Project Initialization**: Established monorepo workspace for frontend and backend with Cognito and SAM deployment pipelines.
* **Sepay API Understanding**: Mastered the webhook mechanisms of Sepay, mapping raw financial transfers to database objects.
* **Database Payment Schema**: Designed secure PostgreSQL schemas utilizing integer types to avoid decimal precision bugs during payment math.
* **AI Question Bank Generator**: Created a pipeline converting raw copied markdown exam sheets into clean, structured JSON question pools.
* **Robust JSON Extraction**: Solved AI parser output anomalies (prose wraps) by implementing a Regex-based JSON extractor in the parser engine.
* **Output Validation Rules**: Implemented strict validation checks for correct answer validation, TFNG structure formatting, and exact evidence substring verification.
