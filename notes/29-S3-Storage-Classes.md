# Amazon S3 Storage Classes

Amazon S3 provides different storage classes designed for different data access patterns, storage costs, availability requirements, and retrieval needs.

The correct storage class depends mainly on:

- How frequently the data is accessed
- How quickly the data is required
- How long the data will be stored
- Storage and retrieval cost requirements

---

## 1. Amazon S3 Standard

Amazon S3 Standard is the default general-purpose storage class. It is designed for frequently accessed data that requires high availability and immediate access.

### Key Features

- Designed for frequently accessed data
- Provides low-latency and high-throughput performance
- Objects can be accessed immediately in milliseconds
- Stores data across multiple Availability Zones
- No minimum storage duration
- No retrieval fee
- Designed for 99.99% availability
- Designed for 99.999999999% durability (11 nines)

### Common Use Cases

- Website content
- Mobile and web applications
- Frequently accessed images and videos
- Active project files
- Cloud applications
- Frequently downloaded documents

### Example

A website stores images that are viewed by users every day. Since these images are accessed frequently, S3 Standard is suitable.

---

## 2. Amazon S3 Standard-IA

**IA** stands for **Infrequent Access**.

Amazon S3 Standard-Infrequent Access is designed for data that is accessed less frequently but must be available immediately whenever required.

It provides lower storage costs than S3 Standard, but retrieval charges apply when the data is accessed.

### Key Features

- Designed for infrequently accessed data
- Immediate access with millisecond latency
- Lower storage cost than S3 Standard
- Retrieval charges apply
- Stores data across multiple Availability Zones
- Designed for 99.9% availability
- Designed for 99.999999999% durability
- Minimum storage duration: 30 days
- Minimum billable object size: 128 KB

### Common Use Cases

- Backup files
- Disaster recovery data
- Older project files
- Long-lived data accessed occasionally
- Previous semester documents

### Example

Old semester results are not accessed regularly, but students may need to download them immediately. Therefore, S3 Standard-IA is suitable.

> Note: An object can be deleted before 30 days, but minimum storage-duration charges may still apply.

---

# Amazon S3 Glacier Storage Classes

Amazon S3 Glacier storage classes are designed for long-term data archiving.

They provide lower storage costs than frequently accessed storage classes. Retrieval cost and retrieval time depend on the selected Glacier storage class.

Common use cases include:

- Long-term backups
- Historical records
- Legal documents
- Financial records
- Compliance data
- Old company records

Amazon S3 provides three main Glacier storage classes.

---

## 3. S3 Glacier Instant Retrieval

S3 Glacier Instant Retrieval is designed for archive data that is accessed very rarely but must be available immediately when required.

### Key Features

- Designed for rarely accessed archive data
- Millisecond retrieval
- Lower storage cost
- Retrieval charges apply
- Minimum storage duration: 90 days

### Common Use Cases

- Medical images
- Archived media
- Old but important documents
- Historical records requiring immediate access

### Example

A hospital stores old X-ray images that are rarely accessed but must be immediately available when a patient requires them.

---

## 4. S3 Glacier Flexible Retrieval

S3 Glacier Flexible Retrieval is designed for archive data that does not require immediate access.

Depending on the selected retrieval option, data retrieval may take from minutes to hours.

### Retrieval Options

- Expedited retrieval: Data may be available within minutes
- Standard retrieval: Data is generally available within hours
- Bulk retrieval: Lower-cost retrieval for large amounts of data

### Key Features

- Designed for long-term archive data
- Lower storage cost
- Retrieval time ranges from minutes to hours
- Retrieval charges apply
- Minimum storage duration: 90 days

### Common Use Cases

- Old backups
- Historical records
- Disaster recovery archives
- Old project archives

### Example

A company stores old backup files that are rarely accessed and do not need to be retrieved immediately.

---

## 5. S3 Glacier Deep Archive

S3 Glacier Deep Archive is designed for very long-term data retention and extremely rare access.

It is one of the lowest-cost Amazon S3 storage classes.

### Key Features

- Designed for data accessed once or twice per year
- Very low storage cost
- Retrieval generally takes several hours
- Retrieval charges apply
- Minimum storage duration: 180 days

### Common Use Cases

- Legal records
- Government records
- Long-term financial records
- Regulatory and compliance data
- Data stored for many years

### Example

A company must retain employee and financial records for 10 years due to legal requirements. Since the data is rarely accessed, S3 Glacier Deep Archive is suitable.

---

# Comparison of S3 Storage Classes

| Feature | S3 Standard | S3 Standard-IA | Glacier Instant Retrieval | Glacier Flexible Retrieval | Glacier Deep Archive |
|---|---|---|---|---|---|
| Access frequency | Frequent | Infrequent | Rare | Very rare | Extremely rare |
| Retrieval speed | Milliseconds | Milliseconds | Milliseconds | Minutes to hours | Several hours |
| Storage cost | Higher | Lower | Very low | Lower | Lowest |
| Retrieval charges | No | Yes | Yes | Yes | Yes |
| Minimum storage duration | None | 30 days | 90 days | 90 days | 180 days |
| Best for | Active data | Backups and DR | Rare archive with instant access | Long-term archives | Very long-term archives |

---

# Storage Class Selection

Use the following approach when selecting an S3 storage class:

```text
Frequently accessed active data
            ↓
       S3 Standard

Infrequently accessed data
but immediate access is required
            ↓
      S3 Standard-IA

Rarely accessed archive data
but immediate access is required
            ↓
S3 Glacier Instant Retrieval

Archive data that can wait
minutes or hours for retrieval
            ↓
S3 Glacier Flexible Retrieval

Long-term archive data that is
almost never accessed
            ↓
S3 Glacier Deep Archive
