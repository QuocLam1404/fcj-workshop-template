---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

# WEEK 9 WORKLOG

### Week 9 Objectives:

* Deploy the complete LingoRise platform to the AWS production environment using SAM and Amplify.
* Configure production environment variables, secrets management, and database migrations on Amazon RDS.
* Set up CloudFront CDN distribution for frontend static assets and S3 media delivery.
* Run production smoke tests to validate all critical user flows end-to-end on live infrastructure.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Prepare the SAM `template.yaml` for production: configure Lambda function memory, timeout, and environment variables <br> - Run `sam build && sam deploy --guided` to provision all backend Lambda functions and API Gateway endpoints | 15/06/2026 | 15/06/2026 | <https://docs.aws.amazon.com/serverless-application-model/> |
| Tue | - Deploy the Next.js frontend to AWS Amplify Hosting with custom domain configuration <br> - Debug and fix environment variable mismatches between local development and Amplify build settings (API base URL, Cognito pool IDs) | 16/06/2026 | 16/06/2026 | <https://docs.aws.amazon.com/amplify/> |
| Thu | - Create CloudFront distribution for S3 bucket serving exam images and audio assets <br> - Configure Origin Access Control (OAC) to keep the S3 bucket private while serving content through CloudFront <br> - Set cache behaviors and TTL policies for different asset types | 18/06/2026 | 18/06/2026 | <https://docs.aws.amazon.com/cloudfront/> |
| Fri | - Run production smoke tests: register new account → create exam session → submit answers → view results <br> - Fix a CORS misconfiguration on API Gateway that blocked frontend requests from the Amplify domain <br> - Verify Cognito authentication flow works correctly in production | 19/06/2026 | 19/06/2026 | <https://docs.aws.amazon.com/apigateway/> |

### Week 9 Achievements:

* **Production Backend Live**: Successfully deployed all Lambda functions and API Gateway routes via SAM, with correct environment variable bindings.
* **Frontend Hosting**: Deployed Next.js frontend on AWS Amplify with automated CI/CD builds on Git push.
* **Database Production-Ready**: Migrated all schemas to production RDS, verified data integrity and seeded essential reference data.
* **CDN Asset Delivery**: Configured CloudFront with OAC to securely deliver exam images and audio files from private S3 buckets.
* **CORS Fix**: Resolved a production-only CORS issue where API Gateway rejected requests from the Amplify-hosted frontend domain.
* **End-to-End Validation**: Confirmed the complete learner flow (register → exam → score → review) works on live AWS infrastructure.
