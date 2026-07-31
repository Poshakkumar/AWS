# 💾 Amazon EC2 Storage & Networking

> Learn how Amazon EC2 uses storage and networking services such as Amazon EBS, EBS Snapshots, Instance Store, Elastic Network Interface (ENI), Placement Groups, Launch Templates, and Auto Recovery.

---

# 📖 Table of Contents

- Amazon EBS
- EBS Volume Types
- EBS Snapshots
- Instance Store
- Elastic Network Interface (ENI)
- Placement Groups
- Launch Templates
- Auto Recovery
- EBS vs Instance Store
- Key Takeaways

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Understand Amazon EBS
- Differentiate EBS and Instance Store
- Create and restore Snapshots
- Understand ENI
- Use Placement Groups
- Create Launch Templates

---

# 💾 Amazon Elastic Block Store (EBS)

Amazon EBS (Elastic Block Store) provides **persistent block storage** for Amazon EC2 instances.

Think of it as a virtual hard disk attached to your EC2 instance.

Features:

- Persistent Storage
- High Performance
- Encryption Support
- Snapshots
- Resize Volumes
- SSD & HDD Options

---

# 📦 EBS Volume Types

| Volume Type | Best For |
|-------------|----------|
| gp3 | General-purpose SSD (Recommended) |
| gp2 | Previous generation SSD |
| io2 | High-performance databases |
| st1 | Throughput-intensive HDD |
| sc1 | Cold HDD storage |

---

# 📸 EBS Snapshots

An **EBS Snapshot** is a backup of an EBS volume stored in Amazon S3.

Use Cases:

- Backup
- Disaster Recovery
- Restore Volumes
- Create New Volumes

Workflow:

```text
EBS Volume
      │
Create Snapshot
      │
Stored in Amazon S3
      │
Restore Anytime
```

---

# 💽 Instance Store

Instance Store provides **temporary storage** directly attached to the physical host.

Characteristics:

- Very fast
- Temporary
- Data is lost if the instance is stopped or terminated
- Suitable for cache and temporary files

---

# ⚖️ EBS vs Instance Store

| Amazon EBS | Instance Store |
|------------|----------------|
| Persistent | Temporary |
| Backups supported | No backups |
| Snapshots available | No snapshots |
| Detachable | Not detachable |
| Best for databases | Best for cache and temporary data |

---

# 🌐 Elastic Network Interface (ENI)

An ENI is a virtual network card attached to an EC2 instance.

Each ENI includes:

- Private IPv4 Address
- Public IPv4 (optional)
- IPv6 Address
- MAC Address
- Security Groups

Benefits:

- Multiple network interfaces
- Easy failover
- Flexible networking

---

# 🏢 Placement Groups

Placement Groups control how EC2 instances are physically placed within AWS infrastructure.

### Cluster

- Low latency
- High throughput
- HPC workloads

### Spread

- Maximum fault tolerance
- Instances placed on different hardware

### Partition

- Large distributed systems
- Hadoop
- Cassandra

---

# 📄 Launch Templates

Launch Templates store EC2 launch configurations.

They include:

- AMI
- Instance Type
- Security Group
- Key Pair
- Storage
- IAM Role
- User Data

Benefits:

- Reusable configuration
- Auto Scaling integration
- Faster deployments

---

# 🔄 Auto Recovery

AWS can automatically recover an EC2 instance if the underlying hardware fails.

Benefits:

- Reduced downtime
- Automatic recovery
- No manual intervention

---

# 🏗 Real-World Example

An e-commerce application uses:

- Amazon Linux AMI
- t3.medium EC2 Instance
- gp3 EBS Volume
- Daily EBS Snapshots
- Launch Template
- Auto Scaling Group
- Elastic Load Balancer

This architecture provides scalability, high availability, and disaster recovery.

---

# 📋 Best Practices

- Use gp3 volumes for most workloads.
- Schedule regular EBS Snapshots.
- Encrypt EBS volumes.
- Use Launch Templates for consistency.
- Avoid storing important data on Instance Store.
- Monitor EBS performance using Amazon CloudWatch.
- Use Placement Groups only when required.

---

# 📝 Key Takeaways

- Amazon EBS provides persistent storage.
- Snapshots are stored in Amazon S3.
- Instance Store is temporary.
- ENI is a virtual network interface.
- Launch Templates simplify EC2 deployments.
- Placement Groups optimize instance placement.
- Auto Recovery minimizes downtime.

---

# 🚀 Next Chapter

**03-hands-on-labs.md**

Labs Include:

- Launch an EC2 Instance
- Connect using SSH
- Install Nginx
- Create an EBS Volume
- Attach & Mount EBS
- Create an EBS Snapshot
- Allocate an Elastic IP
