# Permission Boundary – Admin Access Capped

## Objective
Demonstrate how permission boundaries limit maximum permissions
even when AdministratorAccess is granted.

## Boundary Behavior
The permission boundary allows all actions except `s3:DeleteObject`.
Actions outside the boundary are implicitly denied.

## Result
The test user retained admin capabilities but was unable to delete
S3 objects, proving that permission boundaries cap privilege escalation.
