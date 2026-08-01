---
title: "Build Docker & Push Image"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.4.2. </b> "
---

# Step 6: Package Docker & Push Image

Package your Backend source code into a Docker image and push it directly to your ECR repository.

#### Steps:

1. Open Terminal (or Command Prompt) on your local computer and navigate to the directory containing your Docker setup file (navigate into the `backend` folder).
2. Sequentially copy each push command from the console screen (from the **View push commands** popup in Step 5) and paste into Terminal to run. This includes: Login, Build Image, Tag, and Push to Cloud.

![Docker Push](/images/5-Workshop/5.4-ECR-Docker/5.4.2-docker-push/build.png)

![Docker Push](/images/5-Workshop/5.4-ECR-Docker/5.4.2-docker-push/push.png)

3. Upon success, image logs will appear in the repository images section.

![Docker Push](/images/5-Workshop/5.4-ECR-Docker/5.4.2-docker-push/logs.png)
