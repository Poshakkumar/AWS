# 🔐 Amazon ECR Security & Lifecycle Policies

> Learn how Amazon ECR secures container images using IAM, encryption, image scanning, lifecycle policies, and cross-region replication.

---
![alt text](flow.png)
![alt text](ecr.png)


# 📖 Table of Contents

- Image Scanning
- Encryption
- Repository Policies
- IAM Permissions
- Lifecycle Policies
- Cross-Region Replication
- Best Practices
- Key Takeaways

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Secure ECR repositories
- Scan container images for vulnerabilities
- Manage repository access
- Automatically clean up old images
- Replicate images across AWS Regions

---

# 🔍 Image Scanning

Amazon ECR can automatically scan images for security vulnerabilities.

### Benefits

- Detect security issues
- Improve application security
- Meet compliance requirements

Example:

```text
Docker Image
      │
      ▼
Amazon ECR
      │
      ▼
Image Scan
      │
      ▼
Vulnerability Report
```

---

# 🔒 Encryption

Amazon ECR encrypts container images at rest.

Encryption options:

- AWS Managed Keys
- AWS KMS Customer Managed Keys

### Benefits

- Secure image storage
- Protect sensitive data
- Compliance support

---

# 📜 Repository Policies

Repository Policies define **who can access an ECR repository**.

Examples:

- Allow Push Images
- Allow Pull Images
- Deny Delete Repository

Repository Policies are resource-based policies similar to Amazon S3 Bucket Policies.

---

# 👤 IAM Permissions

IAM controls what users and roles can do with Amazon ECR.

Examples:

- Create Repository
- Delete Repository
- Push Images
- Pull Images
- List Images

Always follow the **Principle of Least Privilege**.

---

# 🗑 Lifecycle Policies

Lifecycle Policies automatically remove old or unused images.

Example:

```text
Repository

├── v1
├── v2
├── v3
├── latest
└── old-image

↓

Lifecycle Policy

↓

Delete old images automatically
```

### Benefits

- Reduce storage costs
- Keep repositories clean
- Automate image management

---

# 🌍 Cross-Region Replication

Amazon ECR can automatically replicate images to another AWS Region.

Example:

```text
ECR (Mumbai)
      │
      ▼
Replication
      │
      ▼
ECR (Singapore)
```

### Benefits

- Disaster Recovery
- Global Deployments
- Faster image availability

---

# 🏗 Production Workflow

```text
Developer

↓

Docker Build

↓

Amazon ECR

↓

Image Scan

↓

Amazon ECS / Amazon EKS

↓

Running Containers
```

---

# ⭐ Best Practices

- Enable image scanning.
- Encrypt repositories using AWS KMS.
- Use Lifecycle Policies to remove unused images.
- Grant least-privilege IAM permissions.
- Use version tags instead of only `latest`.
- Enable Cross-Region Replication for critical applications.
- Regularly delete untagged images.

---

# 📝 Key Takeaways

- Image Scanning improves container security.
- Encryption protects container images.
- Repository Policies control repository access.
- IAM manages user permissions.
- Lifecycle Policies automate image cleanup.
- Cross-Region Replication supports disaster recovery.

---

# 🚀 Next Module

# 🚢 Amazon ECS (Elastic Container Service)

Topics Covered:

- What is Amazon ECS?
- ECS Components
- ECS Launch Types
- Task Definitions
- Services
- Clusters
- Networking