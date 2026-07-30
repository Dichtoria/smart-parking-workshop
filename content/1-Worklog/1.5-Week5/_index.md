---
title: "Worklog Week 5"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* In-depth learning of Amazon Elastic Container Service (ECS) for container orchestration and operations.
* Deploy containerized applications running on Serverless AWS Fargate for optimal cost efficiency.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Source |
| --- | --- | --- | --- | --- |
| Mon | - Overview of Amazon ECS: ECS Cluster architecture, Task Definitions, Tasks & Services <br>- Differentiate launch types: ECS EC2 Launch Type vs ECS Fargate Launch Type (Serverless) | 23/06/2026 | 23/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | - Configure ECS Task Definitions (Container Image URI from ECR, vCPU, RAM, Port Mappings, Environment Variables) <br>- Configure Task Execution IAM Roles | 24/06/2026 | 24/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Wed | - **Amazon ECS Hands-on:** <br>&emsp; + Create an ECS Cluster powered by AWS Fargate <br>&emsp; + Register an ECS Task Definition referencing the ECR Docker Image created in Week 4 | 25/06/2026 | 25/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Thu | - Configure ECS Service, set Desired Task count, and manage VPC Security Group access rules for Tasks | 26/06/2026 | 26/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Fri | - **Hands-on:** Launch ECS Service on Fargate, verify self-healing capabilities when tasks terminate, and test direct HTTP/HTTPS connections to containers | 27/06/2026 | 27/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 5 Achievements:

* Understood container orchestration patterns with Amazon ECS and Serverless AWS Fargate.
* Successfully authored ECS Task Definitions specifying container resources and environment parameters.
* Deployed containerized applications seamlessly on AWS Fargate without managing underlying EC2 server instances.
* Configured networking and security group ingress rules for ECS Tasks.
