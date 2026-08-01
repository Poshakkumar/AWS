# ⚡ AWS Lambda Fundamentals

> Learn the core concepts of AWS Lambda including Serverless Computing, Function Lifecycle, Event Sources, Execution Roles, and Triggers.

---

# 📖 Table of Contents

- Serverless Computing
- Lambda Function
- Event Sources
- Triggers
- Execution Role
- Function Lifecycle
- Best Practices

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Understand Serverless Computing
- Create Lambda Functions
- Configure Triggers
- Manage IAM Execution Roles
- Understand Function Execution

---

# ☁️ What is Serverless Computing?

Serverless means you don't manage servers.

AWS automatically handles:

- Infrastructure
- Scaling
- Availability
- Maintenance

You only focus on writing code.

---

# ⚡ Lambda Function

A Lambda Function is a piece of code that runs when triggered by an event.

Supported Languages:

- Python
- Node.js
- Java
- Go
- C#
- Ruby

---

# 🎯 Event Sources

Lambda can be triggered by many AWS services.

Common Event Sources:

- Amazon S3
- Amazon API Gateway
- Amazon EventBridge
- Amazon DynamoDB
- Amazon SQS
- Amazon SNS
- Amazon CloudWatch

---

# 🔔 Triggers

A Trigger is an event that invokes a Lambda function.

Example:

```text
Image Uploaded to S3
        │
        ▼
AWS Lambda
        │
        ▼
Resize Image
```

---

# 👤 Execution Role

Every Lambda function uses an **IAM Execution Role**.

It grants permissions to access other AWS services.

Example:

```text
Lambda
   │
IAM Role
   │
Amazon S3
CloudWatch
DynamoDB
```

Follow the **Principle of Least Privilege** by granting only the permissions the function needs.

---

# 🔄 Function Lifecycle

```text
Event
   │
   ▼
Lambda Invoked
   │
   ▼
Code Executes
   │
   ▼
Response Returned
```

Lambda automatically scales by running multiple instances when needed.

---

# ⭐ Best Practices

- Keep functions small and focused.
- Use IAM roles with minimum permissions.
- Store secrets in AWS Secrets Manager or Parameter Store.
- Monitor functions using CloudWatch.
- Set appropriate timeout and memory values.

---

# 📝 Key Takeaways

- Lambda is a serverless compute service.
- Functions run only when triggered.
- Event Sources invoke Lambda automatically.
- IAM Execution Roles control permissions.
- Lambda scales automatically.

---

# 🚀 Next Chapter

**02-lambda-advanced.md**

Topics Covered:

- Layers
- Versions
- Aliases
- Concurrency
- Dead Letter Queue (DLQ)
- Error Handling
- Monitoring