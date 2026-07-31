# 🌍 AWS Global Infrastructure

> AWS Global Infrastructure is the worldwide network of data centers, Regions, Availability Zones (AZs), and Edge Locations that enables AWS to deliver secure, scalable, highly available, and low-latency cloud services.

---

# 📖 Table of Contents

- What is AWS Global Infrastructure?
- AWS Regions
- Availability Zones (AZs)
- Edge Locations
- Regional vs Global Services
- How to Choose an AWS Region
- High Availability
- Key Takeaways
- Interview Questions
- References

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Understand AWS Global Infrastructure
- Explain Regions and Availability Zones
- Understand Edge Locations
- Differentiate Regional and Global Services
- Choose the right AWS Region for your applications

---

# 🌍 What is AWS Global Infrastructure?

AWS Global Infrastructure is the worldwide network of AWS data centers that provides cloud services across different geographic locations.

It is designed to provide:

- High Availability
- Fault Tolerance
- Low Latency
- Scalability
- Disaster Recovery
- Global Reach

The infrastructure consists of:

- 🌎 Regions
- 🏢 Availability Zones (AZs)
- 🌐 Edge Locations

---

# 🌎 AWS Regions

A **Region** is a physical geographic location where AWS clusters multiple data centers.

Examples:

- US East (N. Virginia)
- US West (Oregon)
- Europe (Frankfurt)
- Asia Pacific (Mumbai)
- Asia Pacific (Singapore)

Each Region is completely independent from other Regions.

## Why Multiple Regions?

- Reduce latency
- Meet compliance requirements
- Disaster recovery
- Global application deployment

---

# 🏢 Availability Zones (AZs)

An **Availability Zone (AZ)** is one or more physically separate data centers within an AWS Region.

Each Region contains multiple AZs connected through high-speed, low-latency private networking.

Example:

```
Region (Mumbai)

├── AZ-A
├── AZ-B
└── AZ-C
```

### Benefits

- High Availability
- Fault Isolation
- Load Distribution
- Disaster Recovery

**Best Practice:** Always deploy production workloads across multiple Availability Zones.

---

# 🌐 Edge Locations

Edge Locations are AWS sites located closer to end users.

They are mainly used for content delivery and DNS services.

Services using Edge Locations include:

- Amazon CloudFront
- Amazon Route 53
- AWS WAF
- AWS Shield

### Benefits

- Lower latency
- Faster content delivery
- Better user experience
- Global caching

---

# 🔄 Regional vs Global Services

| Regional Services | Global Services |
|-------------------|-----------------|
| Amazon EC2 | AWS IAM |
| Amazon VPC | Amazon CloudFront |
| Amazon RDS | AWS Organizations |
| Amazon S3* | Amazon Route 53 |
| Amazon ECS | AWS WAF |

> **Note:** Amazon S3 buckets are created in a specific Region, even though the service itself is available globally.

---

# 📍 Choosing the Right AWS Region

When selecting a Region, consider:

- 📍 Distance from users
- 💰 Pricing
- 🌍 Service availability
- 📜 Legal and compliance requirements
- ⚡ Latency
- 🛡️ Disaster recovery strategy

Example:

- Indian users → Mumbai Region
- European users → Frankfurt Region
- US users → N. Virginia Region

---

# 🛡️ High Availability

AWS achieves High Availability by:

- Using multiple Availability Zones
- Load Balancers
- Auto Scaling
- Multi-AZ databases
- Redundant networking

This ensures applications remain available even if one Availability Zone experiences a failure.

---

# 📊 Infrastructure Overview

```
                     AWS Global Infrastructure

                            AWS
                             │
        ┌────────────────────┴────────────────────┐
        │                                         │
     Region 1                                 Region 2
        │                                         │
   ┌────┴────┐                             ┌──────┴─────┐
   │         │                             │            │
 AZ-A      AZ-B                         AZ-A         AZ-B
        │
        │
 Users ─────► Edge Location ─────► AWS Region
```

---

# 📝 Key Takeaways

- AWS operates a global network of cloud infrastructure.
- A Region is a geographic area containing multiple Availability Zones.
- Availability Zones are isolated data centers within a Region.
- Edge Locations improve content delivery and reduce latency.
- Production applications should use multiple AZs for high availability.
- Choose Regions based on latency, pricing, compliance, and service availability.

---

# ❓ Interview Questions

### Beginner

1. What is AWS Global Infrastructure?
2. What is an AWS Region?
3. What is an Availability Zone?
4. What is an Edge Location?
5. Why does AWS have multiple Regions?
6. Why should applications use multiple AZs?
7. Give examples of Global AWS Services.
8. Give examples of Regional AWS Services.
9. How do Edge Locations improve performance?
10. Which AWS Region would you choose for users in India?

---

# 📚 References

- AWS Documentation
- AWS Global Infrastructure Overview
- AWS Cloud Practitioner Essentials
- AWS Well-Architected Framework

---

## 🚀 Next Chapter

**04-pricing-security.md**

Topics Covered:

- AWS Pricing Model
- AWS Free Tier
- Shared Responsibility Model
- Cost Optimization Basics