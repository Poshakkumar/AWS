# 🌐 Amazon Route 53 Fundamentals

> Learn the core concepts of Amazon Route 53 including DNS, Hosted Zones, DNS Records, Alias Records, and Domain Registration.

---

# 📖 Table of Contents

- What is DNS?
- Domain Name
- Hosted Zone
- DNS Records
- Alias Record
- Domain Registration
- DNS Resolution
- Best Practices

---

# 🌍 What is DNS?

DNS (Domain Name System) converts domain names into IP addresses.

Example:

```text
google.com
      │
DNS Lookup
      │
142.250.xxx.xxx
```

Without DNS, users would need to remember IP addresses instead of domain names.

---

# 🌐 Domain Name

A domain name is the human-readable address of a website.

Examples:

```
amazon.com
google.com
mywebsite.in
```

---

# 📂 Hosted Zone

A Hosted Zone stores DNS records for a domain.

Example:

```
example.com
│
├── A Record
├── AAAA Record
├── CNAME
├── MX
└── TXT
```

There are two types:

- Public Hosted Zone
- Private Hosted Zone

---

# 📝 DNS Records

| Record | Purpose |
|---------|----------|
| A | Maps domain to IPv4 address |
| AAAA | Maps domain to IPv6 address |
| CNAME | Alias for another domain |
| MX | Mail server |
| TXT | Domain verification & SPF |
| NS | Name Servers |

---

# 🔗 Alias Record

Alias Records are AWS-specific DNS records.

They can point directly to:

- Application Load Balancer
- CloudFront Distribution
- S3 Static Website
- API Gateway

### Benefits

- No additional DNS lookup
- Automatically updates if the AWS resource changes
- No extra Route 53 query charges for supported AWS resources

---

# 🌍 Domain Registration

Route 53 allows you to register and manage domain names.

Example:

```
mycompany.com
```

AWS automatically configures the required Name Servers after registration.

---

# 🔄 DNS Resolution

```text
User
 │
 ▼
Browser
 │
 ▼
Route 53
 │
 ▼
DNS Record
 │
 ▼
EC2 / Load Balancer / S3
```

---

# ⭐ Best Practices

- Use Alias Records for AWS resources.
- Enable Health Checks for critical applications.
- Use meaningful DNS record names.
- Protect your domain with proper access controls.
- Use Private Hosted Zones for internal applications.

---

# 📝 Key Takeaways

- Route 53 is AWS's managed DNS service.
- Hosted Zones store DNS records.
- DNS records map domain names to resources.
- Alias Records are optimized for AWS services.
- Route 53 can register and manage domains.

---

# 🚀 Next Chapter

**02-routing-policies-health-checks.md**

Topics Covered:

- Simple Routing
- Weighted Routing
- Latency Routing
- Failover Routing
- Geolocation Routing
- Health Checks