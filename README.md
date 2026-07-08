# PassDock

PassDock은 Passkey 로그인 이벤트를 수집하고 위험 규칙을 평가해 인증 위험 알림을 관리하는 모니터링 서비스입니다.

```text
passdock-workspace/
  passdock-fe/
  passdock-be/
```

## 서비스 구성

- `passdock-fe`: 로그인 실패, 위험 규칙, 알림 상태를 확인하는 운영 대시보드
- `passdock-be`: 로그인 이벤트 수집, 위험 평가, 알림 API

## 실행

```bash
git submodule update --init --recursive
docker compose up --build
```

## 핵심 흐름

- Passkey 로그인 이벤트 수집
- 활성화된 위험 규칙 평가
- 위험 알림 생성
- 알림 상태와 처리 메모 관리
- Spring Actuator Prometheus 지표 제공

## 운영 구조

- 위험 규칙은 rule-name evaluator map으로 평가합니다.
- Prometheus와 Grafana를 로컬 관측 구성에 포함합니다.
- Docker Compose로 서비스 스택을 실행합니다.
