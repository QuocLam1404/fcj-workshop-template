---
title: "Blog 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

# AUTOMATING PAYMENTS WITH PAYOS WEBHOOKS & AWS LAMBDA

This blog details the step-by-step implementation of automated payment verification using PayOS dynamic QR codes and asynchronous webhook handling on AWS Lambda.

Key points to know:

* A session policy is an inline IAM policy specified when creating or updating a Pod Identity association.
* Effective permissions = intersection between the IAM role permissions and the session policy → the session policy can only narrow permissions, not expand them.
* Helps avoid over-permissioning when reusing a single IAM role for multiple workloads with different needs.
* Supports both same-account and cross-account (via IAM role chaining).
* Significantly reduces the number of IAM roles that need to be managed, helping avoid hitting IAM quota limits in large clusters.
* Easily configured through the AWS Management Console, AWS CLI, or AWS SDK when creating an association between a Kubernetes ServiceAccount and an IAM role.

This feature is especially useful when you have many applications running on the same IAM role but need different permission restrictions (for example: one pod only reads a specific S3 bucket, another pod only calls certain APIs).

...Image...

...Link...

...Guide...