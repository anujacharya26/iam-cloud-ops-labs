# AWS IAM Root & Admin Baseline

## Objective
Establish a secure AWS account baseline.

## Actions Performed
- Enabled MFA on root user
- Created non-root IAM admin user (lab-admin)
- Avoided daily use of root credentials

## Security Rationale
- Root user used as break-glass only
- MFA reduces credential compromise risk
- Admin access delegated via IAM groups
