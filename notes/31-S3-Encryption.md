# Amazon S3 Encryption

Amazon S3 Encryption is used to protect data stored in an S3 bucket by converting it into an encrypted and unreadable format.

There are two main types of encryption:

1. Server-Side Encryption (SSE)
2. Client-Side Encryption (CSE)

---

## 1. Server-Side Encryption (SSE)

In Server-Side Encryption, the file is uploaded to Amazon S3 first, and Amazon S3 encrypts the file before storing it.

```text
Original File
      ↓
Uploaded to Amazon S3
      ↓
Encrypted by Amazon S3
      ↓
Stored in encrypted form
```

### Key Points

- Encryption is performed by Amazon S3.
- The client uploads the file normally.
- Amazon S3 handles the encryption process.
- It is easier to use and manage.

---

## 2. Client-Side Encryption (CSE)

In Client-Side Encryption, the file is encrypted by the client before it is uploaded to Amazon S3.

The client can be a user's device or application.

```text
Original File
      ↓
Encrypted on the client side
      ↓
Uploaded to Amazon S3
      ↓
Stored in encrypted form
```

### Key Points

- Encryption is performed before uploading the file.
- Amazon S3 receives an already encrypted file.
- The client handles encryption and decryption.
- The client is responsible for managing the encryption key.

---

## SSE vs CSE

| Feature | Server-Side Encryption | Client-Side Encryption |
|---|---|---|
| Encryption is performed by | Amazon S3 | Client/User |
| Encryption occurs | After the file reaches S3 | Before uploading to S3 |
| Key management | Handled according to the selected AWS encryption option | Managed by the client |
| Management | Easier | Requires more client-side management |

---

## Quick Revision

```text
SSE
Upload → S3 encrypts → Encrypted data stored
```

```text
CSE
Client encrypts → Upload → Encrypted data stored in S3
```

> **Main Difference:** In SSE, Amazon S3 encrypts the data. In CSE, the client encrypts the data before uploading it.
