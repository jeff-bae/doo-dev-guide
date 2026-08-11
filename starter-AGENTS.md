# AGENTS.md — [프로젝트명]

이 프로젝트는 **doosolution**의 [ agent단 / manage단 ] 프로젝트입니다.
디자인/개발/보안 작업은 아래 가이드 저장소를 기준으로 합니다: `[doo-dev-guide 로컬 경로]`
(저장소가 로컬에 없다면 `git@github.com:jeff-bae/doo-dev-guide.git`에서 clone한 뒤 경로를 채우세요.
이 경로는 프로젝트/기기마다 다르므로 복사할 때마다 실제 경로로 바꿔 씁니다.)

이 파일은 Codex 등 `AGENTS.md`를 자동으로 읽는 AI 코딩 도구용입니다. Claude Code를 쓰는 경우
같은 내용을 담은 `starter-CLAUDE.md`를 `CLAUDE.md`로 복사해서 사용하세요 — 두 파일은 대상 도구만
다르고 내용은 동일하게 유지합니다.

## 프로젝트 성격

- 유형: [ 랜딩페이지 / 쇼핑몰 / 모바일 앱 / 데스크탑 앱 / 관리자 대시보드 ]
- 톤 (agent-dev-guide.md §4 기준, manage단이면 생략 — manage-dev-guide.md §1 고정값 사용):
  - 과감함: [ 낮음 / 중간 / 높음 ]
  - 모션 강도: [ 낮음 / 중간 / 높음 ]
  - 정보 밀도: [ 낮음 / 중간 / 높음 ]
  - 기본 테마: [ 다크 / 라이트 ]

## 반드시 참고할 가이드

모든 작업에 공통:
- `design-guide.md` — 브랜드 아이덴티티(색상·타이포·라운드·모션·아이콘 토큰). 최상위 기준.
- `design-tokens.md`, `tokens/tokens.css` — 실제 토큰 값. **이 프로젝트의 전역 스타일에 이미 병합되어 있어야 함** (`tokens/tokens.css`를 globals.css 등에 복사).
- `content-voice-guide.md` — UI 문구 작성 시 참고 (합니다체 기본, 이모지 절대 금지, 유형별 카피 예시)

이 프로젝트가 agent단이면:
- `agent-dev-guide.md` — 컴포넌트, 상태 카탈로그(loading/empty/error), 반응형, 접근성
- `agent-dev-security-guide.md` — XSS, 인증/세션, 결제, 파일 업로드 등
- `agent-seo-guide.md` — 웹 기반(랜딩/쇼핑몰)인 경우만 해당. 모바일/데스크탑 앱은 제외.

이 프로젝트가 manage단이면:
- `manage-dev-guide.md` — 사이드바+테이블 레이아웃, 필터, 벌크 액션 등
- `manage-dev-security-guide.md` — RBAC, 감사 로그, 재인증, 환경 구분

## 다른 전역 스킬/지침과의 우선순위

`ui-ux-pro-max-codex` 같은 전역 UI/UX 스킬이 함께 설치되어 있더라도, **이 저장소의 가이드와
이 프로젝트의 실제 요구사항·기존 코드가 항상 우선**합니다. 전역 스킬의 제안은 참고 자료로만
쓰고, 여기 정의된 색상·라운드·타이포·컴포넌트 규칙과 충돌하면 이 저장소를 따릅니다.

## 작업 시 바로 적용할 규칙 (요약)

- 이모지 사용 금지. 아이콘은 Remixicon(`-line` 기본, `-fill`은 활성 상태 전용)만 사용.
- 버튼·인풋·카드 등 테두리 있는 박스의 라운드는 4px 이하(`--radius-xs`/`--radius-sm`). 4px 초과는 배지·태그에만.
- 폼 컨트롤·버튼 높이는 xs(28px)/sm(35px)/md(40px, 기본)/lg(48px) 스케일만 사용. 인풋+버튼을 나란히 붙일 때는 같은 크기끼리.
- 그림자는 모달/팝오버/드롭다운처럼 떠 있는 레이어에만(`--surface-elevated` + `--shadow-lg`). 일반 카드엔 사용 안 함.
- 모든 화면은 loading/empty/error/success 상태를 최소한 설계.
- UI 문구는 합니다체, 반말·해요체·과장 표현 금지. 버튼은 결과를 설명하는 문구로.

## 이 프로젝트에서 새로 발견한 패턴은?

가이드에 없는 컴포넌트/원칙이 필요해지면, 이 프로젝트에서 먼저 구현하고 끝내지 말고
`[doo-dev-guide 로컬 경로]`에도 반영을 검토합니다(가이드는 살아있는 문서입니다). `starter-CLAUDE.md`와
`starter-AGENTS.md`는 항상 같은 내용을 유지하세요 — 한쪽만 갱신하고 다른 쪽을 잊지 않도록 합니다.
