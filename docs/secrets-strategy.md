# SecureHR - Secrets & Environment Variable Strategy

## Local development
- Real secrets live only in `.env` files, which are gitignored and never committed.
- `.env.example` files are committed and document required variable names with placeholder values.
- Each app component (backend, later frontend if needed) has its own `.env.example`.

## CI/CD (Phase 4)
- GitHub Actions secrets are stored in the repository's encrypted Secrets settings, never in code.
- Prefer short-lived/OIDC AWS authentication over long-lived access keys in GitHub Secrets.

## AWS (Phase 3+)
- Database credentials and application secrets are not hardcoded into Terraform files or committed .tfvars.
- Real `.tfvars` files are gitignored; `.tfvars.example` documents required variables.

## Rule
If a value would cause harm if leaked (password, API key, access key, secret token), it never appears in a committed file. No exceptions, no "just this once."