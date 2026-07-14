# Amazon S3 Shared Responsibility Model

The AWS Shared Responsibility Model divides security responsibilities between **AWS** and the **customer (user)**.

For Amazon S3:

- AWS is responsible for **security of the cloud**.
- The customer is responsible for **security in the cloud**.

---

## AWS Responsibility – Security of the Cloud

AWS is responsible for protecting and managing the infrastructure on which Amazon S3 runs.

### AWS is responsible for:

- Physical security of AWS data centers
- Physical servers and storage hardware
- Networking infrastructure
- Availability Zone infrastructure
- Maintaining the Amazon S3 service
- Hardware maintenance and replacement
- Protecting the underlying AWS cloud infrastructure

```text
AWS Responsibility
        ↓
Security OF the Cloud
        ↓
Data centers, hardware,
networking and S3 infrastructure
```

---

## Customer Responsibility – Security in the Cloud

The customer is responsible for securely managing the data, permissions, and configurations used in Amazon S3.

### The customer is responsible for:

- Managing S3 bucket permissions
- Configuring bucket policies
- Managing IAM users, roles, and permissions
- Controlling public access to buckets and objects
- Selecting appropriate encryption settings
- Managing customer-controlled encryption keys
- Enabling versioning when required
- Configuring replication and backup based on requirements
- Managing object lifecycle rules
- Classifying and protecting uploaded data
- Preventing accidental public access

```text
Customer Responsibility
          ↓
Security IN the Cloud
          ↓
Data, permissions, encryption,
bucket policies and configurations
```

---

## Example

A user accidentally makes an S3 bucket public and sensitive data becomes accessible.

AWS is responsible for keeping the Amazon S3 infrastructure secure.

However, the customer is responsible for correctly configuring bucket permissions and preventing unauthorized public access.

---

## AWS vs Customer

| AWS Responsibility | Customer Responsibility |
|---|---|
| Physical data centers | Data stored in S3 |
| Storage hardware | S3 bucket permissions |
| AWS networking infrastructure | IAM permissions |
| S3 service infrastructure | Bucket policies |
| Hardware maintenance | Public access settings |
| Availability Zone infrastructure | Encryption configuration |
| Security of the cloud | Security in the cloud |

---

## Quick Revision

```text
AWS
= Security OF the Cloud
= Data centers
= Hardware
= Networking
= S3 infrastructure
```

```text
Customer
= Security IN the Cloud
= Data
= IAM permissions
= Bucket policies
= Public access settings
= Encryption configuration
```

> **Main Difference:** AWS secures the infrastructure that runs Amazon S3, while the customer is responsible for securely managing their data, permissions, and S3 configurations.
