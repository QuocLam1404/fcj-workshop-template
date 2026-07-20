---
title: "Week 12 Worklog"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

# WEEK 12 WORKLOG

### Week 12 Objectives:

* Conduct load and stress testing to evaluate API Gateway and AWS Lambda request handling limits.
* Tune system performance (provisioned resources, database execution costs) based on testing reports.
* Run a comprehensive Security Audit on source code configurations and IAM policies following the principle of least privilege.
* Build and package the release version (v1.0.0) on GitHub, publish the Changelog, and execute final technical handover.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| Mon | - Configure load testing scripts in Artillery/k6 to simulate 500+ concurrent test-submission requests <br> - Measure response latency percentiles on API Gateway | 06/07/2026 | 06/07/2026 | <https://artillery.io/docs/> |
| Tue | - Execute stress testing simulations on the Staging environment <br> - Analyze CloudWatch metrics to monitor Lambda execution error rates and RDS CPU/Memory utilization | 07/07/2026 | 07/07/2026 | <https://docs.aws.amazon.com/rds/> |
| Thu | - Execute Security Audit review: restrict IAM role policies to minimal required actions, close unused inbound ports on VPC Security Groups | 09/07/2026 | 09/07/2026 | <https://docs.aws.amazon.com/IAM/latest/UserGuide/> |

### Week 12 Achievements:

* **Load Testing Executed**: Pinpointed exact performance bottlenecks on Lambda function invocations under high concurrent stress.
* **Effective Performance Tuning**: Reduced average API response latency from ~1.2s to ~350ms by tuning Lambda allocations and SQL queries.
* **Harden Cloud Security**: Successfully locked down S3 bucket access, IAM Roles, and limited RDS access exclusively inside the VPC subnet.
* **Successful Technical Handover**: Tagged and released LingoRise v1.0.0 on GitHub along with complete architecture blueprints and operational guides.
