# 🌐 Amazon ECS Networking & Scaling

> Learn how Amazon ECS handles networking, integrates with Load Balancers, performs service discovery, and scales containerized applications.

![alt text](flow.png)

---

# 📖 Table of Contents

- Networking Modes
- Load Balancer Integration
- Service Discovery
- Auto Scaling
- Deployment Strategies
- Monitoring
- Best Practices
- Key Takeaways

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Understand ECS networking
- Integrate ECS with ALB
- Configure Service Discovery
- Scale ECS Services
- Deploy applications with minimal downtime

---

# 🌐 ECS Networking

ECS tasks communicate using different networking modes.

### Bridge Mode

- Default mode for EC2 launch type
- Containers share the EC2 network

### Host Mode

- Container uses the EC2 network directly
- Better performance
- No port mapping

### awsvpc Mode (Recommended)

- Each ECS Task gets its own Elastic Network Interface (ENI)
- Supports Security Groups
- Required for AWS Fargate

Example:

```text
VPC
 │
 ├── Task 1 (Private IP)
 ├── Task 2 (Private IP)
 └── Task 3 (Private IP)
```

---

# ⚖️ Load Balancer Integration

Amazon ECS integrates with **Application Load Balancer (ALB)**.

Workflow:

```text
Internet
     │
Route 53
     │
ALB
     │
Target Group
     │
ECS Service
     │
Running Tasks
```

Benefits:

- Automatic traffic distribution
- Health checks
- High availability

---

# 🔍 Service Discovery

Service Discovery allows containers to communicate using service names instead of IP addresses.

Example:

```text
frontend.local

↓

backend.local
```

Benefits:

- Easier communication
- Dynamic service discovery
- Better microservices architecture

---

# 📈 ECS Auto Scaling

ECS Service Auto Scaling adjusts the number of running tasks based on demand.

Example:

```text
CPU > 70%

↓

Increase Tasks

3 → 6 Tasks
```

Metrics used:

- CPU Utilization
- Memory Utilization
- Request Count

---

# 🚀 Deployment Strategies

### Rolling Deployment

- Replaces old tasks gradually
- No downtime
- Default deployment type

```text
Version 1
   │
Replace gradually
   │
Version 2
```

### Blue/Green Deployment

Two environments run simultaneously.

```text
Blue → Current Version

Green → New Version

↓

Switch Traffic
```

Benefits:

- Safer deployments
- Easy rollback
- Zero downtime

---

# 📊 Monitoring

Monitor ECS using **Amazon CloudWatch**.

Common metrics:

- CPU Utilization
- Memory Utilization
- Running Tasks
- Pending Tasks
- Service Health

Logs can also be sent to **CloudWatch Logs**.

---

# 🏗 Production Architecture

```text
                 Internet
                     │
               Amazon Route 53
                     │
         Application Load Balancer
                     │
             ECS Service (Fargate)
             ┌────────┴────────┐
             ▼                 ▼
        ECS Task 1        ECS Task 2
             │                 │
             └────────┬────────┘
                      ▼
                Amazon RDS
```

---

# ⭐ Best Practices

- Use **awsvpc** mode for new applications.
- Run ECS tasks in private subnets.
- Use ALB for incoming traffic.
- Enable Service Auto Scaling.
- Store container images in Amazon ECR.
- Monitor services with CloudWatch.
- Use Blue/Green deployments for production releases.

---

# 📝 Key Takeaways

- ECS supports multiple networking modes.
- ALB distributes traffic to ECS tasks.
- Service Discovery simplifies communication.
- Auto Scaling adjusts the number of running tasks.
- Rolling and Blue/Green deployments reduce downtime.
- CloudWatch provides monitoring and logging.

---

# 🚀 Next Module

# ☸️ Amazon EKS (Elastic Kubernetes Service)

Topics Covered:

- What is Kubernetes?
- What is Amazon EKS?
- Cluster Components
- Worker Nodes
- Pods
- Deployments
- Services
- Networking