---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

# WEEK 4 WORKLOG

### Week 4 Objectives:

* Design and implement the administrator dashboard for the LingoRise platform, focusing on content operations and audit logging.
* Integrate backend RBAC checks to secure admin-only routes.
* Set up the question verification and approval queues (`/admin/content-operations`) with AI-assisted grading feedback.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Tue | - Implement Backend Role-Based Access Control (RBAC) middleware in Express <br> - Verify session tokens and roles before allowing access to admin resources | 12/05/2026 | 12/05/2026 | <https://expressjs.com/> |
| Wed | - Create the Audit Logging database schema and integration service in PostgreSQL <br> - Write middleware that logs all post/put/delete operations performed by admins | 13/05/2026 | 13/05/2026 | <https://www.postgresql.org/docs/> |
| Fri | - Conduct end-to-end testing of the admin dashboard mutations <br> - Verify audit logs are recorded correctly in the DB and secure all endpoint tests | 15/05/2026 | 15/05/2026 | <https://playwright.dev/> |

### Week 4 Achievements:

* **Admin UI Implementation**: Designed a premium dashboard interface using Next.js to manage large-scale question pools and passage sets.
* **Robust Access Control**: Implemented route guards and Express middleware to prevent unauthorized escalation of privileges (RBAC validation).
* **Immutable Audit Trail**: Integrated a secure audit logging mechanism tracking all administrator actions in PostgreSQL database records.
* **AI-Enhanced Content Verification**: Built the review queue interface to process AI quality diagnostics (identifying bad options, incorrect answer keys).
* **Verified Security**: Successfully completed testing for unauthorized API requests, ensuring solid protection on all administrative routes.
