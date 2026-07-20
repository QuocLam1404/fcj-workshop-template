---
title: "Week 8 Worklog"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

# WEEK 8 WORKLOG

### Week 8 Objectives:

* Polish the learner-facing exam flow: implement exam result score visualization with charts and detailed answer review screens.
* Build responsive mobile-first layouts for all exam and learning pages to ensure cross-device compatibility.
* Resolve Cognito session management issues: token expiry mid-exam causing data loss, and implement auto-refresh middleware.
* Integrate the Writing feedback AI module into the exam submission pipeline.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Design and implement the exam result summary page with score breakdown by section (Listening/Reading/Writing/Speaking) <br> - Integrate Chart.js radar chart component to visualize band score distribution | 08/06/2026 | 08/06/2026 | <https://www.chartjs.org/docs/> |
| Wed | - Fix Cognito token expiry bug: learners losing exam progress when the access token expires mid-session <br> - Implement a silent token refresh interceptor in the Axios HTTP client to auto-renew tokens before API calls fail | 10/06/2026 | 10/06/2026 | <https://docs.aws.amazon.com/cognito/> |
| Fri | - Connect the AI Writing feedback module: submit learner essays to the AI analysis endpoint and render structured feedback (task achievement, coherence, lexical resource, grammar) <br> - End-to-end testing of the full exam lifecycle on both desktop and mobile browsers | 12/06/2026 | 12/06/2026 | <https://nextjs.org/docs/> |

### Week 8 Achievements:

* **Exam Result Visualization**: Built a comprehensive result summary page with radar charts showing band score distribution across IELTS sections.
* **Answer Review Screen**: Implemented a detailed question-by-question review with color-coded correctness and AI explanations.
* **Cognito Token Fix**: Resolved a critical bug where learners lost exam progress due to token expiry, by implementing an Axios interceptor for silent token refresh.
* **Mobile-First Responsive UI**: Converted all learner-facing pages to mobile-responsive layouts, fixing touch navigation issues on the exam sidebar.
* **AI Writing Feedback Integration**: Connected the Writing analysis AI module, providing structured IELTS-criteria feedback on essay submissions.
