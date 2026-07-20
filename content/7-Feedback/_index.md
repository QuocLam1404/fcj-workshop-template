---
title: "Sharing and Feedback"
date: 2026-07-07
weight: 7
chapter: false
pre: " <b> 7. </b> "
---
# Sharing and Feedback

## Feedback on the FCAJ Internship Program

### What I Liked (From a Beginner's Perspective)
1. **Foundation-to-Advanced Roadmap:** The 4-week AWS core services foundation was an invaluable ramp-up for a newbie like me. Progressing from simple standalone services (EC2, S3, Lambda) to fully integrated serverless stacks prevented me from feeling overwhelmed by AWS's vast ecosystem.
2. **Project-Driven Learning:** Deploying **LingoRise** on real cloud infrastructure taught me first-hand the actual operational challenges a Cloud Engineer solves daily: data security, access control, CDN caching, and database connectivity.
3. **Professional English Environment:** Being required to write all documentation in English was initially challenging but helped me adopt global technical standards and made reading official AWS documentation much easier.
4. **Mentor Guidance:** The mentor patiently explained cloud architecture design patterns and taught safe deployment practices to a beginner in the industry.

### Suggestions for Improvement
1. **Troubleshooting & Debugging Workshops:** For beginners, diagnosing VPC configurations, NAT Gateway routing issues, or CORS errors is extremely difficult. Having dedicated workshops to walk through these common debugging scenarios would be highly beneficial.
2. **Infrastructure Code Reviews:** Standardized reviews of AWS SAM/Terraform configurations to learn how to write production-grade templates and avoid technical debt early on.

---

## Sharing with Future Interns

### Tips for Success (For Newbie Cloud Builders)

**Week 1–4 (Foundation Phase):**
- **Don't just click, write CLI commands:** Avoid doing everything in the AWS Console. Get comfortable typing commands with the AWS CLI; muscle memory is key to retaining knowledge.
- **Document error logs from Day 1:** Errors are a Cloud Engineer's greatest teacher. Write down your deployment errors and how you resolved them in your worklog.

**Week 5–9 (Project Phase):**
- **Leverage official documentation (AWS Docs) and StackOverflow:** When you hit complicated SAM YAML deploy errors or overlapping IAM permission blocks, don't guess in the dark. Search error codes in official AWS documentation or developer communities to understand the underlying mechanics and find solutions.
- **Deploy the core first:** Don't try to build a massive system on day one. Focus on getting a basic API Gateway-to-Lambda-to-RDS flow working first, then layer on security controls like WAF, Cognito, and CloudFront.

**Week 10–12 (Reporting Phase):**
- **Invest in your Portfolio:** This internship report website is your permanent portfolio. Spend time making it look clear and professional to demonstrate how much you've grown.

### Essential Tools for a Newbie Cloud Engineer
| Tool | Why |
|------|-----|
| **AWS SAM CLI** | A fantastic entryway into Infrastructure as Code (IaC), making deployments repeatable and structured. |
| **CloudWatch Logs** | A must-use tool for monitoring your serverless resources and hunting down runtime errors. |


