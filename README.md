# PassDock

PassDock is a Passkey authentication risk monitoring service for collecting login events, evaluating risk rules, and tracking alert handling.

```text
passdock-workspace/
  passdock-fe/
  passdock-be/
```

## Services

- `passdock-fe`: operations dashboard for login failures, risk rules, and alerts.
- `passdock-be`: login event ingestion, risk evaluation, and alert API.

## Run

```bash
git submodule update --init --recursive
docker compose up --build
```

## Core Flow

- Ingest Passkey login events.
- Evaluate enabled risk rules.
- Create risk alerts.
- Track alert status and incident notes.
- Export metrics through Spring Actuator Prometheus.

## Operations

- Risk rules use a rule-name evaluator map.
- Prometheus and Grafana are included in local observability.
- Docker Compose starts the local service stack.
