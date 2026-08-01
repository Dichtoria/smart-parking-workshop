---
title: "Access Amazon ECR & Create Repository"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.4.1. </b> "
---

# Step 5: Access Amazon ECR & Create Repository

Amazon ECR stores your application Docker images before deployment to ECS.

#### Steps:

1. Log in to **AWS Management Console** and search for **Elastic Container Registry (ECR)**.
2. On the main ECR screen, click **Create repository** to begin creating a new repository.
3. **Repository Name**: Enter `parkflow_backend`.
4. Keep remaining default settings, scroll to bottom and click **Create repository**.

![Create Repository](/images/5-Workshop/5.4-ECR-Docker/5.4.1-create-ecr/create_repo.png)

5. ECR provides execution commands as push guidance; click your newly created repository.

![Create Repository](/images/5-Workshop/5.4-ECR-Docker/5.4.1-create-ecr/complete.png)

6. In the top right corner, select **View push commands**.

![Create Repository](/images/5-Workshop/5.4-ECR-Docker/5.4.1-create-ecr/push_commands.png)

7. AWS displays a popup containing 4 execution steps corresponding to 4 pre-populated commands with your AWS Account ID, Region, and Repository Name.

![Create Repository](/images/5-Workshop/5.4-ECR-Docker/5.4.1-create-ecr/commands.png)
