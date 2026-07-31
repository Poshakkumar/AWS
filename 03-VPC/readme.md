# 🌐 Amazon VPC (Virtual Private Cloud)

> Amazon VPC (Virtual Private Cloud) enables you to create an isolated virtual network within AWS where you can securely launch and manage your cloud resources. It gives you full control over networking, IP addressing, routing, and security.

---

# 📖 Table of Contents

- What is Amazon VPC?
- Why Use VPC?
- VPC Components
- Common Architecture
- Learning Roadmap
- Module Structure

---

# 🎯 Learning Objectives

After completing this module, you will be able to:

- Understand Amazon VPC
- Design secure network architectures
- Configure subnets and routing
- Connect resources to the internet
- Control network traffic
- Build highly available applications

---

# 🚀 What is Amazon VPC?

Amazon VPC is a logically isolated virtual network inside AWS.

It allows you to launch AWS resources like EC2, RDS, and Load Balancers inside your own private network.

You control:

- IP Address Range
- Subnets
- Route Tables
- Internet Access
- Security Rules

---

# ❓ Why Use Amazon VPC?

Without VPC:

- No network isolation
- Limited security
- Difficult traffic management

With VPC:

- Private networking
- Secure communication
- Controlled internet access
- Better scalability
- High availability

---

# 🧩 VPC Components

- VPC
- CIDR Block
- Public Subnet
- Private Subnet
- Route Table
- Internet Gateway
- NAT Gateway
- Security Group
- Network ACL
- Elastic IP

---

# 🏗 Typical VPC Architecture

```text
                    Internet
                        │
                Internet Gateway
                        │
                Amazon VPC
      ┌─────────────────┴─────────────────┐
      │                                   │
 Public Subnet                     Private Subnet
      │                                   │
    EC2 + ALB                         RDS Database
```

---

# 📚 Module Structure

```text
03-VPC/
│
├── README.md
├── 01-vpc-fundamentals.md
├── 02-vpc-security-routing.md
```

---

# 🚀 Learning Roadmap

```text
VPC
   ↓
CIDR
   ↓
Subnets
   ↓
Route Tables
   ↓
Internet Gateway
   ↓
NAT Gateway
   ↓
Security Group
   ↓
Network ACL
```

---

## 🚀 Next File

**01-vpc-fundamentals.md**