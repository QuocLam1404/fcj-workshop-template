---
title: "Full-stack Development — Backend Services, Frontend UI & Database"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

# WEEK 7 WORKLOG

### Week 7 Objectives:

* Optimize the AI-assisted exam generation performance, fixing issues causing fluctuating generation speeds and timeouts.
* Implement an asynchronous queue-based architecture for AI generation calls.
* Refactor the admin dashboard landing page to show newly generated exams and streamline the post-creation review and moderation logic.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Tue | - Re-engineer the AI generator loop into an asynchronous background worker using BullMQ <br> - Enable instant client responses with a job ID for tracking generation progress | 02/06/2026 | 02/06/2026 | <https://nodejs.org/api/> |
| Wed | - Optimize prompt structures and token counts, testing response speeds <br> - Establish a caching layer for static exam templates to ensure consistent generation time | 03/06/2026 | 03/06/2026 | <https://redis.io/documentation> |
| Thu | - Redesign the admin dashboard home page layout to display newly generated exams in a "Pending Review" queue immediately after creation | 04/06/2026 | 04/06/2026 | <https://nextjs.org/docs/> |
| Fri | - Implement instant action buttons (Approve/Reject) on the dashboard home page to bypass deep menus <br> - Test the modified moderation workflow and run integration tests | 05/06/2026 | 05/06/2026 | <https://playwright.dev/> |

### Week 7 Achievements:

* **Optimized AI Generation Speed**: Fixed the fluctuating response speed issue by shifting to an async background job architecture with prompt context optimizations.
* **Dashboard Review Pipeline**: Redesigned the admin dashboard home page to list recently created exams for immediate action.
* **Direct Moderation Logic**: Built a direct approval/rejection logic on the home page, reducing steps to publish new exams from 5 screens to 1 click.
* **Decoupled Job Queue**: Implemented background queues to prevent request timeouts, ensuring system reliability during heavy AI loads.
* **Robust Database Integration**: Connected the dashboard moderation actions to PostgreSQL with transaction-wrapped state mutations.
