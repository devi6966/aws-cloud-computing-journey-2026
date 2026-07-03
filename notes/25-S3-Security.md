# Amazon S3 Security

## What is S3 Security?

Amazon S3 Security is used to control who can access an S3 bucket or the objects stored inside it.

It provides different permission methods to securely manage access to S3 resources.

---

## 1. IAM Policy (User-Based Security)

IAM Policy is attached to an IAM User, Group, or Role.

It defines what actions a user is allowed to perform on an S3 bucket.

Examples:
- Upload Object
- Download Object
- Delete Object

Remember:

Human User → IAM Policy

---

## 2. Bucket Policy (Resource-Based Security)

Bucket Policy is attached directly to an S3 Bucket.

It is written in JSON format and controls who can access the bucket or its objects.

A Bucket Policy contains:

- Resource
- Effect (Allow / Deny)
- Action
- Principal

Common Uses:

- Public Access
- Cross-Account Access
- Enforce Encryption

Remember:

Permission is attached to the Bucket, not the User.

---

## 3. Access Control List (ACL)

ACL is an older permission mechanism used to control access.

Types:
- Bucket ACL
- Object ACL

Today, ACL is rarely used because IAM Policies and Bucket Policies are more flexible.

Remember:

ACL is a legacy permission method and can be disabled.

---

## 4. Public Access

Bucket Policy can make an S3 bucket publicly accessible.

Example:

A website stores its images in S3 so that anyone on the internet can view them.

Remember:

Public Access is usually configured using Bucket Policy.

---

## 5. Cross-Account Access

Bucket Policy can allow another AWS Account to access your bucket.

Example:

Company A allows Company B to read files from a shared S3 bucket.

Remember:

Cross-Account Access is managed using Bucket Policy.

---

## 6. IAM Role for EC2

AWS Services should use IAM Roles instead of IAM Users.

For example, if an EC2 instance needs to access an S3 bucket, attach an IAM Role to the EC2 instance.

Never create IAM Users inside an EC2 instance.

Remember:

AWS Service → IAM Role

Examples:
- EC2
- Lambda
- ECS

---

## 7. Explicit Deny

AWS checks both IAM Policies and Bucket Policies before granting access.

If any policy contains an Explicit Deny, access is always denied.

Rule:

Deny overrides Allow.

---

## 8. Encryption

Encryption protects S3 objects by storing them in encrypted form.

Benefits:
- Protects sensitive data
- Prevents unauthorized access
- Improves security

Remember:

Encryption protects data stored in S3.

---

## Key Takeaways

- IAM Policy → Permissions for Users, Groups, and Roles.
- Bucket Policy → Permissions for the S3 Bucket.
- ACL → Legacy permission method (rarely used).
- Public Access → Configured using Bucket Policy.
- Cross-Account Access → Managed using Bucket Policy.
- IAM Role → Used by AWS Services like EC2 and Lambda.
- Explicit Deny always overrides Allow.
- Encryption protects S3 objects by storing them securely.
