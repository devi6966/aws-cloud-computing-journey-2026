# Amazon S3 Replication

## 📌 What is Amazon S3 Replication?

Amazon S3 Replication is a feature that automatically copies objects from one S3 bucket (source bucket) to another S3 bucket (destination bucket). It is mainly used for backup, disaster recovery, compliance, and reducing access latency across different AWS Regions.

---

## 🔹 Types of S3 Replication

### 1. Same-Region Replication (SRR)
- Replicates objects between buckets in the **same AWS Region**.
- Used for:
  - Log aggregation
  - Development & testing
  - Data redundancy within the same region

### 2. Cross-Region Replication (CRR)
- Replicates objects between buckets in **different AWS Regions**.
- Used for:
  - Disaster recovery
  - Compliance requirements
  - Low-latency access for global users

---

## 🔹 Prerequisites

Before configuring S3 Replication:

- Versioning must be **enabled** on both the source and destination buckets.
- Source and destination buckets must be different.
- An IAM Role with replication permissions is required.
- Replication Rule must be configured.

---

## 🔹 How S3 Replication Works

1. Create a source bucket.
2. Create a destination bucket.
3. Enable Versioning on both buckets.
4. Create a Replication Rule.
5. AWS creates/uses an IAM Role for replication.
6. Upload an object to the source bucket.
7. The object is automatically replicated to the destination bucket.

---

## 🔹 Advantages

- Automatic data replication
- Disaster recovery
- High availability
- Compliance support
- Backup across regions
- Reduced latency for global users

---

## 🔹 Limitations

- Existing objects are **not replicated** by default (unless Batch Replication is used).
- Versioning is mandatory.
- Replication may take a short time depending on object size.
- Additional storage and data transfer charges may apply.

---

#  Key Points (Revision)

- S3 Replication automatically copies objects between S3 buckets.
- Two types:
  - **SRR** → Same Region Replication
  - **CRR** → Cross Region Replication
- Versioning must be enabled on **both buckets**.
- Requires an IAM Role and Replication Rule.
- Only **newly uploaded objects** are replicated by default.
- Existing objects require **S3 Batch Replication**.
- Used for **Backup, Disaster Recovery, Compliance, and High Availability**.
