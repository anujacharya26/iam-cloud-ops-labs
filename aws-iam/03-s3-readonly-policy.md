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

## IAM Policy Snippet

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowListBucket",
      "Effect": "Allow",
      "Action": "s3:ListBucket",
      "Resource": "arn:aws:s3:::iam-lab-s3-readonly-aa-1234"
    },
    {
      "Sid": "AllowReadObjects",
      "Effect": "Allow",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::iam-lab-s3-readonly-aa-1234/*"
    }
  ]
}

## Explicit Deny Guardrail

An explicit deny was added to block `s3:DeleteObject` at the object level.
This deny overrides any allow policies and prevents accidental or malicious
deletion of data, even if broader permissions are granted later.

## Explicit Deny Policy Snippet

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "ExplicitDenyDeleteObject",
      "Effect": "Deny",
      "Action": "s3:DeleteObject",
      "Resource": "arn:aws:s3:::iam-lab-s3-readonly-aa-1234/*"
    }
  ]
}