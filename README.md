# doosolution AI 작업 가이드 시스템

doosolution의 UI/UX 아이덴티티를 기반으로, AI(Claude Code 등)를 활용해 작업할 때 작업 성격별로 참고해야 할
표준 가이드 모음입니다. 각 가이드는 독립적으로 쓰이지 않고, `design-guide.md`에 정의된 브랜드 DNA를
공통 기반으로 삼아 파생됩니다.

```
design-guide.md  (브랜드 아이덴티티 / 디자인 시스템 — 모든 가이드의 기반)
        │
        ├── design-tokens.md            (토큰 원장 — tokens/tokens.css, tokens/tokens.json)
        ├── content-voice-guide.md      (보이스 앤 톤 상세 가이드)
        │
        ├── agent-dev-guide.md          (사용자단 UI/UX·프론트엔드 개발 가이드)
        │       ├── agent-dev-security-guide.md  (사용자단 보안 가이드)
        │       └── agent-seo-guide.md            (사용자단 SEO 가이드)
        │
        └── manage-dev-guide.md         (관리자 대시보드 UI/UX·개발 가이드)
                └── manage-dev-security-guide.md  (관리자 보안 가이드)
```

## 용어 정의

- **agent(에이전트)단**: 프로젝트 관리자가 아닌 최종 사용자가 마주하는 결과물. 랜딩페이지, 쇼핑몰,
  모바일 앱, 데스크탑 앱 등 프로젝트 유형에 따라 UI/UX 톤앤매너가 달라질 수 있음.
- **manage(관리자)단**: 어드민 대시보드. 프로젝트 유형이 달라져도 UI/UX 톤앤매너는 크게 변하지 않음
  (데이터 밀도, 생산성 중심 설계가 우선).

## 가이드 목록 및 진행 상태

| 파일 | 목적 | 상태 |
|---|---|---|
| `design-guide.md` | 브랜드 아이덴티티(색상·타이포·모션 등 디자인 토큰)와 톤앤매너 원칙 | 완료 |
| `agent-dev-guide.md` | 사용자단 프론트엔드 개발/컴포넌트 가이드 | 완료 |
| `agent-dev-security-guide.md` | 사용자단 보안 가이드 (XSS, 결제, 입력값 검증 등) | 완료 |
| `agent-seo-guide.md` | 사용자단 SEO/메타데이터/구조화 데이터 가이드 | 완료 |
| `manage-dev-guide.md` | 관리자 대시보드 개발/컴포넌트 가이드 | 완료 |
| `manage-dev-security-guide.md` | 관리자 보안 가이드 (인증, 권한, 감사로그 등) | 완료 |
| `design-tokens.md` | 모든 가이드가 참조하는 디자인 토큰 원장 (`tokens/tokens.css`, `tokens/tokens.json` 포함) | 완료 |
| `content-voice-guide.md` | 카피라이팅/보이스앤톤 가이드 (UI 문구, 에러 메시지 등) | 완료 |

각 가이드는 작성 후 `samples/` 폴더에 해당 가이드를 시각화한 샘플 HTML을 만들어 사용자와 함께
튜닝하는 방식으로 완성합니다.

## 브랜드 한 줄 정의

**doosolution: 심플하고 세련되며, 젊고 혁신적인 느낌의 개발회사.**
