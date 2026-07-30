---
title: "Worklog Week 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Master core security concepts and AWS Identity and Access Management (IAM).
* Enforce security policies based on the Principle of Least Privilege, managing IAM Users, Groups, Roles, and Multi-Factor Authentication (MFA).

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Source |
| --- | --- | --- | --- | --- |
| Mon | - Study the AWS Shared Responsibility Model <br>- Understand core IAM primitives: Users, User Groups, Roles, and Policies | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | - Analyze IAM Policy structure (JSON format: Effect, Action, Resource, Condition) <br>- Compare AWS Managed Policies vs Customer Managed Policies vs Inline Policies | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Wed | - **AWS IAM Hands-on:** <br>&emsp; + Create IAM Users for team roles and assign them to functional IAM Groups <br>&emsp; + Enable Multi-Factor Authentication (MFA) for Root Account and IAM Users | 04/06/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Thu | - Research IAM Roles and Trust Relationships <br>- **Hands-on:** Create an IAM Role allowing EC2 instances to access Amazon S3 securely without hardcoded credentials | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Fri | - Test IAM permissions using IAM Policy Simulator and perform security auditing via AWS Credential Reports | 06/06/2026 | 06/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 2 Achievements:

* Acquired deep understanding of identity and permission control mechanisms in AWS Cloud.
* Implemented standardized IAM User/Group hierarchies and enforced mandatory MFA protection.
* Authored and customized granular IAM Policies following Least Privilege principles.
* Assigned IAM Roles to EC2 workloads, eliminating hardcoded secret keys in application code.
