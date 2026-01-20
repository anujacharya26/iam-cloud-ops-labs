# AWS IAM Guardrails Overview

## What is a Guardrail
A guardrail is a security control that enforces non-negotiable limits
on permissions, even if broader access is granted later.

## Guardrail Types
- Explicit Deny: blocks specific actions
- Permission Boundary: limits maximum permissions for users or roles
- SCP: enforces organization-wide limits across accounts

## Why Enterprises Use Guardrails
Guardrails prevent privilege escalation, admin mistakes,
and future misconfigurations while simplifying audits
and enforcing security boundaries.

## Practical Example
Developers may have broad permissions, but permission boundaries
ensure they cannot exceed predefined limits, even if additional
policies are attached later.
