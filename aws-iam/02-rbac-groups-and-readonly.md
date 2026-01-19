# AWS IAM RBAC – Admin and Read-Only Roles

## Objective
Implement role-based access control using IAM groups.

## Groups Created
- LabAdmins → AdministratorAccess
- ReadOnlyUsers → ReadOnlyAccess

## Design Decisions
- Permissions assigned to groups, not users
- No overlapping admin and read-only access
- Supports least privilege and audits

## Outcome
Clear separation of duties with reduced blast radius.
