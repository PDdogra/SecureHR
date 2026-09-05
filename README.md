# SecureHR

Security-first, API-driven internal HR management platform, built as a reproducible cloud-security and blue-team engineering lab.

## Thesis

SecureHR is deliberately engineered so that realistic application and AWS telemetry is generated, ingested into Wazuh, detected, investigated, and handled through documented incident response.

**Build → Secure → Deploy → Generate telemetry → Attack safely → Detect → Investigate → Respond → Document → Destroy → Rebuild**

## Differentiator

The HR domain itself is not the point. The differentiator is the closed security-engineering loop:

**Threat → Attack → Application/AWS → Telemetry → Detection → Investigation → Response → Lessons → Improved controls**

The project is intentionally lean: roughly 70% application/cloud-security engineering and 30% SOC/detection/IR.

## Locked Principles (condensed)

- Security first, not an afterthought
- Realistic, not massive
- Modular monolith, not microservices
- API-first REST/JSON
- Server-side authorization only — never trust the frontend
- RBAC plus object/function-level authorization
- Identity lifecycle: ONBOARDING → ACTIVE → SUSPENDED → OFFBOARDED
- Wazuh is the primary SIEM/XDR
- Terraform is the source of truth for AWS infrastructure
- AWS resources are on-demand, destroyed when not needed
- No Kubernetes, no microservices, no full SOAR, no multi-region, no giant HR feature set

## Functional Scope

**In scope:**
- Employee: login, MFA, dashboard, profile, attendance, leave, documents
- Manager: team dashboard, leave approval/rejection
- HR: employee management, onboarding/offboarding, documents, leave admin
- Security: audit/security event visibility, incident info
- Admin: role management, controlled system configuration

**Out of scope (unless explicitly approved via scope review):**
- Payroll
- Recruitment
- Performance management
- Benefits
- Chat
- Mobile apps

## Architecture (high level)


## Status

🚧 In active development. See `docs/` for architecture, threat model, detections, and incident response documentation as they are produced phase by phase.

## Roadmap

- [ ] Phase 0 — Project setup & guardrails
- [ ] Phase 1 — SecureHR MVP
- [ ] Phase 2 — Security-first application engineering
- [ ] Phase 3 — AWS deployment
- [ ] Phase 4 — Terraform + reproducibility + CI/CD
- [ ] Phase 5 — Wazuh SOC
- [ ] Phase 6 — Incident response + portfolio