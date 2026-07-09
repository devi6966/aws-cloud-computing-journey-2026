# AWS S3 Static Website Hosting

## Objective
Host a static website using an Amazon S3 bucket.

---

## What is Static Website Hosting?

Amazon S3 can host static websites containing:

- HTML
- CSS
- JavaScript
- Images

It cannot run backend code like PHP, Java, Python, or Node.js.

---

## Steps Performed

### 1. Create an S3 Bucket

- Bucket name must be globally unique.
- Select AWS Region.

---

### 2. Upload Website Files

Uploaded:

- index.html
- coffee.jpg

---

### 3. Enable Static Website Hosting

Properties
→ Static Website Hosting
→ Enable

Index document:

```
index.html
```

---

### 4. Disable Block Public Access

Permissions
→ Block Public Access
→ Edit

Disable:

✔ Block all public access

Save changes.

---

### 5. Apply Bucket Policy

```json
{
  "Version":"2012-10-17",
  "Statement":[
    {
      "Effect":"Allow",
      "Principal":"*",
      "Action":"s3:GetObject",
      "Resource":"arn:aws:s3:::BUCKET_NAME/*"
    }
  ]
}
```

Replace:

```
BUCKET_NAME
```

with your bucket name.

---

### 6. Open Website Endpoint

Properties
→ Static Website Hosting

Open:

Bucket Website Endpoint

Website loads successfully.

---

## Outcome

Successfully hosted a static website on Amazon S3.

---

## Important Points

- S3 hosts only static websites.
- Public access must be enabled.
- Bucket Policy grants read access.
- Index document is mandatory.
- Images must also be publicly accessible.
- Bucket names are globally unique.

---

## Services Used

- Amazon S3
- Bucket Policy
- Static Website Hosting

---

## Result

Website successfully displayed:

- Heading
- Text
- Coffee Image
