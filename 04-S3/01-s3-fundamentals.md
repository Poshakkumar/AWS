# 📦 Amazon S3 Fundamentals

> Learn the core concepts of Amazon S3 including Buckets, Objects, Object Keys, Storage Classes, Versioning, Lifecycle Rules, and Static Website Hosting.

---

# 📖 Table of Contents

- What is Amazon S3?
- Bucket
- Object
- Object Key
- Storage Classes
- Versioning
- Lifecycle Rules
- Static Website Hosting
- S3 Workflow
- Best Practices

---

# 📦 What is Amazon S3?

Amazon S3 (Simple Storage Service) is a fully managed **Object Storage Service** provided by AWS.

Data is stored as **Objects** inside **Buckets**.

Think of it like:

```text
Bucket
   │
   ├── image.png
   ├── video.mp4
   ├── resume.pdf
   └── backup.zip
```

---

# 🪣 Bucket

A Bucket is a logical container that stores objects.

### Rules

- Bucket names must be globally unique.
- Bucket names cannot be changed after creation.
- A bucket belongs to a specific AWS Region.

Example:

```
company-backups
```

---

# 📄 Object

An Object is the actual file stored inside an S3 bucket.

Examples:

- Images
- Videos
- PDFs
- ZIP Files
- Application Backups
- Logs

Each object contains:

- File
- Metadata
- Object Key
- Version ID (optional)

---

# 🔑 Object Key

Every object has a unique identifier called an **Object Key**.

Example:

```text
images/profile.jpg

documents/resume.pdf

backups/db-backup.zip
```

---

# 💾 Storage Classes

Amazon S3 provides multiple storage classes to optimize cost and performance.

| Storage Class | Use Case |
|--------------|----------|
| S3 Standard | Frequently accessed data |
| S3 Intelligent-Tiering | Automatic cost optimization |
| S3 Standard-IA | Infrequently accessed data |
| S3 One Zone-IA | Non-critical infrequent data |
| S3 Glacier Instant Retrieval | Archive with fast retrieval |
| S3 Glacier Flexible Retrieval | Long-term backups |
| S3 Glacier Deep Archive | Lowest-cost archival storage |

---

# 📜 Versioning

Versioning keeps multiple versions of an object.

Example:

```text
resume.pdf
     │
Version 1
Version 2
Version 3
```

Benefits:

- Recover deleted files
- Restore previous versions
- Protect against accidental overwrites

---

# 🔄 Lifecycle Rules

Lifecycle Rules automatically transition or delete objects based on age.

Example:

```text
Day 0
   │
S3 Standard
   │
30 Days
   │
Standard-IA
   │
90 Days
   │
Glacier
   │
365 Days
   │
Delete
```

Benefits:

- Reduce storage costs
- Automate data management
- Simplify archival

---

# 🌍 Static Website Hosting

Amazon S3 can host static websites.

Supported content:

- HTML
- CSS
- JavaScript
- Images

Example:

```text
index.html
style.css
script.js
images/
```

Common use cases:

- Portfolio websites
- Documentation sites
- Landing pages

---

# 🔄 S3 Workflow

```text
Create Bucket
      │
Upload Objects
      │
Manage Permissions
      │
Enable Versioning
      │
Apply Lifecycle Rules
      │
Access Data
```

---

# ⭐ Best Practices

- Enable Versioning.
- Use Lifecycle Rules to reduce costs.
- Organize objects using folders (prefixes).
- Encrypt sensitive data.
- Block Public Access unless required.
- Choose the appropriate Storage Class.

---

# 📝 Key Takeaways

- Amazon S3 is an object storage service.
- Buckets store objects.
- Object Keys uniquely identify objects.
- Storage Classes optimize cost.
- Versioning protects against accidental deletion.
- Lifecycle Rules automate storage management.
- S3 can host static websites.

---

# 🚀 Next Chapter

**02-s3-security-management.md**

Topics Covered:

- Bucket Policies
- IAM vs Bucket Policies
- ACL
- Encryption
- Cross-Region Replication
- Object Lock
- Presigned URLs
- Event Notifications