# 🚀 Advanced Elastic Load Balancing

> Learn advanced ELB concepts including Sticky Sessions, SSL/TLS, Cross-Zone Load Balancing, Connection Draining, and Auto Scaling integration.

---

# 📖 Table of Contents

- Sticky Sessions
- SSL/TLS
- Cross-Zone Load Balancing
- Deregistration Delay
- Auto Scaling Integration
- Monitoring
- Best Practices
- Key Takeaways

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

- Configure Sticky Sessions
- Secure applications with HTTPS
- Balance traffic across Availability Zones
- Handle instance removal gracefully
- Integrate ELB with Auto Scaling

---

# 🍪 Sticky Sessions

Sticky Sessions (Session Affinity) ensure that requests from the same user are sent to the same backend server for a specific duration.

### Example

```text
User

↓

ALB

↓

EC2-1

↓

Future Requests

↓

EC2-1
```

### Use Cases

- Shopping Cart
- User Login Sessions
- Legacy Applications

---

# 🔐 SSL/TLS

SSL/TLS encrypts communication between clients and the Load Balancer.

### HTTP

```text
User
 │
HTTP (Unencrypted)
 │
ALB
```

### HTTPS

```text
User
 │
HTTPS (Encrypted)
 │
ALB
```

Benefits

- Secure communication
- Protects sensitive data
- Required for production applications

AWS Certificate Manager (ACM) can be used to create and manage SSL certificates.

---

# 🌍 Cross-Zone Load Balancing

Cross-Zone Load Balancing distributes traffic evenly across all healthy targets in all enabled Availability Zones.

Without Cross-Zone:

```text
AZ-A → EC2-1
AZ-B → EC2-2
```

Traffic may become uneven.

With Cross-Zone:

```text
Users
 │
ALB
 │
├── EC2-1 (AZ-A)
├── EC2-2 (AZ-A)
├── EC2-3 (AZ-B)
└── EC2-4 (AZ-B)
```

Benefits

- Better traffic distribution
- Improved availability
- Efficient resource utilization

---

# ⏳ Deregistration Delay (Connection Draining)

When an EC2 instance is removed from the Target Group, ELB waits for existing requests to finish before stopping traffic.

Benefits

- No interrupted user requests
- Smooth deployments
- Better user experience

---

# 📈 Auto Scaling Integration

ELB works closely with Auto Scaling Groups.

### Workflow

```text
High Traffic
      │
Auto Scaling launches new EC2
      │
EC2 automatically joins Target Group
      │
ELB starts sending traffic
```

If traffic decreases:

```text
Low Traffic
      │
Auto Scaling terminates EC2
      │
ELB stops routing traffic
```

---

# 📊 Monitoring

Monitor ELB using **Amazon CloudWatch**.

Important metrics:

- Request Count
- Target Response Time
- Healthy Host Count
- Unhealthy Host Count
- HTTP 4XX Errors
- HTTP 5XX Errors

---

# 🏗 Production Architecture

```text
                Internet
                    │
               Amazon Route 53
                    │
        Application Load Balancer
              /              \
      EC2 (AZ-1)          EC2 (AZ-2)
             \              /
          Auto Scaling Group
                    │
              Amazon RDS
```

---

# ⭐ Best Practices

- Use HTTPS with ACM certificates.
- Enable Cross-Zone Load Balancing.
- Configure Health Checks correctly.
- Enable Deregistration Delay.
- Integrate ELB with Auto Scaling.
- Deploy instances in multiple Availability Zones.
- Monitor ELB metrics using CloudWatch.

---

# 📝 Key Takeaways

- Sticky Sessions keep users connected to the same backend.
- SSL/TLS secures client communication.
- Cross-Zone Load Balancing improves traffic distribution.
- Deregistration Delay prevents interrupted requests.
- ELB and Auto Scaling work together for automatic scaling.
- CloudWatch helps monitor ELB performance.

---

# 🚀 Next Module

## 📈 Amazon EC2 Auto Scaling

Topics Covered:

- What is Auto Scaling?
- Launch Templates
- Auto Scaling Groups
- Scaling Policies
- Dynamic Scaling
- Scheduled Scaling
- Health Checks