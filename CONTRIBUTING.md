# Synapse 기여 가이드

이 가이드는 `team-project-final` 조직의 모든 레포에 적용됩니다.

## 브랜치 전략

- `master` — 항상 배포 가능한 상태
- `feat/<short-name>` — 신규 기능
- `fix/<short-name>` — 버그 수정
- `docs/<short-name>` — 문서·ADR
- `chore/<short-name>` — 빌드·CI·잡일

## 커밋 컨벤션 (Conventional Commits)

```
<type>(<scope>): <subject>
```

**type**: `feat` · `fix` · `docs` · `chore` · `refactor` · `test` · `style`
**scope** 예시: `platform` · `learning` · `knowledge` · `engagement` · `ai` · `gitops` · `shared` · `frontend` · `profile`

예시:
- `feat(learning): add SRS scheduler`
- `fix(platform): handle duplicate PaymentCompleted event`
- `docs(decisions): ADR-0002 Why Kafka + Avro`

## PR 규칙

1. 1 PR = 1 목적. 5개 파일 넘으면 분할 검토.
2. PR 본문은 자동 채워지는 템플릿(`PULL_REQUEST_TEMPLATE.md`)을 따른다.
3. 모든 PR은 머지 전 최소 1인 리뷰 통과.
4. 테스트가 깨진 PR은 머지 금지.
5. **Avro 이벤트 스키마 변경**은 별도 리뷰 필수 (BACKWARD 호환성 검증).

## 이슈 작성

- 버그: `bug_report.yml` 폼 사용
- 신기능 제안: `feature_request.yml` 폼 사용
- 빈 이슈는 비활성화.

## 로컬 개발

각 서비스 레포에서 `./gradlew bootRun` (또는 AI Service의 경우 `uvicorn`). 통합 환경은 [synapse-gitops](https://github.com/team-project-final/synapse-gitops)의 로컬 docker-compose 참조.
