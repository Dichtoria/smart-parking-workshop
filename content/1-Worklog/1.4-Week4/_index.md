---
title: "Worklog Week 4"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Master application containerization techniques using Docker Containers and private registry management with Amazon ECR (Elastic Container Registry).
* Build lightweight, optimized Docker Images and perform container authentication, push, and pull workflows to Amazon ECR.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Source |
| --- | --- | --- | --- | --- |
| Mon | - Containerization vs Virtual Machines (VMs) concepts overview <br>- Install Docker Engine, understand Docker Daemon, Client, and Image Layering architectures | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | - Study `Dockerfile` syntax (FROM, WORKDIR, COPY, RUN, EXPOSE, CMD/ENTRYPOINT) <br>- **Hands-on:** Write Dockerfiles for Node.js / Python Web applications and build Docker Images | 17/06/2026 | 17/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Wed | - Research Amazon Elastic Container Registry (ECR): Repositories, Image Tags, Image Scanning, and IAM Authorization Tokens | 18/06/2026 | 18/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Thu | - **Amazon ECR Hands-on:** <br>&emsp; + Create a Private ECR Repository via AWS Management Console <br>&emsp; + Authenticate Docker CLI using `aws ecr get-login-password` | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Fri | - **Hands-on:** Tag (`docker tag`) and push Docker Images successfully to Amazon ECR, enabling Image Vulnerability Scanning | 20/06/2026 | 20/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 4 Achievements:

* Mastered application containerization using optimized, multi-stage Dockerfiles.
* Created and administered private container registries on Amazon ECR.
* Successfully authenticated local Docker CLI with AWS ECR using AWS CLI credentials.
* Published, versioned, and scanned container images securely on Amazon ECR.
