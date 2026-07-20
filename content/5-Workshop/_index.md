---
title : "Workshop"
date : 2026-07-07
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

# Deploying LingoRise — A Serverless English-Learning Platform on AWS

#### Overview

LingoRise is an IELTS/English-learning web application that helps learners practice reading, writing, listening, and speaking with AI-assisted grading and exam simulation. In this workshop you will deploy the entire platform on AWS using a serverless-first architecture.

The backend runs on **AWS Lambda (Node.js 20)** behind **Amazon API Gateway (REST)**, with authentication handled by **Amazon Cognito**. Application data lives in **Supabase PostgreSQL** (external cloud relational database), while static assets are stored in **Amazon S3** and served through **Amazon CloudFront**. The frontend is hosted on **AWS Amplify Hosting**, application secrets are kept in **AWS Systems Manager (SSM) Parameter Store**, and observability is provided by **Amazon CloudWatch**. Everything is packaged and shipped with **AWS SAM** (Serverless Application Model).

By the end of this workshop you will have a working, publicly reachable deployment of LingoRise running in the **ap-southeast-1** region under the **dev** stage, with the SAM stack named **lingorise-dev**. You will integrate the Supabase database, load secrets, deploy the API, publish the frontend, wire up asset delivery, run a smoke test, and finally clean everything up.

Because the architecture is serverless, you gain real benefits over a traditional server setup:

- **Pay-per-use** — you are billed for requests and compute time actually consumed, not for idle servers.
- **No servers to manage** — no patching, no capacity planning for the compute layer; AWS operates the runtime.
- **Scales to zero and beyond** — Lambda scales down to nothing when idle and scales out automatically under load.

![LingoRise serverless architecture on AWS](/images/lingorise_architecture.png)

#### Architecture

The deployment uses the following services and resources:

- **AWS Lambda (Node.js 20)** — runs the LingoRise API business logic.
- **Amazon API Gateway (REST)** — public HTTPS entry point that routes requests to Lambda.
- **Amazon Cognito** — user sign-up, sign-in, and JWT-based authorization.
- **Supabase PostgreSQL** — external relational cloud database hosting the primary application tables.
- **Amazon S3** — asset storage (bucket `lingorise-assets-dev-<accountId>`).
- **Amazon CloudFront** — CDN in front of S3 for fast, cached asset delivery.
- **AWS Amplify Hosting** — builds and serves the frontend web application.
- **AWS Systems Manager (SSM) Parameter Store** — application configuration and secrets under `/lingorise/dev/`.
- **Amazon CloudWatch** — logs and metrics for Lambda and the rest of the stack.
- **AWS SAM** — infrastructure-as-code for packaging and deploying the backend.

#### Content

1. [Introduction & Architecture](5.1-introduction/)
2. [Prerequisites](5.2-prerequisites/)
3. [Secrets & SSM Parameter Store](5.3-secrets-ssm/)
4. [Database — RDS PostgreSQL](5.4-database-rds/)
5. [Backend — AWS SAM Deploy](5.5-backend-sam/)
6. [Frontend — AWS Amplify Hosting](5.6-frontend-amplify/)
7. [Storage & CloudFront (Bonus)](5.7-storage-cloudfront/)
8. [Smoke Test & Operations](5.8-smoke-test/)
9. [Clean up](5.9-cleanup/)