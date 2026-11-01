# IAM Glossary + Core Concepts (2026)

This document is my quick-reference guide for Identity & Access Management (IAM) fundamentals.
It will be expanded throughout the month with examples from Okta, Entra ID, and AWS IAM.

---

## 1) Identity vs Account vs Credential
- **Identity:** A person or system represented digitally (employee, contractor, service).
- **Account:** A record in a system (e.g., Google account, Slack account, AWS IAM user).
- **Credential:** Proof used to authenticate an identity (password, OTP, FIDO key, certificate).

---

## 2) Authentication (AuthN) vs Authorization (AuthZ)
- **Authentication (AuthN):** Proving who you are (login).
- **Authorization (AuthZ):** What you’re allowed to access/do after login.

Example:
- Logging into Gmail = AuthN
- Being allowed to read HR emails or edit Drive files = AuthZ

---

## 3) MFA (Multi-Factor Authentication)
Using 2+ factors:
- Something you know (password)
- Something you have (OTP app, hardware key)
- Something you are (biometric)

Why it matters:
- Reduces risk from password leaks and phishing.

---

## 4) SSO (Single Sign-On)
One login to access multiple apps.

Common standards:
- **SAML** (often used for enterprise web SSO)
- **OIDC** (modern auth layer on OAuth2)

---

## 5) RBAC (Role-Based Access Control)
Access is assigned based on role/job function.
- Users → Groups/Roles → Permissions

Goal:
- Reduce manual access assignment
- Support least privilege
- Make auditing easier

---

## 6) Least Privilege
Give only the minimum access needed to do the job.
Benefits:
- Lower blast radius if account is compromised
- Reduces mistakes and insider risk

---

## 7) Identity Lifecycle (JML: Joiner–Mover–Leaver)
- **Joiner:** onboarding / new hire access provisioning
- **Mover:** role change → adjust access (add/remove)
- **Leaver:** offboarding → remove access quickly

Key risks:
- Orphan accounts (leaver not removed)
- Privilege creep (mover keeps old access)

---

## 8) Provisioning vs Deprovisioning
- **Provisioning:** creating accounts + granting access
- **Deprovisioning:** disabling/removing access + cleaning up

Good practice:
- Centralized control via IAM (Okta/Entra) or IGA(Identity Governance and Administration) tools
- Logging and approvals

---

## 9) Access Reviews / Certifications
Periodic checks to confirm access is still correct.
Common patterns:
- Quarterly manager review
- Application owner review
- High-risk access review (admins)

---

## 10) Typical IAM Tools (examples)
- **IdP (Identity Provider):** Okta, Microsoft Entra ID
- **Directory:** Active Directory, Entra ID
- **IGA:** SailPoint, Saviynt
- **PAM:** CyberArk, BeyondTrust

---

## 11) IAM in Operations (why this matters for IT Ops)
IAM is part of:
- Incident response (account compromise)
- Change management (SSO rollout, MFA enforcement)
- Compliance (ISO27001, SOC2, GDPR)
- Automation (provisioning, reporting)

---

## 12) My Next Hands-on Targets (this month)
- Okta: users, groups, app assignment
- Entra ID: users/groups + security designs
- AWS IAM: policies/roles + least privilege examples
- Automation: PowerShell/Python scripts for onboarding/offboarding