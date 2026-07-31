![alt text](image.png)
# 🚀 Getting Started with AWS

> This chapter will help you set up your AWS account, understand the AWS Management Console, install the AWS CLI, and provide quick revision notes, interview questions, and learning resources.

---

# 📖 Table of Contents

- Create an AWS Account
- AWS Free Tier
- AWS Management Console
- AWS CLI
- AWS SDK
- Best Practices for Beginners
- AWS Learning Path
- Quick Cheatsheet
- Interview Questions
- Learning Resources

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Create an AWS account
- Understand the AWS Management Console
- Install and configure AWS CLI
- Understand AWS SDK
- Follow AWS security best practices
- Prepare for beginner AWS interviews

---

# 📝 Create an AWS Account

Steps:

1. Visit **https://aws.amazon.com/**
2. Click **Create an AWS Account**
3. Enter your email address and account name.
4. Create a strong password.
5. Verify your email.
6. Add your contact information.
7. Add a payment method.
8. Verify your phone number.
9. Choose the **Free Tier** plan.
10. Sign in to the AWS Console.

---

# 🎁 AWS Free Tier

AWS provides a Free Tier for new users.

It includes limited usage of popular services such as:

- Amazon EC2
- Amazon S3
- Amazon RDS
- AWS Lambda
- Amazon DynamoDB

Always monitor your usage to avoid unexpected charges.

---

# 🖥 AWS Management Console

The AWS Management Console is a web-based interface used to manage AWS services.

You can:

- Launch EC2 instances
- Create S3 buckets
- Manage IAM users
- Configure networking
- Monitor resources
- View billing information

---

# 💻 AWS CLI

AWS CLI (Command Line Interface) allows you to manage AWS services from the terminal.

## Install

Download the AWS CLI from the official AWS website.

Verify installation:

```bash
aws --version
```

Configure your account:

```bash
aws configure
```

You'll be prompted for:

- AWS Access Key ID
- AWS Secret Access Key
- Default Region
- Output Format

Useful commands:

```bash
aws s3 ls
```

List EC2 instances:

```bash
aws ec2 describe-instances
```

List IAM users:

```bash
aws iam list-users
```

---

# ⚙️ AWS SDK

AWS SDKs allow developers to interact with AWS services using programming languages.

Popular SDKs:

- Python (Boto3)
- Java
- JavaScript
- Go
- .NET
- PHP

Example use cases:

- Upload files to Amazon S3
- Start an EC2 instance
- Send notifications using Amazon SNS
- Access DynamoDB

---

# 🔒 Beginner Best Practices

- Enable MFA on the root account.
- Never use the root account for daily work.
- Create IAM users instead.
- Use strong passwords.
- Enable billing alerts.
- Delete unused resources.
- Follow the principle of least privilege.
- Monitor Free Tier usage regularly.

---

# 📚 AWS Learning Path

```
Cloud Fundamentals
        ↓
AWS Fundamentals
        ↓
Global Infrastructure
        ↓
IAM
        ↓
EC2
        ↓
VPC
        ↓
S3
        ↓
RDS
        ↓
Load Balancer
        ↓
Auto Scaling
        ↓
CloudWatch
        ↓
CloudTrail
        ↓
Docker on AWS
        ↓
ECS / EKS
        ↓
Terraform
        ↓
CI/CD
        ↓
Projects
```

---

# 📋 Quick Cheatsheet

| Topic | Key Point |
|--------|-----------|
| AWS | Cloud platform by Amazon |
| Region | Geographic area containing multiple AZs |
| Availability Zone | One or more isolated data centers within a Region |
| Edge Location | Improves content delivery and reduces latency |
| IAM | Identity and Access Management |
| EC2 | Virtual Machine |
| S3 | Object Storage |
| VPC | Private Virtual Network |
| RDS | Managed Relational Database |
| Route 53 | DNS Service |
| ELB | Load Balancer |
| Auto Scaling | Automatically adjusts resources |
| CloudWatch | Monitoring and Logging |
| CloudTrail | API Activity Logging |
| Lambda | Serverless Computing |

---

# ❓ Interview Questions

### Beginner

1. What is AWS?
2. What is the AWS Free Tier?
3. What is the AWS Management Console?
4. What is AWS CLI?
5. What is AWS SDK?
6. Why should you avoid using the root account?
7. What is MFA?
8. How do you configure AWS CLI?
9. Name five AWS services.
10. Which AWS service is used for object storage?

### Intermediate

- What is the difference between AWS CLI and AWS SDK?
- Why should IAM users be used instead of the root account?
- How can you prevent unexpected AWS charges?
- How do you secure a new AWS account?
- Explain the AWS account creation process.

---

# 📚 Learning Resources

## Official Resources

- AWS Documentation
- AWS Skill Builder
- AWS Cloud Practitioner Essentials
- AWS Well-Architected Framework
- AWS Architecture Center
- AWS Whitepapers
- AWS Workshops
- AWS FAQs

## Practice Platforms

- AWS Skill Builder
- AWS Workshops
- AWS Free Tier
- AWS Hands-on Labs

## Recommended YouTube Channels

- AWS
- freeCodeCamp.org
- TechWorld with Nana
- KodeKloud

---

# ✅ Congratulations!

You have completed the **AWS Introduction Module**.

You now understand:

- Cloud Computing
- AWS Fundamentals
- AWS Global Infrastructure
- AWS Account Setup
- AWS CLI
- AWS SDK
- AWS Best Practices

---
