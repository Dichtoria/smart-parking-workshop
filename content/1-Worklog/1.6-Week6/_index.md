---
title: "Worklog Week 6"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* In-depth study of Amazon CloudFront Content Delivery Network (CDN).
* Optimize application latency globally, integrate SSL/TLS certificates via AWS Certificate Manager (ACM), and secure origin servers.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Source |
| --- | --- | --- | --- | --- |
| Mon | - Overview of Amazon CloudFront: CDN concepts, Edge Locations, Regional Edge Caches <br>- Differentiate Origin types: S3 Buckets, ECS Service Domain/IP, or Custom Origins | 30/06/2026 | 30/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | - Study Caching Behaviors, TTL (Time-To-Live), Query String & Header forwarding <br>- **Hands-on:** Create a CloudFront Distribution pointing to an S3 static website bucket | 01/07/2026 | 01/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Wed | - Restrict S3 Origin access using Origin Access Control (OAC) / Origin Access Identity (OAI) to prevent direct public S3 bucket access | 02/07/2026 | 02/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Thu | - Configure Custom Domains integrated with free HTTPS certificates via AWS Certificate Manager (ACM) <br>- Study CloudFront Cache Invalidation commands | 03/07/2026 | 03/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Fri | - **Hands-on:** <br>&emsp; + Create CloudFront Distribution backed directly by an ECS Fargate application origin <br>&emsp; + Execute Create Invalidation requests and benchmark global edge latency | 04/07/2026 | 04/07/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 6 Achievements:

* Understood the operational mechanics of Amazon CloudFront Content Delivery Network (CDN).
* Successfully created CloudFront Distributions to drastically reduce global page load latency.
* Secured S3 Bucket Origins with OAC policy restrictions, forcing all user traffic through CloudFront.
* Configured SSL/TLS HTTPS security certificates and mastered CloudFront cache invalidation procedures.
