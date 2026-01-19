# AWS IAM – S3 Read-Only Access Policy

## Objective
Grant read-only access to a specific S3 bucket using least privilege.

## Actions Allowed
- s3:ListBucket (bucket-level)
- s3:GetObject (object-level)

## Design Notes
- Permissions applied via IAM group
- No write or delete access granted
- Bucket access restricted to a single bucket ARN

## Outcome
Read-only users can list and download objects without modifying data.
