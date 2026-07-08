# PassDock

## Role Fit
- Frontend: TypeScript, Vue 3 Composition API, Nuxt, pnpm, ky, Cypress E2E
- Backend: Kotlin, Spring Boot MVC, PostgreSQL, Kafka dependency, Prometheus registry
- Infra: Docker Compose with Kafka, Prometheus, Grafana, GitHub Actions, GHCR
- Git Flow: develop default, main retained, policy workflow for branch and PR title rules

## Service
PassDock is a pass risk dashboard for monitoring credential/pass anomalies, revocation pressure, and operational risk signals.

## Problem Solving
- Modeled Kafka-ready backend dependencies and observability hooks for distributed event processing evidence.
- Added CI/CD across app/api repos and workspace compose validation for repeatable local operations.
- Migrated frontend to pnpm to keep dependency resolution stable across local and CI builds.

## Evidence
- App repo: https://github.com/passdock-labs/passdock-fe
- API repo: https://github.com/passdock-labs/passdock-be
- Workspace repo: https://github.com/cyjoon68/passdock-workspace
- CI/CD: frontend/backend CI, Docker build/push, workspace ops verification
