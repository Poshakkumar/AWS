# 🔐 Amazon RDS High Availability & Security

> Learn how Amazon RDS provides security, high availability, monitoring, maintenance, and disaster recovery for production databases.

---

# 📖 Table of Contents

- Security Groups
- IAM Database Authentication
- Encryption
- Monitoring
- Performance Insights
- Maintenance Window
- Backup & Recovery
- Best Practices
- Key Takeaways

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Secure Amazon RDS
- Configure database access
- Monitor database performance
- Understand maintenance and backups
- Apply production-ready best practices

---

# 🛡 Security Groups

Amazon RDS uses **Security Groups** to control network access.

Example:

| Protocol | Port | Purpose |
|----------|------|---------|
| MySQL | 3306 | MySQL Database |
| PostgreSQL | 5432 | PostgreSQL Database |
| SQL Server | 1433 | SQL Server |
| Oracle | 1521 | Oracle Database |

> Only allow trusted EC2 instances or application servers to connect to your database.

---

# 👤 IAM Database Authentication

IAM Authentication allows users to connect to supported RDS databases using **IAM credentials** instead of database passwords.

### Benefits

- Improved security
- No hardcoded passwords
- Centralized access management
- Temporary authentication tokens

---

# 🔒 Encryption

Amazon RDS supports encryption for:

- Database Storage
- Automated Backups
- Snapshots
- Read Replicas

Encryption is managed using **AWS Key Management Service (KMS)**.

### Benefits

- Protects sensitive data
- Meets compliance requirements
- Secures backups and replicas

---

# 📊 Monitoring

Amazon RDS integrates with **Amazon CloudWatch**.

Monitor important metrics such as:

- CPU Utilization
- Memory Usage
- Storage Space
- Database Connections
- Read/Write Operations
- Network Throughput

Monitoring helps detect performance issues before they impact applications.

---

# ⚡ Performance Insights

Performance Insights helps identify slow SQL queries and database bottlenecks.

It provides:

- Database load analysis
- Query performance
- Wait events
- Performance history

---

# 🔄 Maintenance Window

AWS performs routine maintenance during the configured maintenance window.

Maintenance includes:

- Operating System Updates
- Database Engine Updates
- Security Patches
- Minor Version Upgrades

Choose a maintenance window during low-traffic hours.

---

# 💾 Backup & Recovery

Amazon RDS provides two backup options:

### Automated Backups

- Scheduled automatically
- Point-in-Time Recovery
- Retention: 0–35 days

### Manual Snapshots

- Created manually
- Stored until deleted
- Useful before upgrades or migrations

---

# 🏗 Production Architecture

```text
                Internet
                    │
          Application Load Balancer
                    │
              EC2 Application
                    │
        Amazon RDS (Primary)
                    │
      Synchronous Replication
                    │
        Standby DB (Multi-AZ)
                    │
          Automated Backups
                    │
          Amazon S3 Storage
```

---

# ⭐ Best Practices

- Enable Multi-AZ for production databases.
- Enable automated backups.
- Take manual snapshots before upgrades.
- Encrypt databases using AWS KMS.
- Restrict database access using Security Groups.
- Monitor performance using CloudWatch.
- Enable Performance Insights for troubleshooting.
- Use Read Replicas for read-heavy workloads.
- Rotate database credentials regularly.

---

# 📝 Key Takeaways

- Security Groups protect database access.
- IAM Authentication improves security.
- Encryption protects data at rest.
- CloudWatch monitors database health.
- Performance Insights helps optimize queries.
- Automated Backups and Snapshots support disaster recovery.
- Multi-AZ improves availability.

---

# 🚀 Next Module

## 🌍 Amazon Route 53

Topics Covered:

- What is Route 53?
- DNS Basics
- Hosted Zones
- DNS Records
- Routing Policies
- Health Checks
- Domain Registration