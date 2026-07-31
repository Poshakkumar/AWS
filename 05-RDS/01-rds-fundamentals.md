# 🗄️ Amazon RDS Fundamentals

> Learn the core concepts of Amazon RDS including database engines, DB instances, storage, backups, snapshots, Multi-AZ deployments, and Read Replicas.

---

# 📖 Table of Contents

- DB Instance
- Database Engines
- Storage
- Automated Backups
- DB Snapshots
- Multi-AZ Deployment
- Read Replicas
- Multi-AZ vs Read Replica
- Best Practices

---

# 💻 DB Instance

A **DB Instance** is the database server that runs your chosen database engine.

It includes:

- CPU
- Memory
- Storage
- Database Engine
- Network Configuration

---

# 🗃️ Database Engines

| Engine | Common Use Case |
|---------|-----------------|
| MySQL | Web Applications |
| PostgreSQL | Enterprise Applications |
| MariaDB | Open Source Projects |
| Oracle | Enterprise Systems |
| SQL Server | Microsoft Applications |
| Aurora | High Performance AWS Database |

---

# 💾 Storage

Amazon RDS supports multiple storage options.

| Storage Type | Best For |
|--------------|-----------|
| General Purpose SSD (gp3) | Most workloads |
| Provisioned IOPS (io2) | High-performance databases |
| Magnetic | Legacy workloads |

Storage can be increased without downtime in most cases.

---

# 💽 Automated Backups

Amazon RDS automatically creates backups during the configured backup window.

Benefits:

- Point-in-Time Recovery
- Automatic recovery
- Data protection

Backup retention:

- 0–35 days

---

# 📸 DB Snapshots

A DB Snapshot is a manual backup of your database.

Unlike automated backups, snapshots remain until you delete them.

Use Cases:

- Long-term backup
- Database migration
- Testing

---

# 🌍 Multi-AZ Deployment

Multi-AZ creates a standby database in another Availability Zone.

Architecture:

```text
Primary Database
        │
Synchronous Replication
        │
Standby Database
```

Benefits:

- High Availability
- Automatic Failover
- Disaster Recovery

---

# 📖 Read Replicas

Read Replicas create read-only copies of the primary database.

Architecture:

```text
Primary Database
       │
Asynchronous Replication
       │
Read Replica
```

Use Cases:

- Read-heavy applications
- Reporting
- Analytics

---

# ⚖️ Multi-AZ vs Read Replica

| Multi-AZ | Read Replica |
|-----------|--------------|
| High Availability | Read Scaling |
| Synchronous Replication | Asynchronous Replication |
| Automatic Failover | No Automatic Failover |
| Disaster Recovery | Reporting & Analytics |

---

# ⭐ Best Practices

- Use Multi-AZ for production databases.
- Enable automated backups.
- Create manual snapshots before major updates.
- Use Read Replicas for heavy read traffic.
- Encrypt sensitive databases.
- Monitor database performance using CloudWatch.

---

# 📝 Key Takeaways

- Amazon RDS is a managed relational database service.
- Multi-AZ provides high availability.
- Read Replicas improve read performance.
- Automated Backups support point-in-time recovery.
- Snapshots are manual backups.

---

# 🚀 Next Chapter

**02-rds-high-availability-security.md**

Topics Covered:

- Security Groups
- IAM Authentication
- Encryption
- Monitoring
- Performance Insights
- Maintenance Windows
- Best Practices