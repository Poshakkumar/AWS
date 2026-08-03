# 🚀 Amazon ECS Commands Cheat Sheet

> Common AWS CLI and Docker commands for Amazon ECS.

---

# 📋 Prerequisites

- AWS CLI installed
- Docker installed
- IAM permissions for ECS & ECR
- Configured AWS credentials

```bash
aws configure
```

---

# 🔍 List ECS Clusters

```bash
aws ecs list-clusters
```

---

# 📄 Describe a Cluster

```bash
aws ecs describe-clusters \
--clusters my-cluster
```

---

# 🏗 Create a Cluster

```bash
aws ecs create-cluster \
--cluster-name my-cluster
```

---

# ❌ Delete a Cluster

```bash
aws ecs delete-cluster \
--cluster my-cluster
```

---

# 📋 Register a Task Definition

```bash
aws ecs register-task-definition \
--cli-input-json file://task-definition.json
```

---

# 📄 List Task Definitions

```bash
aws ecs list-task-definitions
```

---

# 🔍 Describe a Task Definition

```bash
aws ecs describe-task-definition \
--task-definition my-app
```

---

# ▶️ Run a Task

```bash
aws ecs run-task \
--cluster my-cluster \
--task-definition my-app
```

---

# 🛑 Stop a Task

```bash
aws ecs stop-task \
--cluster my-cluster \
--task TASK_ID
```

---

# 📋 List Running Tasks

```bash
aws ecs list-tasks \
--cluster my-cluster
```

---

# 🔍 Describe a Task

```bash
aws ecs describe-tasks \
--cluster my-cluster \
--tasks TASK_ID
```

---

# 🚀 Create an ECS Service

```bash
aws ecs create-service \
--cluster my-cluster \
--service-name my-service \
--task-definition my-app \
--desired-count 2
```

---

# 📄 List Services

```bash
aws ecs list-services \
--cluster my-cluster
```

---

# 🔍 Describe a Service

```bash
aws ecs describe-services \
--cluster my-cluster \
--services my-service
```

---

# 📈 Scale a Service

```bash
aws ecs update-service \
--cluster my-cluster \
--service my-service \
--desired-count 4
```

---

# 🔄 Force New Deployment

```bash
aws ecs update-service \
--cluster my-cluster \
--service my-service \
--force-new-deployment
```

---

# ❌ Delete a Service

```bash
aws ecs delete-service \
--cluster my-cluster \
--service my-service \
--force
```

---

# 📊 View ECS Service Events

```bash
aws ecs describe-services \
--cluster my-cluster \
--services my-service
```

---

# 📝 List Container Instances (EC2 Launch Type)

```bash
aws ecs list-container-instances \
--cluster my-cluster
```

---

# 📦 Docker Build Image

```bash
docker build -t my-app .
```

---

# 🏷 Tag Docker Image

```bash
docker tag my-app:latest \
ACCOUNT_ID.dkr.ecr.REGION.amazonaws.com/my-app:latest
```

---

# 🔐 Login to Amazon ECR

```bash
aws ecr get-login-password --region REGION \
| docker login \
--username AWS \
--password-stdin ACCOUNT_ID.dkr.ecr.REGION.amazonaws.com
```

---

# ⬆️ Push Image to Amazon ECR

```bash
docker push ACCOUNT_ID.dkr.ecr.REGION.amazonaws.com/my-app:latest
```

---

# ⬇️ Pull Image

```bash
docker pull ACCOUNT_ID.dkr.ecr.REGION.amazonaws.com/my-app:latest
```

---

# 📊 View CloudWatch Logs

```bash
aws logs describe-log-groups
```

---

# 🔍 Tail Logs

```bash
aws logs tail LOG_GROUP_NAME --follow
```

---

# 📈 Check ECS Metrics

```bash
aws cloudwatch list-metrics \
--namespace AWS/ECS
```

---

# 🧹 Best Practices

- Use Amazon ECR for container images.
- Store secrets in AWS Secrets Manager or Parameter Store.
- Use Fargate for serverless workloads.
- Enable CloudWatch Logs.
- Keep task definitions versioned.
- Use IAM Roles instead of hardcoded credentials.
- Use rolling deployments for production.

---

# ⚡ Quick Workflow

```text
Docker Build
      │
      ▼
Docker Tag
      │
      ▼
Push Image to ECR
      │
      ▼
Register Task Definition
      │
      ▼
Create ECS Service
      │
      ▼
Application Load Balancer
      │
      ▼
Running Containers
```

---
