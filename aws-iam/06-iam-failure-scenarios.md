# IAM Failure Scenarios and Preventive Controls

## Scenario 1: Accidental Data Deletion
Cause: Over-privileged developer access without permission boundaries.
Prevention: Permission boundaries and explicit deny guardrails.

## Scenario 2: Admin-Induced Outage
Cause: Unrestricted IAM changes without change controls.
Prevention: Change management, permission boundaries, and separation of duties.

## Scenario 3: IAM Sprawl and Audit Failure
Cause: Direct user policies, unclear ownership, and lack of RBAC.
Prevention: Group-based access, ownership models, and periodic access reviews.

## Key Takeaway
Effective IAM design assumes human error and enforces guardrails
to limit blast radius, simplify audits, and maintain security posture.
