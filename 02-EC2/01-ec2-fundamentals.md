# 🖥️ Amazon EC2 Fundamentals

> Learn the core concepts of Amazon EC2, including instances, AMIs, instance types, key pairs, security groups, user data, and Elastic IPs.

---

# 📖 Table of Contents

- What is Amazon EC2?
- EC2 Workflow
- Amazon Machine Image (AMI)
- EC2 Instance Types
- Key Pair
- Security Group
- Elastic IP
- User Data
- Instance Lifecycle
- Key Takeaways

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Understand how Amazon EC2 works
- Launch an EC2 instance
- Choose the right AMI and Instance Type
- Secure an EC2 instance
- Connect to an instance using SSH
- Understand the EC2 lifecycle

---

# 🚀 What is Amazon EC2?

Amazon EC2 (Elastic Compute Cloud) is a service that allows you to create virtual servers (called **instances**) in the AWS Cloud.

Instead of buying physical servers, you can launch a virtual machine within minutes.

You only pay for the resources you use.

---

# 🔄 EC2 Launch Workflow

```text
Choose AMI
      ↓
Choose Instance Type
      ↓
Configure Network (VPC/Subnet)
      ↓
Attach Storage (EBS)
      ↓
Configure Security Group
      ↓
Create/Select Key Pair
      ↓
Launch EC2 Instance
```

---

# 💿 Amazon Machine Image (AMI)

An **Amazon Machine Image (AMI)** is a pre-configured template used to launch an EC2 instance.

An AMI contains:

- Operating System
- Application Server (optional)
- Software Packages
- Configuration Settings

### Common AMIs

| AMI | Purpose |
|------|---------|
| Amazon Linux | AWS recommended Linux OS |
| Ubuntu | Development & Web Servers |
| Red Hat Enterprise Linux | Enterprise workloads |
| Windows Server | Windows applications |

**Think of an AMI as a blueprint for creating an EC2 instance.**

---

# 💻 EC2 Instance Types

Instance Types define the CPU, memory, storage, and networking capacity of an EC2 instance.

### General Purpose

Balanced CPU and memory.

Examples:

- t2.micro
- t3.micro
- t3.small

Use Cases:

- Web servers
- Development
- Small applications

---

### Compute Optimized

High CPU performance.

Examples:

- C5
- C6

Use Cases:

- Gaming
- High-performance APIs
- Batch Processing

---

### Memory Optimized

High RAM.

Examples:

- R5
- R6

Use Cases:

- Databases
- Caching
- Analytics

---

### Storage Optimized

Fast local storage.

Examples:

- I3
- D2

Use Cases:

- Big Data
- Data Warehouses

---

# 🔑 Key Pair

A Key Pair is used to securely connect to a Linux EC2 instance using SSH.

It consists of:

- Public Key (stored by AWS)
- Private Key (.pem file stored by you)

### Linux Connection

```bash
ssh -i my-key.pem ec2-user@<Public-IP>
```

### Best Practices

- Never share your `.pem` file.
- Store it securely.
- Create separate keys for different environments.

---

# 🛡️ Security Group

A Security Group acts as a **virtual firewall** for an EC2 instance.

It controls:

- Inbound Traffic
- Outbound Traffic

### Example Rules

| Protocol | Port | Purpose |
|----------|------|---------|
| SSH | 22 | Remote Login |
| HTTP | 80 | Web Traffic |
| HTTPS | 443 | Secure Web Traffic |

> Security Groups are **stateful**, meaning return traffic is automatically allowed.

---

# 🌐 Elastic IP

An Elastic IP is a **static public IPv4 address** that you can associate with an EC2 instance.

### Why use Elastic IP?

- Static IP address
- Survives instance stop/start (when reassociated)
- Useful for production servers

> AWS charges for unused Elastic IPs.

---

# ⚙️ User Data

User Data is a script that runs automatically **only during the first boot** of an EC2 instance.

Example:

```bash
#!/bin/bash
yum update -y
yum install httpd -y
systemctl start httpd
systemctl enable httpd

echo "<h1>Hello from Amazon EC2</h1>" > /var/www/html/index.html
```

This script:

- Updates packages
- Installs Apache
- Starts the web server
- Creates a simple webpage

---

# 🔄 EC2 Instance Lifecycle

```text
Launch
   │
Pending
   │
Running
   │
───────────────
│      │      │
Stop  Reboot Terminate
│
Start
```

### States

| State | Description |
|-------|-------------|
| Pending | Instance is starting |
| Running | Instance is active |
| Stopped | Compute is stopped, storage remains |
| Rebooting | Restarting the OS |
| Terminated | Permanently deleted |

---

# 💼 Real-World Example

A company hosts its website on an EC2 instance.

- **Amazon Linux AMI** → Operating System
- **t3.micro** → Instance Type
- **Security Group** → Allows HTTP (80) and HTTPS (443)
- **Elastic IP** → Static public IP
- **User Data** → Automatically installs Nginx during launch

---

# 📝 Key Takeaways

- EC2 provides virtual servers in AWS.
- AMIs are templates used to launch instances.
- Instance Types determine CPU, RAM, and storage.
- Key Pairs provide secure SSH access.
- Security Groups act as virtual firewalls.
- Elastic IP provides a static public IP address.
- User Data automates instance setup.

---

# 🚀 Next Chapter

**02-ec2-storage-networking.md**

Topics Covered:

- Amazon EBS
- EBS Snapshots
- Instance Store
- ENI (Elastic Network Interface)
- Placement Groups
- Launch Templates
- Auto Recovery