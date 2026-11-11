---
name: security-audit
description: Conduct authorized, risk-based application security reviews with safe testing boundaries and actionable evidence.
---

# Security Audit

## Authorization and safety
- Confirm target repository, environment and written scope.
- Default to read-only static review.
- Do not test production, access real user data, exploit third parties or perform destructive actions without explicit authorization.
- Do not expose full secrets in output.

## Review areas
- Authentication, authorization, session lifecycle and privilege boundaries.
- IDOR/BOLA and tenant isolation.
- Input validation, injection, serialization and file handling.
- Sensitive data at rest, in transit, logs and analytics.
- Secret/configuration exposure and build artifacts.
- Dependency and supply-chain risks.
- Rate limiting, abuse controls and error information leakage.
- Mobile reverse engineering and client-side trust assumptions.

## Finding quality
For every finding include affected asset, preconditions, evidence, safe reproduction, impact, severity, confidence and remediation.
Distinguish exploitable vulnerabilities from theoretical concerns. Public client identifiers are not automatically secrets; assess their privileges and abuse potential.
Conclude with PASS, PASS WITH CONDITIONS, FAIL or BLOCKED and list coverage limitations.
