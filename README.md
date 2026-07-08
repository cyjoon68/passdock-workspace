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
- Frontend: Next.js App Router, React Compiler, TypeScript, ky.
- Backend: Kotlin, Spring Boot MVC, PostgreSQL schema, Kafka dependency, Prometheus endpoint.
- CI: FE lint/build, BE Gradle test.
