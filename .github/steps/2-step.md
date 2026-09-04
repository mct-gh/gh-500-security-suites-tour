## 2단계 · Code Security 켜기

이번엔 코드 자체를 봅니다. `app/app.js` 에는 `innerHTML` 로 값을 넣는 부분이 있습니다.

### 할 일

`.github/workflows/codeql.yml` 을 만들고 아래 내용을 넣으세요.

```yaml
name: CodeQL

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]
  schedule:
    - cron: "0 3 * * 1"

jobs:
  analyze:
    runs-on: ubuntu-latest
    permissions:
      security-events: write
      contents: read
    steps:
      - uses: actions/checkout@v5
      - uses: github/codeql-action/init@v3
        with:
          languages: javascript-typescript
      - uses: github/codeql-action/analyze@v3
```

### 왜 이렇게 하나

`security-events: write` 가 없으면 결과를 업로드하지 못합니다. 가장 흔한 실패 원인입니다.
`schedule` 을 같이 거는 이유는, 코드가 바뀌지 않아도 **쿼리 팩이 갱신**되면 새 취약점이 잡히기 때문입니다.
이벤트 기반 스캔만 걸면 조용한 저장소는 영원히 옛 기준으로 남습니다.

커밋한 뒤 **Actions** 탭에서 실행을 확인하고, **Security → Code scanning** 에서 알림을 보세요.
