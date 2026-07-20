---
title: "Core Feature Development — Auth, APIs & Database Integration"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

# WEEK 6 WORKLOG

### Week 6 Objectives:

* Troubleshoot and resolve rendering issues where online-scraped IELTS Reading questions lacked diagrams or charts.
* Fix gap-fill rendering bugs to ensure input text boxes display correctly for student answers.
* Design robust case-insensitive grading algorithms and structured exam generation logic.
* Develop an automated asset downloader and storage architecture using Amazon S3 to store images.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Audit copied IELTS Academic Reading questions and trace why diagrams failed to load <br> - Investigate gap-fill rendering bug where blank tokens failed to display input text boxes | 25/05/2026 | 25/05/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html> |
| Tue | - Program a backend downloader service to automatically scrape raw image links inside markdown, fetch the binary files, and re-upload them to a secure Amazon S3 bucket <br> - Write regex-based parsing helper on the frontend to replace custom blank notations with HTML `<input>` elements | 26/05/2026 | 26/05/2026 | <https://nodejs.org/api/> |
| Thu | - Refactor the exam UI parser on the frontend (`lingorise-app`) to convert internal S3 markdown paths into pre-signed S3 links, enabling secure, credential-less image loading <br> - Implement exam generation service on the backend to organize questions, enforce ordering rules, and cache configurations | 28/05/2026 | 28/05/2026 | <https://react.dev/reference/react> |

### Week 6 Achievements:

* **Resolved Broken Reading Images**: Successfully resolved missing diagrams/charts in copied online reading tests by establishing a dedicated image hosting flow.
* **Gap-Fill Input Box Fix**: Restored missing text inputs inside reading passages by implementing a regex parser for gap tokens.
* **Case-Insensitive Grading**: Implemented string normalization algorithms (lowercasing, trimming whitespace) to evaluate student gap-fill responses accurately.
* **Exam Generation Logic**: Programmed backend handlers to dynamically assemble exam objects, structuring sections and sorting questions systematically.
* **S3 Downloader Pipeline**: Coded a Node.js scraper tool that pulls external assets and hosts them inside LingoRise S3 storage automatically.
* **Database Content Fix**: Executed database migration scripts replacing all invalid image URLs with S3 pre-signed references.
* **Secure Frontend Renderers**: Created a customized React markdown wrapper component that renders secure S3 image URLs dynamically.
* **Optimized Layouts**: Corrected responsive image dimensions to ensure stable exam layouts across desktop and mobile screens, avoiding Cumulative Layout Shift (CLS).
