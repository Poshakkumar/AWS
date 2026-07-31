# 📈 Amazon EC2 Auto Scaling Fundamentals

> Learn the core concepts of Amazon EC2 Auto Scaling including Launch Templates, Auto Scaling Groups, Desired Capacity, Minimum Capacity, Maximum Capacity, and Health Checks.

---

# 📖 Table of Contents

- Launch Template
- Auto Scaling Group (ASG)
- Desired, Minimum & Maximum Capacity
- Health Checks
- Scaling Workflow
- Best Practices

---

# 🚀 Launch Template

A Launch Template stores the configuration required to launch EC2 instances.

It includes:

- Amazon Machine Image (AMI)
- Instance Type
- Security Group
- Key Pair
- IAM Role
- Storage (EBS)
- User Data

Using Launch Templates ensures every new EC2 instance is created with the same configuration.

---

# 👥 Auto Scaling Group (ASG)

An Auto Scaling Group manages a collection of EC2 instances.

It automatically:

- Launches new instances
- Replaces unhealthy instances
- Removes unnecessary instances

Example:

```text
          Auto Scaling Group
         /        |        \
      EC2-1    EC2-2    EC2-3
```

---

# 📊 Capacity Settings

### Minimum Capacity

The minimum number of EC2 instances that must always be running.

Example:

```
Minimum = 2
```

---

### Desired Capacity

The number of instances Auto Scaling tries to maintain.

Example:

```
Desired = 3
```

---

### Maximum Capacity

The highest number of EC2 instances that Auto Scaling can launch.

Example:

```
Maximum = 10
```

---

# ❤️ Health Checks

Auto Scaling continuously monitors EC2 instances.

If an instance becomes unhealthy:

```text
EC2 Failed
     │
Terminate
     │
Launch New EC2
```

This helps maintain application availability.

---

# 🔄 Auto Scaling Workflow

```text
High Traffic
      │
CloudWatch Alarm
      │
Auto Scaling Group
      │
Launch New EC2
      │
Register with Load Balancer
```

---

# 🏗 Production Architecture

```text
             Internet
                 │
           Amazon Route 53
                 │
       Application Load Balancer
                 │
        Auto Scaling Group
          /             \
     EC2 (AZ-1)     EC2 (AZ-2)
                 │
            Amazon RDS
```

---

# ⭐ Best Practices

- Use Launch Templates instead of Launch Configurations.
- Deploy across multiple Availability Zones.
- Integrate Auto Scaling with ELB.
- Configure Health Checks properly.
- Monitor scaling events using CloudWatch.
- Set realistic minimum and maximum capacities.

---

# 📝 Key Takeaways

- Launch Templates define EC2 configuration.
- Auto Scaling Groups manage EC2 instances.
- Desired Capacity maintains the target number of instances.
- Health Checks automatically replace failed instances.
- Auto Scaling improves availability and reduces costs.

---

# 🚀 Next Chapter

**02-scaling-policies-monitoring.md**

Topics Covered:

- Dynamic Scaling
- Target Tracking
- Step Scaling
- Simple Scaling
- Scheduled Scaling
- Cooldown Period
- CloudWatch Integration