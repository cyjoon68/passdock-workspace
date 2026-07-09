# PassDock

PassDock은 인증 시도 이벤트를 수집하고 위험 규칙을 평가해 운영자가 알림을 확인·해결하는 인증 이벤트 운영 콘솔입니다.

```text
passdock-workspace/
  passdock-fe/
  passdock-be/
```

## 서비스 구성

- `passdock-fe`: 사용자 로그인 시도 화면과 운영 대시보드
- `passdock-be`: 로그인 이벤트 수집, 위험 평가, 알림 API

## 실행

```bash
git submodule update --init --recursive
docker compose up --build
```

## 핵심 흐름

- 사용자 로그인 시도에서 이벤트 수집
- 활성화된 위험 규칙 평가
- 위험 알림 생성
- 알림 상태와 처리 메모 관리
- Spring Actuator Prometheus 지표 제공

## 범위

- 실제 WebAuthn/Passkey 등록·서명 검증 구현이 아닙니다.
- Passkey 이름은 인증 이벤트 도메인을 설명하기 위한 것이며, 화면은 이벤트 수집과 운영 대응 흐름에 집중합니다.

## 운영 구조

- 위험 규칙은 rule-name evaluator map으로 평가합니다.
- Prometheus와 Grafana를 로컬 관측 구성에 포함합니다.
- Docker Compose로 서비스 스택을 실행합니다.
