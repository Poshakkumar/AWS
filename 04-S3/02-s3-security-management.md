# 🔒 Amazon S3 Security & Management

> Learn how to secure and manage Amazon S3 using Bucket Policies, IAM Policies, Access Control Lists (ACLs), Encryption, Versioning, Replication, Event Notifications, and Object Lock.

---

# 📖 Table of Contents

- S3 Access Control
- IAM vs Bucket Policy vs ACL
- Block Public Access
- Encryption
- Cross-Region Replication (CRR)
- Same-Region Replication (SRR)
- Presigned URLs
- Object Lock
- Event Notifications
- Best Practices
- Key Takeaways

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Secure S3 Buckets
- Control access to objects
- Protect sensitive data using encryption
- Replicate data across regions
- Generate temporary file access
- Automate workflows using S3 events

---

# 🔐 S3 Access Control

Amazon S3 provides multiple ways to control access.

- IAM Policies
- Bucket Policies
- Access Control Lists (ACLs)
- Block Public Access

AWS recommends using **IAM Policies** and **Bucket Policies** instead of ACLs whenever possible.

---

# ⚖️ IAM Policy vs Bucket Policy vs ACL

| Feature | IAM Policy | Bucket Policy | ACL |
|----------|------------|---------------|-----|
| Scope | User/Role | Bucket | Bucket/Object |
| Cross-Account Access | ✅ | ✅ | Limited |
| Recommended | ✅ | ✅ | ❌ |
| JSON Based | ✅ | ✅ | ❌ |

---

# 🚫 Block Public Access

Block Public Access prevents accidental exposure of your S3 buckets.

Benefits:

- Protects sensitive data
- Prevents unintended public access
- Enabled by default for new buckets

Always keep this enabled unless your bucket is intentionally public (e.g., static website hosting).

---

# 🔐 Server-Side Encryption (SSE)

Encryption protects data stored in Amazon S3.

### SSE-S3

AWS manages the encryption keys.

Best for:

- General workloads
- Easy management

---

### SSE-KMS

Uses AWS Key Management Service (KMS).

Benefits:

- More control
- Audit logging
- Key rotation

Best for:

- Sensitive data
- Enterprise workloads

---

### SSE-C

Customer provides the encryption key.

Best for:

- Organizations managing their own encryption keys

---

# 🌍 Cross-Region Replication (CRR)

CRR automatically copies objects from one AWS Region to another.

Example:

```text
Mumbai Bucket
      │
      ▼
Singapore Bucket
```

Use Cases:

- Disaster Recovery
- Global Applications
- Compliance

> Versioning must be enabled on both buckets.

---

# 🔄 Same-Region Replication (SRR)

SRR copies objects between buckets within the same AWS Region.

Use Cases:

- Log aggregation
- Backup
- Testing

---

# 🔗 Presigned URLs

A Presigned URL provides temporary access to a private object.

Example:

```text
Private File
      │
Generate Presigned URL
      │
Share with User
      │
Access expires automatically
```

Common Use Cases:

- Secure file sharing
- Temporary downloads
- Uploads from web applications

---

# 🔒 Object Lock

Object Lock protects objects from deletion or modification for a specified period.

Modes:

- Governance Mode
- Compliance Mode

Use Cases:

- Financial records
- Legal documents
- Regulatory compliance

---

# ⚡ Event Notifications

Amazon S3 can trigger events when objects are created or deleted.

Supported Destinations:

- AWS Lambda
- Amazon SNS
- Amazon SQS

Example:

```text
Upload Image
      │
S3 Bucket
      │
Lambda Function
      │
Resize Image
```

---

# ⭐ Best Practices

- Enable Versioning.
- Enable Block Public Access.
- Use SSE-KMS for sensitive data.
- Enable Lifecycle Rules.
- Use CRR for disaster recovery.
- Follow the Principle of Least Privilege.
- Monitor bucket activity with AWS CloudTrail.

---

# 📝 Key Takeaways

- IAM Policies control user permissions.
- Bucket Policies control bucket access.
- Block Public Access protects against accidental exposure.
- Encryption secures stored data.
- CRR and SRR replicate objects.
- Presigned URLs provide temporary access.
- Object Lock prevents accidental deletion.
- Event Notifications automate workflows.

---

# 🚀 Next Module

## 🗄️ Amazon RDS (Relational Database Service)

Topics Covered:

- What is Amazon RDS?
- Database Engines
- Multi-AZ Deployment
- Read Replicas
- Backups & Snapshots
- Storage
- Security
- High Availability