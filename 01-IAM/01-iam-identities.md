# 👥 IAM Identities

> IAM Identities represent people or services that interact with AWS resources.

---

# 📖 Table of Contents

- IAM Users
- IAM Groups
- IAM Roles
- Users vs Groups vs Roles
- Best Practices
- Key Takeaways

---

# 👤 IAM User

An IAM User is an identity created for a person or application that needs access to AWS.

Each user has unique credentials.

A user can have:

- Username
- Password
- Access Keys
- MFA Device
- Permissions

Example:

```

Developer → Login → AWS Console

```

Use Cases

- Developer
- DevOps Engineer
- Cloud Engineer
- Administrator

---

# 👥 IAM Group

An IAM Group is a collection of IAM Users.

Instead of assigning permissions individually, permissions are attached to the group.

Example

```

Developers Group

├── Rahul
├── Aman
├── Priya

```

Attach one policy to the Developers Group and every member receives the same permissions.

Benefits

- Easy permission management
- Centralized administration
- Better scalability

---

# 🎭 IAM Role

An IAM Role is an identity with temporary permissions.

Unlike users, roles do not have passwords or long-term credentials.

Roles are assumed when needed.

Examples

- EC2 accessing S3
- Lambda accessing DynamoDB
- Cross-account access
- AWS Services communicating securely

Example

```

EC2 Instance

↓

Assume IAM Role

↓

Access Amazon S3

```

Benefits

- Temporary credentials
- Improved security
- No hardcoded access keys
- Cross-account access

---

# 📊 Comparison

| Feature | User | Group | Role |
|----------|------|-------|------|
| Login | ✅ | ❌ | ❌ |
| Password | ✅ | ❌ | ❌ |
| Access Keys | ✅ | ❌ | Temporary |
| Contains Users | ❌ | ✅ | ❌ |
| Permissions | Direct | Shared | Temporary |
| Best For | Humans | Teams | AWS Services |

---

# 💼 Real-World Example

Company Structure

```

AWS Account

│

├── Developers Group

│ ├── Rahul

│ ├── Priya

│ └── Aman

│

├── Admin Group

│ └── Admin

│

└── EC2 Role

↓

Amazon S3 Access

```

---

# 📝 Key Takeaways

- Users are individual identities.
- Groups organize users.
- Roles provide temporary permissions.
- Roles are preferred for AWS services.
- Groups simplify permission management.

---

# 🚀 Next File

02-iam-security.md