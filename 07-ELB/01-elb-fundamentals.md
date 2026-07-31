# ⚖️ Elastic Load Balancing Fundamentals

> Learn the core concepts of Elastic Load Balancing including ALB, NLB, GWLB, Target Groups, Listeners, and Health Checks.

---

# 📖 Table of Contents

- Types of ELB
- Target Groups
- Listeners
- Health Checks
- Request Flow
- Best Practices

---

# 🌍 Types of Load Balancers

## 1️⃣ Application Load Balancer (ALB)

Works at **Layer 7 (Application Layer)**.

Supports:

- HTTP
- HTTPS
- Host-based Routing
- Path-based Routing
- WebSocket
- HTTP/2

### Example

```text
example.com

        │

      ALB

   ┌────┴────┐

 /api      /images

EC2-1      EC2-2
```

Best For

- Websites
- REST APIs
- Microservices

---

## 2️⃣ Network Load Balancer (NLB)

Works at **Layer 4 (Transport Layer)**.

Supports:

- TCP
- UDP
- TLS

Benefits

- Ultra-low latency
- High performance
- Millions of requests

Best For

- Gaming
- Financial applications
- Real-time systems

---

## 3️⃣ Gateway Load Balancer (GWLB)

Works at **Layer 3 & Layer 4**.

Used for:

- Firewalls
- Intrusion Detection
- Security Appliances

---

## 4️⃣ Classic Load Balancer (CLB)

Legacy Load Balancer.

Supports:

- HTTP
- HTTPS
- TCP

AWS recommends using ALB or NLB for new applications.

---

# 🎯 Target Groups

A Target Group is a collection of backend resources that receive traffic.

Targets can be:

- EC2 Instances
- IP Addresses
- Lambda Functions

Example

```text
ALB

↓

Target Group

↓

EC2-1

EC2-2

EC2-3
```

---

# 🎧 Listeners

A Listener checks incoming requests on a specific protocol and port.

Example

| Protocol | Port |
|----------|------|
| HTTP | 80 |
| HTTPS | 443 |

The listener forwards traffic to the appropriate Target Group.

---

# ❤️ Health Checks

Health Checks continuously verify whether targets are healthy.

Healthy targets receive traffic.

Unhealthy targets are automatically removed until they recover.

---

# 🔄 Request Flow

```text
User

↓

Route 53

↓

Application Load Balancer

↓

Target Group

↓

EC2 Instances
```

---

# ⭐ Best Practices

- Use ALB for web applications.
- Use NLB for high-performance TCP/UDP workloads.
- Configure Health Checks correctly.
- Deploy targets across multiple Availability Zones.
- Enable HTTPS for secure communication.

---

# 📝 Key Takeaways

- ELB distributes incoming traffic.
- ALB works at Layer 7.
- NLB works at Layer 4.
- GWLB integrates security appliances.
- Target Groups contain backend resources.
- Health Checks improve availability.

---

# 🚀 Next Chapter

**02-elb-advanced.md**

Topics Covered:

- Sticky Sessions
- SSL/TLS
- Cross-Zone Load Balancing
- Connection Draining
- Integration with Auto Scaling