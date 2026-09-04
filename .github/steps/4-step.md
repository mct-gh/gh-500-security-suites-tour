## 4단계 · 알림을 제품군으로 구분하기

세 개를 다 켰습니다. 이제 **알림만 보고 출처를 말할 수 있어야** 합니다.

### 할 일

`docs/security-suites.md` 파일을 만들고, 아래 세 제품군 이름을 각각 한 번 이상 쓰면서
이 저장소에서 실제로 본 알림을 하나씩 적으세요.

- `Code Security`
- `Secret Protection`
- `Supply Chain Security`

각 항목에 이렇게 적으면 됩니다.

```markdown
## Code Security
- 어디서 봤나: Security 탭 → Code scanning
- 무엇을 잡았나: app/app.js 의 innerHTML 사용
- 누가 고치나: 코드 작성자
```

### 왜 이렇게 하나

시험은 기능 이름을 2026년 7월에 전부 바꿨습니다.
Learn 본문과 강사 슬라이드는 아직 옛 이름(secret scanning, Dependabot, code scanning)을 씁니다.
새 이름으로 스스로 정리해 두지 않으면 시험에서 같은 것을 다른 이름으로 보고 헷갈립니다.
