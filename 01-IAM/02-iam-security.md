# 🔒 IAM Security

> IAM Security controls what identities can access and protects AWS accounts using policies and authentication mechanisms.

---

# 📖 Table of Contents

- IAM Policies
- MFA
- Password Policy
- Principle of Least Privilege
- IAM Best Practices

---

# 📜 IAM Policies

Policies are JSON documents that define permissions.

A policy answers:

- Who?
- What Action?
- Which Resource?

Example

```json
{
  "Effect": "Allow",
  "Action": "s3:*",
  "Resource": "*"
}
```

Policy Types

- AWS Managed Policies
- Customer Managed Policies
- Inline Policies

---

# 🔐 Multi-Factor Authentication (MFA)

MFA adds an extra security layer.

Login requires:

- Password
- OTP from Authenticator App

Benefits

- Protects Root User
- Prevents unauthorized access
- Recommended for every IAM user

---

# 🔑 Password Policy

A strong password policy includes:

- Minimum 8–12 characters
- Uppercase letters
- Lowercase letters
- Numbers
- Special characters
- Password expiration (optional)

---

# ⭐ Principle of Least Privilege

Always grant only the permissions required to perform a task.

❌ Bad

```

AdministratorAccess

```

✅ Good

```

ReadOnlyAccess

```

or

```

AmazonS3ReadOnlyAccess

```

---

# ✅ IAM Best Practices

- Never use Root User for daily work.
- Enable MFA.
- Create IAM Users.
- Use IAM Groups.
- Use IAM Roles for AWS Services.
- Avoid long-term Access Keys.
- Rotate credentials regularly.
- Follow Least Privilege.
- Remove unused users.
- Review permissions periodically.

---

# 📋 Summary

- Policies define permissions.
- MFA improves security.
- Least Privilege minimizes risk.
- Roles are preferred over hardcoded credentials.
- IAM is the first security layer in AWS.

---

# 🚀 Next File

03-hands-on-labs.md