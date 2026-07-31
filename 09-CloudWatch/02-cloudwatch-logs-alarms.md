# 📋 Amazon CloudWatch Logs & Alarms

> Learn how Amazon CloudWatch collects logs, creates alarms, sends notifications, and automates responses to keep AWS applications healthy.

---

# 📖 Table of Contents

- CloudWatch Logs
- Log Groups
- Log Streams
- CloudWatch Alarms
- Amazon SNS Integration
- Amazon EventBridge
- Log Retention
- Best Practices
- Key Takeaways

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Collect and manage logs
- Create CloudWatch Alarms
- Send notifications using Amazon SNS
- Automate workflows with EventBridge
- Configure log retention policies

---

# 📜 CloudWatch Logs

CloudWatch Logs is used to collect, store, and monitor log files from AWS services and applications.

Sources include:

- Amazon EC2
- AWS Lambda
- Amazon ECS
- Amazon EKS
- Application Logs
- System Logs

Benefits:

- Centralized logging
- Easy troubleshooting
- Security monitoring

---

# 📂 Log Groups

A Log Group is a container that organizes related log streams.

Example:

```text
Application Logs
│
├── EC2 Logs
├── Lambda Logs
└── ECS Logs
```

Use separate Log Groups for different applications or environments.

---

# 📄 Log Streams

A Log Stream contains log events from a specific resource.

Example:

```text
Log Group
      │
      ├── EC2-Instance-1
      ├── EC2-Instance-2
      └── EC2-Instance-3
```

Each EC2 instance or Lambda function typically writes to its own Log Stream.

---

# 🚨 CloudWatch Alarms

CloudWatch Alarms monitor metrics and trigger actions when thresholds are reached.

### Example

```text
CPU > 80%

↓

Alarm Triggered

↓

Send Notification

↓

Scale Application
```

Alarm States:

- OK
- ALARM
- INSUFFICIENT_DATA

---

# 📩 Amazon SNS Integration

CloudWatch Alarms can send notifications using Amazon Simple Notification Service (SNS).

Example:

```text
CloudWatch Alarm
        │
        ▼
     SNS Topic
        │
        ├── Email
        ├── SMS
        └── Lambda
```

Use Cases:

- Email alerts
- SMS notifications
- Incident response automation

---

# ⚡ Amazon EventBridge

Amazon EventBridge responds to AWS events and automates actions.

Example:

```text
EC2 Instance Stopped
        │
        ▼
   EventBridge Rule
        │
        ▼
 Lambda Function / SNS
```

Common Use Cases:

- Auto-remediation
- Scheduled jobs
- Workflow automation

---

# 🗑 Log Retention

Log Retention controls how long CloudWatch stores logs.

Examples:

- 7 Days
- 30 Days
- 90 Days
- 1 Year
- Never Expire

Choose a retention period based on compliance and cost requirements.

---

# 🏗 Monitoring Architecture

```text
EC2 / Lambda / RDS
         │
         ▼
 CloudWatch Metrics & Logs
         │
         ▼
 CloudWatch Alarm
         │
         ▼
      SNS Topic
         │
         ▼
 Email / SMS / Lambda
```

---

# ⭐ Best Practices

- Create alarms for critical metrics.
- Use SNS for instant notifications.
- Organize logs using Log Groups.
- Set appropriate log retention periods.
- Monitor application and infrastructure logs.
- Automate responses with EventBridge.
- Review alarms regularly to reduce false alerts.

---

# 📝 Key Takeaways

- CloudWatch Logs centralize application and system logs.
- Log Groups organize related logs.
- Log Streams contain logs from individual resources.
- CloudWatch Alarms monitor metrics and trigger actions.
- SNS sends notifications.
- EventBridge automates AWS workflows.
- Log Retention helps control storage costs.

---

# 🚀 Next Module

## 🛡️ AWS CloudTrail

Topics Covered:

- What is CloudTrail?
- Event History
- Management Events
- Data Events
- Insights
- Trail Creation
- Security & Auditing