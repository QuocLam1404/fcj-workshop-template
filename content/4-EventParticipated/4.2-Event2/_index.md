---
title: "Event 2: AWS First Cloud AI Journey — MNC Career & Culture Sharing Seminar"
date: 2026-06-13
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# AWS First Cloud AI Journey — MNC Career & Culture Sharing Seminar

### Event Details
| | |
|---|---|
| **Event Name** | AWS First Cloud AI Journey — MNC Career & Culture Sharing Seminar |
| **Date** | 13/06/2026 |
| **Location** | 26th Floor, Bitexco Financial Tower, 2 Hai Trieu Street, Ben Nghe Ward, District 1, Ho Chi Minh City |
| **Organizer** | AWS Study Group |
| **Role** | Participant / Intern |

### Event Description
The **MNC Career & Culture Sharing Seminar** was a corporate mentoring event organized by the AWS Study Group at Bitexco Financial Tower. The seminar aimed to bridge the gap between academic learning and industry realities by bringing seasoned professionals to share practical experiences about career paths, workspace culture, and essential skill sets in multinational corporations (MNCs) and high-growth startups.

### Topic 1: "Real Stories to Corporate Culture in Multinational Corporations"
Presented by **Mr. Dat Pham** (Data Analytics Engineer) and **Mr. Cuong Nguyen** (Process Engineer), this session focused on real-world engineering responsibilities, career growth mindsets, and key technical/soft skills required in modern enterprises.

#### 1. Job Functions in Different Business Domains:
The speakers contrasted the responsibilities of a Data Analytics Engineer across two different organizational models:
*   **Kamereo (Fast-growing Startup)**:
    *   Building daily, weekly, monthly, and quarterly reports to track operational performance.
    *   Designing management dashboards to monitor data trends, detect anomalies, and aid real-time decision-making.
    *   Analyzing business/operational metrics to identify root causes of problems and propose solutions.
    *   Collaborating with cross-functional departments to resolve live issues.
*   **Colgate-Palmolive (Multinational Manufacturing)**:
    *   Participating in machinery data projects, operations, and designing IoT equipment inside production plants.
    *   Identifying opportunities to optimize production costs and improve factory efficiency.
    *   Supporting enterprise digital transformation initiatives.
    *   Building data-driven, long-term operational solutions for factories.

#### 2. Essential Skill Set:
*   **Critical Thinking**: Objectively analyzing data and information to make logical judgments.
*   **Communication Skills**: Translating complex data insights into clear, understandable messages for diverse audiences.
*   **Data Storytelling**: Turning dry statistics and numbers into meaningful narratives that drive business action.
*   **Problem Solving**: Finding optimal solutions to business challenges by leveraging data foundations.

#### 3. Career Development Mindset (The 3 Phases):
The presenters shared a personal growth framework used to navigate career stages:
*   **Phase 1: Follower (Executor)**: The entry-level stage (Interns / fresh Juniors). Relies on step-by-step guidance from senior colleagues, focusing on building foundational skills and adapting to the work environment.
*   **Phase 2: Learner (Active Learner)**: Understands solution options but still requires mentorship. Focuses on fast learning and asking deep, constructive questions.
*   **Phase 3: Problem Solver**: The milestone stage. No longer working strictly off checklists. Actively analyzes deep business challenges, proposes optimal solutions, and takes ownership of output quality.

#### 4. Corporate Culture in MNCs:
An overview of collaboration, compliance, communication frameworks, and cultural dynamics when working in large multinational environments.


### Topic 2: "DevOps Landscape & Role: What does a DevOps Engineer really do?"
Presented by **Trong H. Truong** (DevOps Engineer @ Endava Vietnam), this session demystified the actual responsibilities of DevOps engineers, the contextual factors shaping their scope, and the vast lifecycle tool landscape.

#### 1. The Perception vs. Reality Gap:
The speaker addressed common misconceptions about the role:
*   *Perception*: Simply writing CI/CD pipelines, administering Docker/Kubernetes, deploying code, or acting as the "person who fixes production at midnight."
*   *Reality*: DevOps is a strategic methodology focused on improving software delivery velocity, system reliability, and collaboration between development and operations.

#### 2. Scope Dependent on Context:
A DevOps engineer's daily scope is not one-size-fits-all but depends heavily on:
*   Company and project size, team structures, and product complexity.
*   The cloud infrastructure maturity level and existing automation.
*   Production support ownership models and platform/SRE/security structures.

#### 3. The DevOps Tool Landscape:
The presentation mapped out the tools essential for the 10 phases of the DevOps lifecycle:
*   **Plan & Code**: Tools for collaboration and source control (Jira, Git, GitHub).
*   **Build & Test**: Continuous Integration systems (Jenkins, GitLab CI, GitHub Actions) and package registries (npm, NuGet, Docker Hub).
*   **Release & Deploy**: Infrastructure as Code (AWS CDK, Terraform, Pulumi) and Configuration Management (Ansible, Chef).
*   **Operate & Monitor**: Container orchestration (Docker, Kubernetes), Cloud providers (AWS, Azure, GCP), and observability suites (Datadog, Prometheus, logging/tracing).
*   **Security (DevSecOps) & Platform Engineering**: Integrating vulnerability scanning (SonarQube, Wiz), vault management, and developer experience platforms.


### Topic 3: "From First Cloud AI Journey to AWS Partner"
Presented by **Danh Hoang Hieu Nghi** (AI Engineer, AWS Community Builder, and AWS Student Builder Group Leader), this presentation detailed a structured pathway from student explorer to professional cloud engineering and active community leadership.

#### 1. The 8-Step Career Growth Loop:
The speaker outlined the evolution of a cloud builder's career:
1.  **Student Curiosity**: Starting with curiosity and asking fundamental tech questions.
2.  **First Cloud Journey**: Finding the right environment and bootcamp sandboxes.
3.  **Workshop & Community**: Actively learning from peers and participating in workshops.
4.  **Hands-on Labs**: Gaining practical experience by building on the cloud.
5.  **School/Personal Projects**: Applying learned concepts to real-world projects.
6.  **Portfolio**: Designing a clean showcase of projects and code repositories to demonstrate capability.
7.  **AWS Partner**: Landing professional roles and solving complex client problems for AWS partners.
8.  **Share Back**: Giving back by mentoring the next generation of cloud builders.

#### 2. Landing the Job is Just the Beginning:
He emphasized that entering the field is just the start of specialization. Cloud builders can grow into diverse specializations: Solutions Architect, Head of Solutions Architect, DevOps Engineer, Platform Engineer, or Software Engineer.

#### 3. AWS Student Builder Community & Benefits:
The presentation highlighted the benefits, badges, and rewards available for active students:
*   **Leader & Core Team Badges**: Licenses and credential perks.
*   **AWS Credits**: Accumulating AWS credits (ranging from $25 up to $500 across events) to fund testing and personal project deployments.
*   **AWS Certification Vouchers**: Vouchers awarded for leading events and demonstrating active participation, lowering financial barriers to official certifications.


### Topic 4: "A Scalable URL Shortening Service on AWS"
Presented by **Dinh Trung Kien** and **Nguyen Minh Tho**, this session broke down the system design, deployment architecture, and optimization strategies for building a high-concurrency URL shortener on AWS.

#### 1. System Design Fundamentals:
*   An URL shortener takes a long URL (e.g., product page URL) and maps it into a short code (e.g., `https://a.co/d/00Ayvqgl`).
*   Core flow: User requests redirection -> Server reads short code from database -> Server performs HTTP 301/302 redirect to the target long URL.

#### 2. Infrastructure Architecture Overview:
Deploying for scalability and fault tolerance:
*   **Routing & Security**: Route 53 routes incoming traffic through Amazon CloudFront and AWS WAF for low latency caching and perimeter security.
*   **UI Hosting**: Static frontend hosted on AWS Amplify.
*   **API Layer**: Application logic run on Spring Boot containers using AWS Fargate (ECS) inside a VPC across multiple Availability Zones, behind an Application Load Balancer (ALB).
*   **Storage & Cache**: Amazon DynamoDB acts as the persistent store for URL mappings. Amazon ElastiCache for Redis is deployed in private subnets across two AZs to cache mapping records and reduce read latency.
*   **Security & Encryption**: KMS for encryption, Secrets Manager for database keys, Certificate Manager for HTTPS certificates, and IAM for least-privilege role boundaries.

#### 3. Key Generation Service (KGS) Pattern:
To prevent write bottlenecks and collision issues under massive load, they introduced a **Key Generation Service (KGS)**:
*   KGS runs as a background worker on Amazon ECS, pre-generating unique, non-colliding short strings.
*   These strings are pushed in batches to a Redis queue in Amazon ElastiCache (`LPUSH key_queue`).
*   When a new shortening request arrives, the API backend pops a pre-generated key instantly (`RPOP`), completely avoiding real-time hashing calculation overhead and database lock contentions.

### Key Takeaways
*   **Domain-Driven Analytics**: Understood that technical skills must be mapped to the business domain to create real business value.
*   **Problem-Solver Mindset**: Inspired to transition from a "follower" to a "problem solver" who proactively identifies bugs and proposes optimal fixes, which guided my work on LingoRise.
*   **Pre-computation Strategy (KGS)**: The Key Generation Service design illustrated how pre-computing heavy tasks (like generating keys) and storing them in an in-memory queue can massive optimize write paths. I kept this in mind when designing high-throughput background tasks.
*   **Distributed Caching**: Saw how combining DynamoDB (persistence) and Redis (in-memory cache) provides extremely low-latency lookups, which is a great pattern for high-read platforms.
*   **The Power of Portfolio**: Realized the critical importance of a documented project portfolio, prompting me to meticulously write down the week-by-week progress of LingoRise.
*   **Community Contribution & Learning**: Learned about the resources and vouchers available in the AWS Builder community, motivating me to prepare for my next AWS Associate Certification.
*   **DevOps Tools Mapping**: Gained a clear structural overview of how Infrastructure as Code (IaC) via AWS CDK or Terraform fits into the deploy phase of software release cycles.
*   **Automation is Key**: Understood how automating the release pipeline directly impacts delivery speed, which reinforces why we used AWS SAM to automate resource deployment for LingoRise.
*   **Data Storytelling**: Realized that building a database schema or backend code is only half the battle; presenting its value to stakeholders clearly is just as critical.
