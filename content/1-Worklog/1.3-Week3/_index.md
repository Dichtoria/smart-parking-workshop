---
title: "Worklog Week 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* In-depth learning of managed relational databases with Amazon Relational Database Service (Amazon RDS).
* Provision, configure, and secure PostgreSQL/MySQL infrastructure, DB Subnet Groups, Security Groups, and DB Snapshot backup policies.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Source |
| --- | --- | --- | --- | --- |
| Mon | - Amazon RDS overview: Compare self-hosted databases on EC2 vs Amazon RDS managed services <br>- Study supported DB engines: PostgreSQL, MySQL, MariaDB, Oracle, SQL Server | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Tue | - Research Multi-AZ High Availability architecture (Primary & Synchronous Standby Replica) <br>- Understand Read Replicas for scaling read-heavy database workloads | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Wed | - **Amazon RDS Hands-on:** <br>&emsp; + Create a DB Subnet Group across isolated Private Subnets <br>&emsp; + Provision an Amazon RDS PostgreSQL instance within Private Subnets | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Thu | - Configure VPC Security Groups for RDS: Restrict port 5432 ingress exclusively to Application/EC2 Security Groups <br>- Test database connectivity from an EC2 instance | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| Fri | - Study database backup strategies: Automated Backups & Manual DB Snapshots <br>- **Hands-on:** Create a manual snapshot, restore a new DB instance from snapshot, and copy snapshots | 13/06/2026 | 13/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Week 3 Achievements:

* Mastered Amazon RDS cloud database architectures and Multi-AZ high availability deployments.
* Successfully launched an Amazon RDS PostgreSQL instance isolated within private VPC subnets.
* Secured database network boundaries using strict Security Group ingress rules.
* Proficient in automated backup management and point-in-time recovery using DB Snapshots.
