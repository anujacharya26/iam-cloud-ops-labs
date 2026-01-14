# Entra Lab 01 — Users & Groups (RBAC Foundation)

## Objective
Build a basic RBAC model in Microsoft Entra ID using users + security groups.

## Users created
- joiner1
- mover1
- leaver1
- contractor1

## Groups created
- CF-IT
- CF-HR
- CF-Finance

## Group membership mapping
- joiner1 → CF-IT
- contractor1 → CF-IT
- mover1 → CF-HR
- leaver1 → CF-Finance

## Steps performed (high level)
1) Created 4 test users in Microsoft Entra ID.
2) Created 3 security groups (Assigned membership).
3) Added users to groups to model RBAC.

## What I learned
- Group-based access is the foundation of RBAC.
- Joiner/Mover/Leaver (JML) lifecycle becomes manageable when access is group-driven, not user-by-user.
