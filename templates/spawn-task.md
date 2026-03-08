# sessions_spawn Task Template

아래 블록을 그대로 복붙해서 사용.

```txt
[대상]
- 수정/조회 대상: (파일, 경로, 시스템)

[목표]
- 완료 기준(DoD):
  1) ...
  2) ...

[제약]
- 반드시 지킬 규칙:
  - ...
- 금지:
  - ...

[참고]
- 먼저 읽기:
  - ...

[검증]
- 검증 명령/기준:
  - ...

[산출물]
- 반드시 아래 형식으로 보고:
  1) 변경 요약 3줄
  2) 수정 파일 목록
  3) 검증 결과
  4) 리스크/후속 TODO
```

---

## 예시 (코드 수정)

```js
sessions_spawn({
  label: "studycard-button-rule",
  runTimeoutSeconds: 600,
  task: `
[대상]
- apps/web/components/StudyCard.tsx

[목표]
- 모집 마감 전 단톡방/캘린더 버튼 비활성화
- 마감 다음날 00:00 KST부터 활성화

[제약]
- UI 텍스트는 '모집 마감 후 이용 가능'
- 기존 스타일 토큰 체계 유지

[참고]
- references/ui-rules.md
- references/date-policy.md

[검증]
- npm run build 통과
- 관련 테스트 통과

[산출물]
1) 변경 요약 3줄
2) 수정 파일 목록
3) 빌드/테스트 결과
4) 리스크/후속 TODO
`
})
```
