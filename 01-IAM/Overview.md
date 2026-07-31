# 🔐 AWS Identity and Access Management (IAM)

> AWS Identity and Access Management (IAM) is the foundation of AWS security. It enables you to securely manage identities, control access to AWS resources, and enforce the principle of least privilege.

---

# 📖 Table of Contents

- What is IAM?
- Why IAM?
- IAM Components
- IAM Authentication vs Authorization
- IAM Best Practices
- Learning Roadmap
- Module Structure

---

# 🎯 Learning Objectives

After completing this module, you will be able to:

- Understand AWS IAM
- Create and manage IAM Users
- Create IAM Groups
- Understand IAM Roles
- Write IAM Policies
- Secure AWS Accounts using MFA
- Follow IAM Best Practices
- Answer IAM interview questions

---

# 🔐 What is IAM?

AWS Identity and Access Management (IAM) is a global AWS service used to securely control access to AWS resources.

IAM helps you answer three important questions:

- Who can access AWS?
- What resources can they access?
- What actions are they allowed to perform?

Instead of sharing one AWS account with everyone, IAM allows you to create separate identities with specific permissions.

---

# ❓ Why IAM?

Without IAM:

- Everyone would use the Root User.
- No access control.
- High security risk.
- Difficult auditing.
- No permission management.

With IAM:

- Individual users
- Role-based access
- Fine-grained permissions
- Multi-Factor Authentication
- Secure access management

---

# 🧩 IAM Components

- IAM Users
- IAM Groups
- IAM Roles
- IAM Policies
- MFA
- Access Keys
- Password Policies

---

# 🔑 Authentication vs Authorization

| Authentication | Authorization |
|---------------|---------------|
| Who are you? | What can you do? |
| Login | Permissions |
| Username & Password | IAM Policy |
| MFA | Allow/Deny Actions |

---

# 📚 Module Structure

```

01-IAM/
│
├── README.md
├── 01-iam-identities.md
├── 02-iam-security.md
├── 03-hands-on-labs.md
└── 04-interview-questions.md

```

---

# 🚀 Learning Roadmap

```

IAM Overview
        ↓
Users
        ↓
Groups
        ↓
Roles
        ↓
Policies
        ↓
MFA
        ↓
Hands-on Labs
        ↓
Interview Questions

```

---

## 🚀 Next File

**01-iam-identities.md**

```
Users
Groups
Roles
```
