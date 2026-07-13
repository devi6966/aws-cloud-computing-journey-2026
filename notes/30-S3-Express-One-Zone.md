# Amazon S3 Express One Zone

Amazon S3 Express One Zone is a high-performance, single-Availability Zone storage class designed for frequently accessed data and performance-critical applications.

It is built for workloads that require extremely low latency and very high request performance.

Unlike traditional S3 storage classes, S3 Express One Zone uses a special bucket type called a **Directory Bucket**.

---

# Key Features

- High-performance Amazon S3 storage class
- Designed for frequently accessed data
- Provides consistent single-digit millisecond latency
- Can provide data access speeds up to 10 times faster than S3 Standard
- Stores data within a single Availability Zone
- Uses S3 Directory Buckets
- Allows storage and compute resources to be placed in the same Availability Zone
- Designed for latency-sensitive applications
- Supports request-intensive workloads
- Provides lower request costs than S3 Standard for suitable workloads
- Designed for 99.95% availability within a single Availability Zone

---

# What Is a Directory Bucket?

A Directory Bucket is a special Amazon S3 bucket type designed for low-latency and high-performance workloads.

S3 Express One Zone stores objects in Directory Buckets instead of traditional general-purpose buckets.

When creating a Directory Bucket:

- A specific AWS Region must be selected
- A specific Availability Zone must be selected
- The selected Availability Zone cannot be changed after bucket creation
- Data is stored across multiple devices within the selected Availability Zone
- Data is not automatically replicated across multiple Availability Zones

---

# General-Purpose Bucket vs Directory Bucket

| Feature | General-Purpose Bucket | Directory Bucket |
|---|---|---|
| Used by | Traditional S3 storage classes | S3 Express One Zone |
| Main purpose | General object storage | High-performance object storage |
| Availability Zone architecture | Usually multi-AZ | Single AZ |
| Performance | High | Extremely high |
| Latency | Millisecond access | Consistent single-digit millisecond access |
| Best for | Websites, applications and backups | ML, analytics, HPC and latency-sensitive workloads |

---

# How S3 Express One Zone Works

```text
High-performance application
              ↓
Compute resource such as EC2
              ↓
Same Availability Zone
              ↓
S3 Directory Bucket
              ↓
S3 Express One Zone
              ↓
Consistent single-digit millisecond access
