# 🌐 Amazon VPC Fundamentals

> Learn the core networking concepts of Amazon VPC, including CIDR blocks, subnets, route tables, Internet Gateways, NAT Gateways, Security Groups, and Network ACLs.

---

# 📖 Table of Contents

- What is VPC?
- CIDR Block
- Public & Private Subnets
- Route Tables
- Internet Gateway
- NAT Gateway
- Security Groups
- Network ACLs
- VPC Workflow
- Best Practices

---

# 🌐 What is Amazon VPC?

A Virtual Private Cloud (VPC) is your own isolated network inside AWS.

It allows you to securely deploy AWS resources while controlling networking and security.

Think of it as your own private data center in the cloud.

---

# 📍 CIDR Block

CIDR (Classless Inter-Domain Routing) defines the IP address range of your VPC.

Example:

```text
10.0.0.0/16
```

This provides IP addresses for resources inside the VPC.

Example subnet ranges:

```text
VPC

10.0.0.0/16

├── 10.0.1.0/24
├── 10.0.2.0/24
└── 10.0.3.0/24
```

---

# 🌍 Public Subnet

A Public Subnet has a route to the Internet Gateway.

Resources inside can access the internet.

Common Resources:

- Web Server
- Bastion Host
- Load Balancer

---

# 🔒 Private Subnet

A Private Subnet has **no direct internet access**.

Common Resources:

- Databases
- Internal APIs
- Backend Services

---

# 🛣 Route Table

A Route Table determines where network traffic should go.

Example:

| Destination | Target |
|------------|--------|
| Local | VPC |
| 0.0.0.0/0 | Internet Gateway |

---

# 🌍 Internet Gateway (IGW)

An Internet Gateway connects a VPC to the internet.

Without an IGW:

- No public internet access

Use Cases:

- Public EC2
- Web Servers
- Public APIs

---

# 🚪 NAT Gateway

A NAT Gateway allows resources in a **Private Subnet** to access the internet **without allowing inbound internet traffic**.

Example:

```text
Private EC2
      │
NAT Gateway
      │
Internet Gateway
      │
Internet
```

Use Cases:

- Software updates
- Package downloads
- API access

---

# 🛡 Security Groups

Security Groups protect individual AWS resources.

Characteristics:

- Stateful
- Instance-level firewall
- Allow rules only

---

# 🚧 Network ACL (NACL)

Network ACL protects the subnet.

Characteristics:

- Stateless
- Subnet-level firewall
- Allow and Deny rules

---

# ⚖ Security Group vs NACL

| Security Group | Network ACL |
|---------------|-------------|
| Instance Level | Subnet Level |
| Stateful | Stateless |
| Allow Rules Only | Allow & Deny Rules |
| Easier to Manage | More Granular Control |

---

# 🔄 VPC Traffic Flow

```text
Internet
    │
Internet Gateway
    │
Public Subnet
    │
Application Load Balancer
    │
Private EC2
    │
Amazon RDS
```

---

# ⭐ Best Practices

- Use multiple Availability Zones.
- Keep databases in Private Subnets.
- Use NAT Gateway for outbound internet access.
- Restrict Security Group rules.
- Apply least-privilege network access.
- Enable VPC Flow Logs for monitoring.

---

# 📝 Key Takeaways

- A VPC is an isolated network in AWS.
- CIDR defines the IP range.
- Public Subnets have internet access.
- Private Subnets do not have direct internet access.
- Internet Gateway provides internet connectivity.
- NAT Gateway enables secure outbound internet access.
- Security Groups protect instances.
- NACLs protect subnets.

---

# 🚀 Next Chapter

**02-vpc-security-routing.md**

Topics Covered:

- VPC Peering
- Transit Gateway
- VPC Endpoints
- DHCP Options
- DNS in VPC
- VPC Flow Logs