---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Smart Parking System
## Integrated AI & AWS Cloud Smart Parking Solution

### 1. Executive Summary
The **Smart Parking System** is designed to address modern parking management challenges by optimizing spot discovery and automating vehicle entry/exit recognition. The platform combines Artificial Intelligence (AI/Computer Vision) with robust AWS Cloud infrastructure, featuring Automatic Number Plate Recognition (ANPR), real-time occupancy monitoring, and centralized management. By leveraging AWS Serverless & Containerization services (Amazon RDS PostgreSQL, Amazon ECS Fargate, Amazon ECR, Amazon CloudFront, and AWS Amplify), the system ensures high availability, flexible scalability, and operational cost optimization without relying on expensive Load Balancers.

### 2. Problem Statement
*Current Problem*  
Traditional parking lots face significant limitations:
- **Manual Collection & Operations**: Drivers spend excessive time hunting for vacant spots, creating internal traffic congestion.
- **Lack of Real-time Visibility**: Facility managers lack real-time insights into parking occupancy and vehicle flow metrics.
- **Revenue Leakage Risk & High Labor Costs**: Entry/exit control relies on paper tickets or manual RFID cards, prone to human error and fraud.

*Solution*  
The Smart Parking System enables users to pre-register vacant spots, generate reservation QR codes, and pay in advance. The system utilizes AI (Computer Vision) to automatically scan and recognize license plates and QR codes at entry/exit gates.
- **Backend & Database**: Containerized using Docker, images stored on Amazon ECR, and executed on Serverless Amazon ECS Fargate. Secure transactional and vehicle data stored in Amazon RDS PostgreSQL.
- **Content Delivery & Frontend**: Amazon CloudFront CDN connects directly to the ECS Backend to minimize real-time data transmission latency; AWS Amplify hosts a Fullstack Web Application (Next.js/React) allowing drivers and managers to access dashboards anytime, anywhere.
- **Security**: Granular access management with AWS IAM and network protection via Security Groups. (This security setup is for demonstration purposes; production deployments can utilize higher-level security services such as AWS WAF, etc.)

*Benefits and Return on Investment (ROI)*  
- Reduces vehicle parking spot search time by 60%.
- Automates 90% of entry/exit gate controls, reducing parking facility labor overhead.
- Optimizes infrastructure costs by eliminating unnecessary Load Balancers (ALB) and adopting AWS Pay-as-you-go / Serverless billing models.
- Estimated Return on Investment (ROI) timeframe within 6 to 12 months.

### 3. Solution Architecture
The system adopts a modern architecture integrating Edge AI and AWS Cloud Services for real-time parking data processing:

![Platform Architecture](/images/2-Proposal/FINAL_ARCHITECTURE.png)

*AWS Services Used*  
- **AWS CLI & IAM**: Command-line administration and secure access management adhering to Least Privilege principles.
- **Amazon RDS (PostgreSQL)**: Managed relational database storing license plate logs, entry/exit timestamps, and spot availability status.
- **Amazon ECR (Elastic Container Registry)**: Secure storage and management of Docker Container Images.
- **Amazon ECS (AWS Fargate)**: Serverless container orchestration and execution for backend services without server management.
- **Amazon CloudFront**: Global Content Delivery Network (CDN) pointing directly to ECS Services, accelerating API responses & real-time data streaming.
- **AWS Amplify**: Fullstack Web Frontend hosting and automated CI/CD deployment pipelines.

*Component Design*  
- **Cameras & AI Processing**: Entry/exit gate cameras capture video streams; AI models extract license plate numbers & vacant spot status.
- **Backend Ingestion & Processing**: Amazon CloudFront routes API requests directly to ECS Fargate Tasks for business logic execution.
- **Data Storage**: Amazon RDS PostgreSQL stores transactional logs; Amazon ECR stores application images.
- **User Dashboard**: AWS Amplify provides real-time web interface maps for customers and facility operators.

### 4. Technical Implementation
*Implementation Phases*  
1. **Research & Architecture Design**: Evaluate AI license plate recognition models and design AWS cloud architecture (Month 1).
2. **Container Build & Packaging**: Build backend application logic, containerize Docker Images, and push to Amazon ECR (Month 1 - Month 2).
3. **AWS Cloud Infrastructure Provisioning**: Deploy RDS PostgreSQL, VPC, ECS Fargate Clusters, CloudFront CDN, and AWS Amplify (Month 2).
4. **End-to-End Integration & Testing**: Connect end-to-end data pipelines from Camera/AI -> ECS Backend -> RDS Database -> Amplify Frontend (Month 2 - Month 3).

*Technical Requirements*  
- **Edge AI Infrastructure**: Computer Vision models (YOLO/OCR) optimized for edge deployment or central inference servers.
- **AWS Cloud Infrastructure**: Operating proficiency in AWS CLI, Docker, Amazon ECR, Amazon ECS Fargate, Amazon RDS PostgreSQL, CloudFront CDN, and AWS Amplify.

### 5. Roadmap & Milestones
- **Phase 1 (Weeks 1 - 4)**: AWS core fundamentals, IAM security governance, VPC setup & Amazon RDS PostgreSQL database initialization.
- **Phase 2 (Weeks 5 - 7)**: Docker containerization, ECR pushing, ECS Fargate cluster deployment, CloudFront & AWS Amplify integration.
- **Phase 3 (Weeks 8 - 9)**: Workshop project peak execution, end-to-end Smart Parking System integration.
- **Phase 4 (Weeks 10 - 12)**: Security hardening, Cost Optimization assessment, and final report compilation.

### 6. Budget Estimation
Infrastructure costs calculated via [AWS Pricing Calculator](https://calculator.aws/):

*Estimated Monthly AWS Infrastructure Costs:*
- **Amazon RDS PostgreSQL (db.t4g.micro / Free Tier)**: ~$14.50/month ($0.00 under AWS Free Tier).
- **Amazon ECS Fargate (0.25 vCPU, 0.5 GB RAM)**: ~$9.00/month.
- **Amazon ECR (5 GB Container Image Storage)**: ~$0.50/month.
- **Amazon CloudFront (10 GB Data Transfer Out)**: ~$0.85/month.
- **AWS Amplify (Hosting & Build time)**: ~$1.50/month.
- **Route 53 & Domain Name**: ~$1.00/month.

*Total Estimated AWS Cost*: **~$27.35/month** (Estimated < $10.00/month when applying AWS Free Tier limits and eliminating ALB overhead).

### 7. Risk Assessment
*Risk Matrix*  
- **Internet Network Disruption**: Impact High, Probability Medium.
- **AI Recognition Errors (Dim lighting/blurred plates)**: Impact Medium, Probability Medium.
- **AWS Cost Budget Overrun**: Impact Medium, Probability Low.

*Mitigation Strategies*  
- **Network**: Implement local data caching on edge devices during temporary internet outages.
- **AI**: Combine image preprocessing and allow manual operator verification on Dashboard when AI confidence < 85%.
- **Cost**: Configure AWS Budgets alerts when expenditure exceeds 80% of projected thresholds.

*Contingency Plan*  
- Use AWS CloudFormation / AWS CDK to rapidly recreate infrastructure in case of disaster recovery events.
- Switch to manual license plate entry on Web Dashboard if hardware cameras experience failure.

### 8. Expected Outcomes
*Technical Improvements*: Complete automation of real-time parking recognition and management workflows. Streamlined Serverless cloud architecture eliminating ALB to optimize operational costs.  
*Long-term Value*: Provides standardized data feeds for urban traffic analysis, optimizes parking operating expenses, and elevates user experience.

### 9. Demo of Achieved Results

**Menu-login Interface**

![Menu-login](/images/2-Proposal/Frontend_menu.png)

**Booking Interface**

![Booking](/images/2-Proposal/booking.png)

**Admin Interface**

![Admin](/images/2-Proposal/admin.png)

**VNPay Payment Interface**

![VNPay1](/images/2-Proposal/vnp1.png)

![VNPay2](/images/2-Proposal/vnp2.png)

**Scanning**

![Scanning](/images/2-Proposal/scanning.png)