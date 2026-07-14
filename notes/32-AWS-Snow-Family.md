# AWS Snow Family

AWS Snow Family is a collection of physical devices used to securely transfer large amounts of data between on-premises locations and AWS.

It is useful when transferring data through the internet would be slow, expensive, or difficult because of limited network bandwidth.

---

## How AWS Snow Family Works

```text
AWS sends a Snow device
          ↓
Customer transfers data to the device
          ↓
Device is returned to AWS
          ↓
AWS uploads the data to the cloud
```

---

## AWS Snowcone

AWS Snowcone is the smallest and most portable device in the AWS Snow Family.

### Key Points

- Small, lightweight, and portable
- Used for edge computing and data transfer
- Suitable for locations with limited space or network connectivity
- Can transfer data physically or through AWS DataSync

---

## AWS Snowball Edge

AWS Snowball Edge is a physical device used to transfer large amounts of data between on-premises environments and AWS.

### Key Points

- Used for large-scale offline data transfer
- Supports data migration and edge computing
- Useful when internet bandwidth is limited
- Can import data into Amazon S3
- Can export data from Amazon S3

### Example

A company needs to transfer hundreds of terabytes of data to AWS, but its internet connection is slow.

The company can use AWS Snowball Edge instead of transferring all the data through the internet.

```text
On-Premises Data
        ↓
AWS Snowball Edge
        ↓
Device returned to AWS
        ↓
Data uploaded to AWS
```

---

## AWS Snowmobile

AWS Snowmobile is used to transfer extremely large amounts of data to AWS.

It is a secure data-transfer service transported using a large shipping container.

### Key Points

- Designed for extremely large-scale data migration
- Can transfer exabytes of data
- Suitable for data centers and very large organizations
- Used when Snowball devices are not sufficient

---

## Comparison

| Service | Best Used For |
|---|---|
| AWS Snowcone | Small and portable data-transfer or edge workloads |
| AWS Snowball Edge | Large-scale offline data transfer and edge computing |
| AWS Snowmobile | Extremely large, exabyte-scale data migration |

---

## Current AWS Snowball Edge Update

AWS Snowball Edge is no longer available to new customers.

Existing customers can continue using the service.

The AWS Snow Family and Snowball Edge may still be studied to understand offline data migration and AWS Cloud migration concepts.

---

## Quick Revision

```text
Snowcone
= Smallest and portable device
```

```text
Snowball Edge
= Large-scale offline data transfer
= Edge computing
```

```text
Snowmobile
= Extremely large data transfer
= Exabyte-scale migration
```

> **Main Purpose:** AWS Snow Family helps transfer large amounts of data when internet-based transfer is slow, expensive, or impractical.
