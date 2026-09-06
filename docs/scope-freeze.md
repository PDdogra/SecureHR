# SecureHR - Scope Freeze

**Status:** FROZEN as of Phase 0 completion.
**Authority:** SecureHR AI Development Master Plan + SecureHR AI Execution Prompt (source of truth documents).

## Phase 0 Done Criteria (Gate)

- [x] Repository exists with main/dev branch strategy
- [x] README documents project thesis and scope
- [x] Tech stack versions locked and documented
- [x] Local development environment verified (Python, Node, PostgreSQL all confirmed working)
- [x] .gitignore, environment-variable strategy, and secret-handling rules in place
- [x] Issue/checklist tracking structure created on GitHub
- [x] Scope freeze documented (this file)

**Gate status: PASS**

## Frozen Functional Scope

**In scope** (see README.md for full detail):
- Employee, Manager, HR, Security, Admin roles with defined functional boundaries
- Authentication, MFA, RBAC, object/function-level authorization
- Attendance, leave, documents, employee lifecycle management
- AWS deployment (VPC/EC2/RDS/ALB/CloudFront/WAF), Terraform-managed
- Wazuh SOC integration, five flagship detections, five incident response reports

**Explicitly out of scope** (require an explicit scope review to add):
- Payroll
- Recruitment
- Performance management
- Benefits administration
- Chat/messaging
- Mobile applications
- Kubernetes, microservices, service mesh
- Multiple SIEMs (ELK, OpenSearch, Security Onion, Splunk)
- Full SOAR platform
- Multi-region architecture

## Change Process

Any request to add an out-of-scope item, or expand an in-scope item significantly, must be classified per the Execution Prompt's Rule 25:
 CORE : required for the locked scope, proceed
 OPTIONAL : allowed only after the relevant phase gate has passed
 OUT OF SCOPE : not implemented without an explicit, deliberate scope-review decision recorded here

## Project Balance Target

Maintain approximately 70% application/cloud-security engineering, 30% SOC/detection/IR, per Master Plan Section 3.