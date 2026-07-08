# passdock-workspace

Root workspace for PassDock. Child repos are managed as git submodules.

```text
passdock-workspace/
  passdock-fe/
  passdock-be/
```

## Run

```bash
git submodule update --init --recursive
docker compose up --build
```

## Resume evidence

- Passkey risk monitoring: login event ingest, risk rules, alert status.
- Risk evaluator bottleneck fix: if-chain replaced with a rule-name strategy map; see `docs/risk-evaluator-refactor.md`.
- Frontend: Next.js App Router, React Compiler, TypeScript, ky.
- Backend: Kotlin, Spring Boot MVC, PostgreSQL schema, Kafka dependency, Prometheus endpoint.
- Observability: Prometheus scrape config and Grafana service.
- CI: FE lint/build, BE Gradle test.
