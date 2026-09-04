## 1단계 · Supply Chain Security 켜기

의존성부터 봅니다. 이 저장소의 `package.json` 에는 오래된 버전이 두 개 들어 있습니다.

### 할 일

`.github/dependabot.yml` 파일을 만들고 아래 내용을 넣으세요.

```yaml
version: 2
updates:
  - package-ecosystem: "npm"
    directory: "/"
    schedule:
      interval: "weekly"
```

그리고 저장소 **Settings → Advanced Security** 에서 Dependabot alerts 를 켜세요.

### 왜 이렇게 하나

`package-ecosystem` 은 어떤 패키지 매니저를 볼지 정합니다.
`directory` 는 매니페스트 파일이 있는 위치이고, 루트면 `/` 입니다.
Dependabot 은 이 파일이 있어야 업데이트 PR 을 만듭니다.
반면 **알림**은 이 파일 없이도 의존성 그래프만 켜져 있으면 나옵니다. 둘을 구분하세요.

파일을 커밋하면 자동으로 채점됩니다.
