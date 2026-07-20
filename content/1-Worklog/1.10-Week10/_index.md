---
title: "Handover, Final Report & Presentation"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

# WEEK 10 WORKLOG

### Week 10 Objectives:

* Fix production bugs discovered during Week 9 smoke testing: edge cases in exam scoring, file upload errors, and UI rendering inconsistencies.
* Harden platform security: implement input validation on all API endpoints, add rate limiting middleware, and enforce parameterized SQL queries.
* Optimize performance: reduce Lambda cold start times, compress S3 media assets, and tune database query execution plans.
* Run final code cleanup and ensure all build/lint/test commands pass cleanly.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Tue | - Implement Joi input validation schemas on all API Gateway endpoints <br> - Add express-rate-limit middleware to prevent brute-force attacks on auth endpoints <br> - Audit all SQL queries to confirm parameterized execution | 23/06/2026 | 23/06/2026 | <https://express-validator.github.io/docs/> |
| Wed | - Optimize Lambda cold starts: reduce package bundle size by tree-shaking unused dependencies <br> - Configure Lambda provisioned concurrency for the exam submission handler to ensure consistent response times | 24/06/2026 | 24/06/2026 | <https://docs.aws.amazon.com/lambda/latest/dg/provisioned-concurrency.html> |
| Fri | - Final code cleanup: remove console.log statements, unused imports, and dead code branches <br> - Run full verification suite: `npm run build`, `npm run typecheck`, `npm run lint`, `npm test` — all passing green | 26/06/2026 | 26/06/2026 | <https://eslint.org/docs/> |

### Week 10 Achievements:

* **Scoring Bug Fix**: Corrected partial scoring logic for multiple-answer Reading questions that was undercounting correct responses.
* **Upload Error Handling**: Added proper error boundaries and user notifications for oversized file uploads exceeding the 5MB S3 limit.
* **Security Hardening**: Implemented input validation, rate limiting, and confirmed parameterized queries across all API endpoints.
* **Cold Start Optimization**: Reduced Lambda cold start times by ~40% through dependency tree-shaking and provisioned concurrency on critical handlers.
* **Asset Optimization**: Compressed all exam images via Sharp, reducing average image size by 60% and improving page load times.
* **Database Performance**: Added strategic indexes, reducing average query times for exam session lookups from ~200ms to ~15ms.
* **Clean Codebase**: All build, lint, typecheck, and test commands passing green with zero warnings.
