# 🎯 Route 53 Routing Policies & Health Checks

> Learn how Amazon Route 53 routes user requests using different routing policies and how Health Checks improve application availability.

---

# 📖 Table of Contents

- What are Routing Policies?
- Simple Routing
- Weighted Routing
- Latency Routing
- Failover Routing
- Geolocation Routing
- Geoproximity Routing
- Multi-Value Routing
- Health Checks
- Routing Policy Comparison
- Best Practices

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Understand Route 53 Routing Policies
- Configure traffic routing
- Improve application availability
- Perform health monitoring
- Select the right routing policy

---

# 🌐 What are Routing Policies?

Routing Policies determine **how Route 53 responds to DNS queries** and decides which AWS resource should receive the user's request.

---

# 1️⃣ Simple Routing

Simple Routing directs traffic to **one resource**.

### Example

```text
example.com
      │
      ▼
EC2 Instance
```

### Use Cases

- Single website
- Development environments
- Small applications

---

# 2️⃣ Weighted Routing

Weighted Routing distributes traffic based on assigned percentages.

### Example

```text
Users
 │
 ├── 80% → EC2-1
 └── 20% → EC2-2
```

### Use Cases

- A/B Testing
- Blue-Green Deployment
- Gradual application rollout

---

# 3️⃣ Latency Routing

Routes users to the AWS Region with the **lowest network latency**.

### Example

```text
India Users
      │
 Mumbai Region

USA Users
      │
 N. Virginia Region
```

### Benefits

- Faster response time
- Better user experience
- Global applications

---

# 4️⃣ Failover Routing

Automatically redirects traffic to a backup resource if the primary resource becomes unavailable.

### Example

```text
Primary Server
      │
 Health Check
      │
If Failed
      ▼
Backup Server
```

### Use Cases

- Disaster Recovery
- High Availability
- Business Continuity

---

# 5️⃣ Geolocation Routing

Routes traffic based on the **user's geographic location**.

### Example

```text
India → Mumbai Server

Europe → Frankfurt Server

USA → Virginia Server
```

### Use Cases

- Localized content
- Regional compliance
- Country-specific websites

---

# 6️⃣ Geoproximity Routing

Routes traffic based on the **physical distance** between users and AWS resources.

Traffic bias can be adjusted to shift more users toward a preferred Region.

### Use Cases

- Global applications
- Regional traffic optimization

---

# 7️⃣ Multi-Value Routing

Returns multiple healthy IP addresses in response to a DNS query.

If one resource becomes unhealthy, Route 53 automatically removes it from the response.

### Example

```text
example.com

↓

EC2-1
EC2-2
EC2-3
```

### Benefits

- Improved availability
- Basic load distribution

---

# ❤️ Health Checks

Health Checks continuously monitor your application or endpoint.

If a resource becomes unhealthy, Route 53 can stop sending traffic to it.

Health Checks monitor:

- HTTP
- HTTPS
- TCP

Example:

```text
Route 53

↓

Health Check

↓

Healthy ✅

↓

Send Traffic
```

---

# 📊 Routing Policy Comparison

| Policy | Best For |
|---------|----------|
| Simple | Single Resource |
| Weighted | Traffic Splitting |
| Latency | Lowest Response Time |
| Failover | Disaster Recovery |
| Geolocation | Country/Region Based Routing |
| Geoproximity | Distance-Based Routing |
| Multi-Value | High Availability |

---

# ⭐ Best Practices

- Use Latency Routing for global applications.
- Use Failover Routing with Health Checks.
- Use Weighted Routing for testing new releases.
- Use Geolocation Routing for regional content.
- Enable Health Checks for production workloads.
- Prefer Alias Records when routing to AWS resources.

---

# 📝 Key Takeaways

- Routing Policies control DNS traffic flow.
- Weighted Routing supports traffic splitting.
- Latency Routing improves user experience.
- Failover Routing increases availability.
- Health Checks monitor application health.
- Route 53 integrates seamlessly with AWS services.

---

# 🚀 Next Module

## ⚖️ Elastic Load Balancing (ELB)

Topics Covered:

- What is ELB?
- Types of Load Balancers
- Target Groups
- Health Checks
- Sticky Sessions
- SSL/TLS
- Cross-Zone Load Balancing