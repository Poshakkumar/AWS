# 📈 Amazon CloudWatch Fundamentals

> Learn the core concepts of Amazon CloudWatch including Metrics, Namespaces, Dimensions, Dashboards, and CloudWatch Agent.

---

# 📖 Table of Contents

- Metrics
- Namespaces
- Dimensions
- CloudWatch Dashboards
- CloudWatch Agent
- Monitoring Workflow
- Best Practices

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Understand CloudWatch Metrics
- Organize monitoring data
- Build Dashboards
- Collect custom metrics
- Monitor applications effectively

---

# 📊 Metrics

A Metric is a measurable value that represents the performance of a resource.

Examples:

- CPU Utilization
- Memory Usage*
- Disk Usage*
- Network In
- Network Out
- Request Count

> *Memory and Disk metrics require the CloudWatch Agent.

---

# 📂 Namespaces

A Namespace groups related metrics.

Examples:

```text
AWS/EC2

AWS/RDS

AWS/S3

AWS/Lambda
```

Custom applications can also create their own namespaces.

---

# 🏷 Dimensions

Dimensions are key-value pairs that identify a specific resource.

Example:

```text
Metric:
CPUUtilization

Dimension:
InstanceId=i-123456789
```

This allows CloudWatch to monitor individual resources.

---

# 📊 CloudWatch Dashboards

Dashboards provide a centralized view of multiple metrics.

You can monitor:

- EC2 CPU
- ELB Requests
- RDS Connections
- Lambda Invocations
- Auto Scaling Activity

All in one place.

---

# 🖥 CloudWatch Agent

The CloudWatch Agent collects additional metrics from EC2 instances.

It can monitor:

- Memory Usage
- Disk Space
- Disk I/O
- Processes
- Log Files

Install the agent when you need operating system-level monitoring.

---

# 🔄 Monitoring Workflow

```text
AWS Resource
      │
CloudWatch Metrics
      │
Dashboard
      │
Alarm
      │
SNS Notification / Auto Scaling
```

---

# ⭐ Best Practices

- Use Dashboards for centralized monitoring.
- Install the CloudWatch Agent on EC2 instances.
- Monitor both infrastructure and application metrics.
- Organize metrics using Namespaces.
- Use Dimensions to monitor individual resources.

---

# 📝 Key Takeaways

- Metrics measure resource performance.
- Namespaces organize metrics.
- Dimensions identify specific resources.
- Dashboards visualize monitoring data.
- CloudWatch Agent collects additional system metrics.

---

# 🚀 Next Chapter

**02-cloudwatch-logs-alarms.md**

Topics Covered:

- CloudWatch Logs
- Log Groups
- Log Streams
- Alarms
- SNS Notifications
- EventBridge
- Log Retention