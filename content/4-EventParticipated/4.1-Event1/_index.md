---
title: "Event 1: AWS First Cloud AI Journey — Community Day"
date: 2026-05-23
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# AWS First Cloud AI Journey — Community Day

### Event Details
| | |
|---|---|
| **Event Name** | AWS First Cloud AI Journey — Community Day |
| **Date** | 23/05/2026 |
| **Location** | 26th Floor, Bitexco Financial Tower, 2 Hai Trieu Street, Ben Nghe Ward, District 1, Ho Chi Minh City |
| **Organizer** | AWS Study Group |
| **Role** | Participant / Intern |

![AWS First Cloud AI Journey — Community Day](/images/event_1.jpg)

### Event Description
The **AWS First Cloud AI Journey — Community Day** was a tech conference hosted at Bitexco Financial Tower in Ho Chi Minh City. The event brought together leading experts, Cloud Architects, GenAI Engineers, and DevOps professionals to share real-world experiences, architecture patterns, and strategies of deploying GenAI, DevOps, and Platform Engineering solutions on AWS.

### Key Highlights
- **GenAI Applications in Enterprise**: Speakers from VIB and VPBank discussed how Generative AI models are being leveraged in banking systems to streamline business analysis and automate customer support.
- **DevOps & Platform Engineering**: Engineers from FCAJ and GoTymeX shared insights into building platform engineering layers and optimizing serverless deployment pipelines on AWS.
- **Cloud Consulting & Architecture**: Experts from G-AsiaPacific and Cloud Kinetics highlighted architectural design patterns for scalable, highly available enterprise workloads.

### Featured Presentation: "Context Is Everything — Making AI Actually Work for You"
Presented by **Tinh Truong** (Platform Engineer, GoTymeX), this session explored the vital role of context in working with Large Language Models (LLMs).

#### Key Concepts Shared:
1. **Why AI Fails Without Context**: While modern AI models are extremely powerful, they fail when input instructions are weak or lack situational awareness.
2. **What "Context" Actually Means**: The information that helps AI understand the "task behind the task." It is composed of:
   - **Your Goal**: The desired outcome.
   - **Your Situation**: Background (e.g., student project, deadline).
   - **Your Constraints**: Tech stack, coding style, budget, format.
   - **Relevant Evidence**: Code blocks, documentation, requirements.
   - *Core Takeaway*: "Context turns a vague request into a solvable task."
3. **Common Mistakes (The "Internet Puller" Problem)**:
   - *Bad Habit*: Blindly copying entire articles, PDFs, and endless screenshots into a single chat window.
   - *Impact*: Irrelevant text distracts the model, accuracy drops as the signal gets buried in noise, and token costs spike.
   - *Core Takeaway*: "More context is not always better context."
4. **Second AI Brain Case Study (Context + Memory)**:
   - Emphasized building a "Second AI Brain" that remembers learning progress, understands project goals, and dynamically retrieves the right context before answering.
   - *Core Takeaway*: "A Second AI Brain is not magic. It is context + memory done correctly."


### Featured Presentation: "GenAI-Powered Auto Audit for AWS Workload"
Presented by **Pham Nguyen Hai Anh** (Cloud Consultant at G-AsiaPacific Vietnam, AWS Community Builder - Security), this session focused on using GenAI assistants to automate workload auditing and solve daily pain points for business and security teams.

#### Key Concepts Shared:
1. **Business User Pain Points**: Highlighting the struggles of typical business users who must manually gather and analyze information from multiple scattered sources, consult experts for specialized datasets, and repeat the same time-consuming routines.
2. **Amazon Q Business (Quick Suite)**: Explored a comprehensive agentic architecture utilizing:
   - **Insights**: Natural language chat and search capabilities.
   - **Agentic BI & Automation**: Interactive dashboards, scenario simulation, and automated workflow triggers (HR, Sales, Support).
   - **Data Connectors**: Over 40 data connectors (databases, Google Workspace, S3) coupled with Bedrock models and secure action calls in third-party apps.
   - **Security & Guardrails**: Integrated access controls and regulatory compliance filters.
3. **Use Case - PM Assistant**: Showcased how generative agents can automate PM tasks: drafting Minutes of Meeting (MoM) from recording transcripts, notifying stakeholders via email, and scheduling follow-up sessions.
4. **Automated Security Auditing**: Demonstrated how to leverage LLMs to automatically run security audits, verify compliance status, and flags vulnerabilities on AWS infrastructure.


### Featured Presentation: "From Edge to Origin: CloudFront as Your Foundation"
Presented by **Nguyen Tuan Thinh** (DevOps Engineer, First Cloud AI Journey), this session explored the role of Amazon CloudFront as a foundational delivery layer, as well as the billing challenges and financial risks associated with cloud CDN deployments.

#### Key Concepts Shared:
1. **Edge-to-Origin Foundation**: Leveraging CloudFront as the first line of defense to serve static/dynamic assets from global edge locations, minimizing latency to the end users.
2. **The Pay-As-You-Go Billing Paradox**: While AWS offers a generous 1TB CloudFront Free Tier (ideal for small projects starting at $0), pay-as-you-go billing introduces several operational challenges:
   - **Cost Estimation**: Predicting monthly cloud costs is difficult due to variable traffic patterns.
   - **Traffic Volatility**: Going viral or encountering unexpected usage spikes can lead to sudden billing spikes.
   - **Financial Risks**: Extreme cases (like large-scale DDoS attacks or misconfigured assets) can result in unexpected bills of up to $100K+, creating critical business risks for founders.
3. **Addressing Customer Concerns**: Solved common fears regarding CDN deployments, such as forecasting monthly budgets, protecting origins from malicious traffic, and avoiding complex billing structures.
4. **Best Practices**: The importance of setting up CloudWatch Billing Alerts, deploying AWS WAF to block attack traffic, and tuning TTL settings to optimize cache ratios.


### Featured Presentation: "36 hrs with LotusHacks: Building UTMorpho from Idea to Reality"
Presented by **Team VIB** (representing VIB GenAI and software engineers), this session shared their high-pressure experience participating in the 36-hour LotusHacks hackathon to build and launch a working prototype of a product called **UTMorpho**.

#### Key Concepts Shared:
1. **The Brainstorming Journey**: Moving from "Hour 0" with a blank mind, to analyzing friction in daily workflows during the opening day, leading to the clear identification of the problem and the birth of UTMorpho.
2. **The 36-Hour Hackathon Sprint**: A structured methodology for rapid product delivery under immense time pressure:
   - **Setup & Alignment**: Aligning the team on the scope of the Minimum Viable Product (MVP).
   - **First Slice**: Defining the core architecture, data schemas, and API boundaries.
   - **Building the Core**: High-speed, parallel development of core features.
   - **The Hard Middle**: Resolving unexpected bugs and integration issues midway.
   - **Integration & Polish**: Merging frontend and backend components and finalizing the UI.
   - **Submit & Pitch**: Preparing the demo script and pitching the product value to the evaluation board.
3. **Key Learnings**: Focus on rapid prototyping, managing technical debt dynamically, maintaining team alignment, and focusing on a single solvable problem rather than feature bloat.


### Featured Presentation: "Non-Determinism of 'Deterministic' LLM Settings"
Presented by **Duc Dao** (Solution Architect - Cloud Kinetics), this session explored the hidden mechanics of token selection, LLM sampling settings, and why setting Temperature = 0 does not guarantee deterministic model outputs.

#### Key Concepts Shared:
1. **Token Generation Mechanics**: LLMs generate text token by token. At each step, the model calculates logits (scores) for every word in its vocabulary, converts them to probabilities via softmax, and samples the next token from that distribution.
2. **The Role of Temperature**: Temperature scales logit distribution. While high temperatures increase randomness, setting Temperature to 0 *theoretically* forces the model to perform argmax selection (always picking the token with the absolute highest probability) for consistent results.
3. **The Determinism Paradox**: In practice, setting Temperature = 0 on GPUs still leads to non-deterministic outputs. This is caused by:
   - **GPU Parallelization**: Floating-point rounding errors are non-associative; running parallel GPU threads changes calculation order, subtly altering probability distributions.
   - **API Layer Inconsistencies**: Server load balancing and minor hardware variations at hosting providers introduce drift.
4. **Mitigation Strategies**: Using strict JSON validation schemas, configuring system prompts with high structural constraints, leveraging seeding parameters, and building robust backend retry parsers.


### Featured Presentation: "Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring"
Presented by **Vy Lam** (Senior Business Systems Analyst, VPBank), this session analyzed the structural challenges of banking credit evaluations for startups and how a multi-agent AI architecture solves the limitations of single-agent models.

#### Key Concepts Shared:
1. **The Structural Mismatch**: Traditional bank credit scoring requires 3+ years of financial history, collateral, and stable revenue. Startups—with 6-18 months of operation, unstructured data, and assets tied to intellectual property (IP) and traction—are routinely rejected because they don't fit the rigid data models of banks.
2. **The Single Agent Problem**: Using a single AI agent for credit decisions has critical limits: context window limitations, dilution of domain expertise, lack of checks and balances, and a single point of failure.
3. **Multi-Agent Paradigm**: Proposed a "Virtual Credit Committee" blueprint, decoupling the evaluation into a collaborative group of specialized agents (financial analyst, IP evaluator, risk auditor) coordinating under a central agent layer.
4. **Enterprise-Grade Governance**: Hardening LLM workloads across five architectural layers:
   - *Perimeter*: WAF, DDoS protection, and rate limiting.
   - *Network*: VPC, private links (PrivateLink), security groups.
   - *Identity*: IAM, Cognito, role-based access control (RBAC), and MFA.
   - *Application*: Input validation, prompt injection prevention, and output filtering.
   - *Data*: Encryption at rest/in transit and immutable audit logging.

### Key Takeaways
- **Context is Key**: I realized that providing clean, targeted context to AI models yields significantly better code generation.
- **Multi-Agent Systems vs. Single Agents**: Understood the necessity of decoupling monolithic AI systems into specialized task-oriented agents, matching how we split LingoRise's AI logic between the exam generator (text parsing) and the writing assessor (four-criteria grading).
- **Enterprise Security Hardening**: Learned how to secure API boundaries, enforce rate limiting, and protect against prompt injection, which inspired the Week 10 security hardening features I added to LingoRise.
- **LLM Fluctuation Defense**: Duc's presentation on LLM non-determinism explained why our LingoRise AI generator occasionally produced malformed JSON. This highlighted the need for the regex-based `extractJsonObject()` fallback parser I built in Week 5 to handle slight LLM output variations.
- **CDN Security & Budgeting**: Learned the absolute necessity of setting up tight budget alerts and CloudFront Origin Access Control (OAC) to prevent billing spikes on S3 storage.
- **Industry Networking**: Connected directly with cloud mentors and senior engineers, exchanging thoughts on the LingoRise database and payment integration design.
