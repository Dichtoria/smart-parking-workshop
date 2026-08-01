---
title: "Configure Task Definition for ECS"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.5.1. </b> "
---

# Step 7: Configure Task Definition for ECS

> **💡 Why configure an ECS Task Definition?**  
> An **ECS Task Definition** serves as a standardized architectural blueprint. It defines exact container vCPU resources, allocated RAM, container network port mappings (Port 8000), and securely injects database credentials and environment variables into the running container.

---

A Task Definition functions as a blueprint defining how your containers run on the ECS service (environment variables can be configured directly through the task).

#### Steps:

1. Log in to **AWS Management Console** and search for **Elastic Container Service (ECS)**.
2. In the left navigation menu, select **Task definitions**.
3. Click **Create new task definition with JSON** (Create new configuration blueprint).  
   *(This step can be set up manually, but pasting a pre-configured JSON file is recommended)*.
4. Copy the contents of file `ecs-task-definition.json` and paste ➔ Click **Create**.

![Task Definition](/images/5-Workshop/5.5-ECS-Fargate/5.5.1-task-definition/complete.png)
