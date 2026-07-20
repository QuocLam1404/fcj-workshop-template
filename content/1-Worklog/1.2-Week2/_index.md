---
title: "Week 2 Worklog"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

# WEEK 2 WORKLOG

### Week 2 Objectives:

* Implement advanced identity controls and secure cross-service access using IAM Roles.
* Construct a resilient storage architecture using Amazon S3 with lifecycle management and bucket security policies.
* Evaluate and deploy relational databases (RDS PostgreSQL) and key-value stores (DynamoDB) for structured data.
* Establish secure VPC connection pathways between computation nodes (EC2) and database servers.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Configure Amazon S3 properties: Implement default server-side encryption <br> - Configure object versioning to prevent accidental deletions <br> - Write custom Bucket Policies to restrict access to trusted source IPs | 27/04/2026 | 27/04/2026 | <https://docs.aws.amazon.com/AmazonS3/latest/userguide/> |
| Wed | - Deep dive into AWS IAM policies: Create custom JSON policy documents <br> - Create IAM Roles for EC2 service execution <br> - Disable access keys for daily work and shift to role-based access control | 29/04/2026 | 29/04/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/> |
| Thu | - Establish a connectivity bridge: Configure network security groups to allow traffic only from web subnets to RDS database ports <br> - Mount S3 SDK endpoints inside application logic on EC2 | 30/04/2026 | 30/04/2026 | <https://docs.aws.amazon.com/vpc/> |

### Week 2 Achievements:

* **Advanced Data Protection**: Configured S3 bucket security with policy controls, object versioning, and transit encryption.
* **Dual Database Experience**: Gained practical experience setting up relational (RDS) and non-relational (DynamoDB) databases, understanding their pricing and usage differences.
* **Credential-less EC2 Security**: Eliminated security risks by attaching IAM Roles to EC2 instances using Instance Profiles, allowing secure API calls to S3.
* **Secure Network Integration**: Established secure database access using VPC Security Groups, locking down traffic to private subnets.
* **Architecture Integration**: Successfully validated the EC2-RDS-S3 connection loop, proving system stability.
