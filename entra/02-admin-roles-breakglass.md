# Entra Lab 02 — Admin Roles + Break-glass Design

## Objective
Document an admin security model for a small organization using Microsoft Entra ID.

## Principles
- Least privilege: assign the minimum admin role needed.
- Separate daily user identity from admin identity.
- Enforce MFA for administrative access.
- Maintain emergency access ("break-glass") accounts with monitoring.

## Admin roles (what they are used for)
- Global Administrator: full control; use sparingly.
- Privileged Role Administrator: manage role assignments (preferred for admin operations).
- User Administrator: manage users/groups without full tenant control.
- Security Administrator: manage security policies/alerts (limited scope).
- Application Administrator: manage app registrations/enterprise apps.

## Break-glass design (recommended)
### Purpose
Emergency access if admins are locked out (CA/MFA outage, misconfiguration).

### Controls
- 2 break-glass accounts minimum.
- Very strong passwords stored in a password manager.
- No day-to-day use; sign-in alerts enabled.
- Document the access and review quarterly.

## Operational model (example)
- Daily account: normal user permissions.
- Admin account: used only for admin work.
- Break-glass: emergency only.

## What I learned
- Over-permissioned admin accounts create the most risk.
- A break-glass plan is essential but must be monitored and reviewed.
