# Amazon S3 object

## What is an Object?

Object means the actual file stored inside an S3 bucket.

Examples:
- image.jpg
- video.mp4
- resume.pdf
- notes.txt

An S3 Object contains:
- Key
- Value (File)
- Metadata
- Tags
- Version ID (if versioning is enabled)

---

## Key

Key is the unique path of an object inside a bucket.

Example:

s3://my-bucket/images/photo.jpg

Key:

images/photo.jpg

---

## Value

Value is the actual content of the file.

Example:
- Image
- PDF
- Video
- ZIP

---

## Metadata

Metadata is information about the object.

Examples:
- File Size
- Content Type
- Last Modified

---

## Tags

Tags are key-value pairs used to organize objects.

Example:

Environment = Dev
Project = AWS

Used for:
- Billing
- Lifecycle Rules
- Automation

---

## Version ID

Version ID is created when Bucket Versioning is enabled.

It helps restore old versions if a file is updated or deleted.

---

## Folder in S3

S3 does not have real folders.

Folders are created using prefixes.

Example:

images/photo.jpg

Prefix:

images/

---

## Example

s3://my-bucket/my_folder/file.txt

Bucket:
my-bucket

Prefix:
my_folder/

Object:
file.txt

Key:
my_folder/file.txt

---

## Limits

- Maximum Object Size = 5 TB
- Files larger than 5 GB should use Multipart Upload

---

## Remember

- Bucket stores Objects.
- Object = File.
- Key = Object path.
- Metadata = File information.
- Tags = Labels.
- Version ID = Different versions of the same object.
