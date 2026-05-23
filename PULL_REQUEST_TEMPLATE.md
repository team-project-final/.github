## 변경 요약

<!-- 무엇을, 왜 변경했는지 1-3문장. -->

## 관련 이슈

<!-- Closes #N · Refs #M -->

## 변경 분류

- [ ] feat (신기능)
- [ ] fix (버그)
- [ ] docs (문서·ADR)
- [ ] refactor (리팩토링)
- [ ] test
- [ ] chore (빌드·CI·잡일)

## 영향 받는 서비스

- [ ] Platform Service
- [ ] Learning Service
- [ ] Knowledge Service
- [ ] Engagement Service
- [ ] AI Service
- [ ] Frontend (Flutter)
- [ ] Infrastructure (gitops)
- [ ] Shared (Avro 스키마)

## 테스트 결과

```
./gradlew test
# 또는 pytest, flutter test 등
```

## 체크리스트

- [ ] 코드가 빌드되고 테스트가 통과한다
- [ ] 새 기능에는 테스트를 추가했다
- [ ] **이벤트 스키마 변경 시**: Avro BACKWARD 호환성 확인
- [ ] **이벤트 발행자 변경 시**: Outbox 처리 확인
- [ ] 문서를 갱신했다 (해당하는 경우)
- [ ] 설계 결정이 있다면 ADR로 기록했다 (해당하는 경우)

## 스크린샷 (UI 변경 시)
