# 랩 A · 세 가지 보안 제품군 한 바퀴

_GH-500 모듈 1 · GitHub Security suites 구조와 역할 구분_

## 이 랩에서 하는 일

Contoso 보안 데모 앱 하나에 GitHub 의 세 가지 보안 제품군을 전부 켭니다.
켜보고 나면 "어떤 알림이 어느 제품군에서 나온 것인지"를 화면만 보고 구분할 수 있게 됩니다.

| 제품군 | 옛 이름 | 이 랩에서 켜는 것 |
| --- | --- | --- |
| Supply Chain Security | Dependabot, Dependency Review | `.github/dependabot.yml` |
| Code Security | Code Scanning with CodeQL | `.github/workflows/codeql.yml` |
| Secret Protection | Secret scanning | `.github/secret_scanning.yml` |

> [!IMPORTANT]
> 이 랩은 **public 저장소**를 전제로 합니다.
> public 저장소에서는 코드 스캐닝, 시크릿 스캐닝, 푸시 보호, 의존성 그래프가 무료입니다.
> Security Overview 와 커스텀 시크릿 패턴은 유료라서 이 랩의 채점 대상이 아닙니다.

## 소요 시간

약 30분, 4단계

## 시작하는 법

1. 오른쪽 위 **Use this template → Create a new repository** 를 누릅니다.
2. 소유자는 본인 계정, 공개 범위는 **Public** 으로 둡니다.
3. 만들고 20초쯤 기다렸다가 새로고침하면 첫 단계가 이슈로 열립니다.
