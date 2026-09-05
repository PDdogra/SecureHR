# SecureHR - Tech Stack (Locked)

Decided in Phase 0, Task 0.3. Do not change without an explicit scope review.

## Backend
- Python 3.11.x
- FastAPI 0.115.x
- Uvicorn 0.30.x (ASGI server)
- SQLAlchemy 2.0.x (ORM)
- Alembic 1.13.x (migrations)
- Pydantic 2.x (validation, ships with FastAPI)

## Database
- PostgreSQL 17.x

## Frontend
- Node.js 22.x LTS
- React 18.x
- Vite 5.x

## Rationale
- FastAPI chosen over Django REST Framework (too heavy/opinionated) and Flask (too much manual boilerplate for validation/async).
- SQLAlchemy chosen for parameterized-query-by-default safety and maturity.
- React + Vite chosen over server-rendered templates to preserve a realistic SPA + REST API attack surface for later OWASP API Security work.
- Python 3.11.x used instead of 3.12.x (already installed; fully supported by FastAPI, SQLAlchemy 2.0.x, Alembic, Pydantic 2.x - no 3.12-specific features required).
- PostgreSQL 17.x used instead of 16.x (already installed; fully compatible with SQLAlchemy 2.0.x / Alembic).
- Node.js 22.x LTS used instead of 20.x (already installed, current LTS-track version; no compatibility concerns for React 18/Vite 5).
