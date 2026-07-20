---
title: "Proposal"
date: 2026-07-07
weight: 2
chapter: false
pre: " <b> 2. </b> "
---
This section presents the project proposal for **LingoRise** — the capstone product built during the FCAJ Cloud Internship program.

# LingoRise — AI-Powered IELTS & TOEIC Learning Platform

{{% notice info %}}
* **Deployed Website:** [lingorise.xyz](https://www.lingorise.xyz/)
* **Project Demo Video:** [Google Drive Demo Folder](https://drive.google.com/drive/u/0/folders/1p3dhFRWf3rbgyNnlVk-R2KkELfWrA1Ce)
{{% /notice %}}

### 1. Background & Motivation

When I first started my internship at First Cloud Journey, I tried out some popular IELTS and TOEIC prep platforms. I noticed a big issue: almost all of them only have English interfaces, and their subscription fees are way too expensive for students. Plus, none of them tell you which areas you're actually struggling with. Many Vietnamese beginners get frustrated just trying to navigate the website before they even start studying.

That's why I came up with the idea for **LingoRise**—a Vietnamese-first IELTS and TOEIC preparation web app. It features an AI assistant to analyze test attempts and give personalized feedback. Since it runs completely on AWS serverless tech, the operational costs are very low, making it perfect for a student project.

### 2. Problem Analysis

#### Who are the target users?
- Vietnamese university students preparing for IELTS Academic/General or TOEIC certification exams.
- Self-learners who cannot afford expensive prep courses or one-on-one tutoring.
- Educators and content creators who need a centralized tool to manage and distribute exam materials.

#### What specific problems does LingoRise solve?

| Problem | How LingoRise Addresses It |
|---------|---------------------------|
| English-only platforms create barriers for beginners | Vietnamese-first UI with bilingual content throughout |
| Quality exam content is expensive and scattered | Centralized exam bank with AI-assisted question generation from raw markdown sources |
| No personalized feedback on practice performance | AI Writing analysis (task achievement, coherence, grammar, lexical resource), score radar charts, and per-question answer review with AI explanations |
| Manual content creation is slow and error-prone | Admin content pipeline with automated parsing, duplicate detection, and audit logging |
| Payment integration for Vietnamese market is limited | PayOS integration for automated payment verification via dynamic QR code |

### 3. Technical Architecture

LingoRise uses a decoupled architecture where the frontend and backend communicate via REST APIs, with AWS services handling authentication, file storage, and content delivery.

![LingoRise Technical Architecture](/images/2-Proposal/lingorise_architecture.png)

#### Technology Stack
| Layer | Technology | Rationale |
|-------|-----------|-----------|
| **Frontend** | Next.js 15, React 19, TailwindCSS | Server-side rendering for SEO, modern component architecture |
| **Backend** | Express.js on AWS Lambda (via SAM) | Serverless deployment eliminates server management overhead |
| **Database** | Supabase PostgreSQL (External) | Relational integrity for exam scoring, user progress, and transaction records |
| **Authentication** | AWS Cognito (JWT) | Managed user pools with built-in MFA, token refresh, and role-based access |
| **File Storage** | Amazon S3 + CloudFront (OAC) | Private bucket with CDN distribution via Origin Access Control |
| **AI Services** | OpenRouter API | Flexible model routing for exam question generation and writing feedback |
| **Payment** | PayOS webhook (payment automation) | Local Vietnamese payment gateway with dynamic QR code verification |
| **Deployment** | AWS SAM + AWS Amplify | Infrastructure-as-code for backend; managed hosting for frontend |

#### AWS Services Integration
- **AWS Lambda** — Runs the Express backend as a single serverless function, handling all API routes.
- **Amazon API Gateway** — HTTP proxy routing with CORS configuration for the Amplify-hosted frontend.
- **Amazon S3** — Stores exam images, audio pronunciation files, and uploaded documents. Private bucket with no public access.
- **Amazon CloudFront** — CDN with Origin Access Control to serve S3 assets securely without exposing the bucket.
- **Amazon Cognito** — User pool managing learner and admin accounts with JWT-based authentication.
- **AWS Polly** — Generates pronunciation audio for the vocabulary notebook feature.

### 4. Core Features

#### For Learners
| Feature | Description |
|---------|-------------|
| **IELTS/TOEIC Exam Engine** | Full exam simulations with countdown timer, question navigation sidebar, persistent session state (resume mid-exam), and Cambridge band scoring |
| **Score Visualization** | Radar chart (Chart.js) showing band score distribution across Listening, Reading, Writing, and Speaking sections |
| **Answer Review** | Per-question review with color-coded correctness indicators, correct answer display, and AI-generated explanations |
| **AI Writing Feedback** | Structured essay analysis evaluating four IELTS criteria: task achievement, coherence & cohesion, lexical resource, grammatical range |
| **Gap-Fill Question Support** | Dynamic text input rendering via regex parser for fill-in-the-blank questions, with case-insensitive grading |
| **Vocabulary Notebook** | Personal word bank with AWS Polly audio pronunciation and spaced repetition tracking |

#### For Admins
| Feature | Description |
|---------|-------------|
| **AI Exam Generator** | Paste raw markdown exam content; AI parses and structures it into the database question format |
| **Pending Review Dashboard** | Newly generated exams appear on the dashboard home page with one-click Approve/Reject actions |
| **Content Moderation Queue** | Review queue with quality flags and audit log tracking all admin actions |
| **Image Asset Pipeline** | Automated scraper tool downloads external images from copied exam content and uploads them to S3 |
| **PayOS Payment Monitor** | Webhook receiver for QR-based payment verification, displaying transaction status in the admin panel |

### 5. Development Timeline

The development followed a progressive approach, building from AWS infrastructure foundations to feature development, then deployment and hardening:

| Phase | Weeks | Key Activities |
|-------|-------|----------------|
| **AWS Foundation** | 1–2 (20/04–01/05) | Account security (IAM, MFA), S3 encryption policies, network configuration and VPC Security Groups |
| **AI Pair-Programming** | 3 (04/05–08/05) | Consulting AI to design serverless architecture, writing Lambda handlers, prompt engineering for exam parsing |
| **Admin Portal** | 4 (11/05–15/05) | Admin dashboard UI, RBAC middleware, content review queue, database audit logging |
| **Payment & AI Exams** | 5 (18/05–22/05) | PayOS webhook integration, AI question bank generator from markdown, JSON extraction regex parser |
| **Bug Fixing — Exams** | 6 (25/05–29/05) | Missing Reading images (S3 scraper pipeline), gap-fill input box rendering, case-insensitive grading, exam generation logic |
| **AI Speed & Moderation** | 7 (01/06–05/06) | Async job queue for AI generation, dashboard pending review widget, one-click moderation actions |
| **Frontend Polish** | 8 (08/06–12/06) | Score visualization charts, answer review screens, Cognito token refresh fix, responsive mobile UI, AI Writing feedback |
| **Production Deployment** | 9 (15/06–19/06) | SAM deploy to AWS, Amplify hosting, Supabase migration, CloudFront CDN setup, CORS fix, smoke testing |
| **Hardening** | 10 (22/06–26/06) | Scoring bug fixes, input validation, rate limiting, Lambda cold start optimization, image compression, database indexing |
| **Beta & Documentation** | 11–12 (29/06–10/07) | User feedback collection, UX refinements, internship report website, final submission |

### 6. Budget Estimation

All services operate within or near the AWS Free Tier, making the project sustainable for a student:

| Service | Monthly Cost | Notes |
|---------|-------------|-------|
| AWS Lambda | ~$0.00 | Free tier covers 1M requests/month |
| Amazon S3 | ~$0.23 | Exam images and audio files |
| Amazon CloudFront | ~$0.10 | CDN distribution with OAC |
| Amazon Cognito | ~$0.00 | Free tier for <50,000 users |
| Supabase PostgreSQL | ~$0.00 | Free tier supports all required DB capabilities |
| AWS Polly | ~$4.00 | Pay-per-character for vocabulary audio |
| OpenRouter AI API | ~$5.00 | Exam generation and writing feedback |
| **Total** | **~$9.33/month** | |

### 7. Risk Assessment & Mitigations

| Risk | Impact | Mitigation Applied |
|------|--------|---------------------|
| AI generation speed fluctuations causing timeouts | High | Moved to async background job queue (BullMQ); instant response with job tracking ID |
| Missing images in copied exam content | Medium | Built automated Node.js scraper to download and re-host assets on S3 |
| Cognito token expiry during exams | High | Implemented Axios interceptor for silent token refresh |
| CORS blocking on production deployment | Medium | Configured explicit origin whitelist on API Gateway for the Amplify domain |
| Lambda cold start latency | Medium | Applied dependency tree-shaking and provisioned concurrency on critical handlers |

### 8. Expected Outcomes

#### Technical Deliverables
- A fully deployed IELTS/TOEIC exam platform on AWS serverless infrastructure.
- AI-powered exam generation pipeline converting raw markdown into structured question banks.
- Admin dashboard with real-time content moderation and one-click approval workflow.
- Responsive mobile-first learner interface with score visualization and AI writing feedback.
- Automated asset management pipeline (image scraping, S3 upload, CloudFront delivery).

#### Learning Outcomes
- Hands-on experience deploying and operating AWS services in a real production environment.
- Full-stack development proficiency with Next.js 15, Express, TypeScript, and Supabase PostgreSQL.
- Problem-solving skills for real-world bugs: token management, CORS, image asset pipelines, and scoring edge cases.
- AI integration experience: prompt engineering, JSON extraction, async job processing, and writing analysis.