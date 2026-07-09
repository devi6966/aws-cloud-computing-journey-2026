# Amazon S3 Versioning

## What is S3 Versioning?

Amazon S3 Versioning is a feature that keeps multiple versions of the same object in a bucket. It helps protect data from accidental deletion or overwriting.

---

## Why Use Versioning?

- Recover accidentally deleted files.
- Restore previous versions of an object.
- Protect important data.
- Maintain object history.
- Improve backup and disaster recovery.

---

## How Versioning Works

When Versioning is enabled, every upload of the same object creates a new Version ID.

Example:

```
resume.pdf (Version 1)
        ↓
resume.pdf (Version 2)
        ↓
resume.pdf (Version 3)
```

All previous versions remain stored until they are deleted manually or by Lifecycle Rules.

---

## Versioning States

### 1. Unversioned (Default)

- Versioning is disabled.
- Uploading a file with the same name replaces the old file.

---

### 2. Enabled

- Every object gets a unique Version ID.
- Previous versions are preserved.
- Deleted objects receive a Delete Marker.

---

### 3. Suspended

- Existing versions remain available.
- New uploads receive a **null Version ID**.
- Previous versions can still be accessed.

---

## Delete Marker

When Versioning is enabled and an object is deleted, AWS does not immediately remove it.

Instead, it creates a **Delete Marker**, while the previous versions remain stored and can be restored.

---

## Advantages

- Prevents accidental data loss.
- Easy rollback to previous versions.
- Supports backup and recovery.
- Maintains version history.
- Improves data protection.

---

## Limitations

- Multiple versions consume additional storage.
- More storage means higher storage costs.

---

## Real-World Use Cases

- Backup important documents.
- Store multiple versions of project files.
- Recover accidentally deleted website assets.
- Maintain audit history.

---

## Key Takeaways

- S3 Versioning stores multiple versions of the same object.
- Every new upload creates a unique **Version ID**.
- Deleting an object creates a **Delete Marker** instead of permanently deleting it.
- Versioning cannot be disabled once enabled; it can only be **Suspended**.
- Previous versions remain available until deleted manually or by Lifecycle Rules.
- Versioning improves backup, recovery, and data protection.
