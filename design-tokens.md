# design-tokens.md — doosolution 디자인 토큰 원장

> 이 문서는 `design-guide.md`(브랜드 설명·원칙)와 실제 코드(`tokens/tokens.css`, `tokens/tokens.json`) 사이의
> **번역판**입니다. 값 자체는 여기서 만들지 않고 `design-guide.md`에서 파생되며, 값을 바꿀 때는 세 파일
> (`design-guide.md`, `tokens/tokens.css`, `tokens/tokens.json`)을 함께 갱신합니다.
>
> **사용법**: 새 프로젝트를 시작할 때 `tokens/tokens.css`를 프로젝트의 전역 스타일(예: `globals.css`,
> `index.css`)에 그대로 복사하거나 `@import`합니다. Tailwind 등 유틸리티 프레임워크를 쓰는 프로젝트는
> `tokens/tokens.json`을 `theme.extend`에 매핑해 사용합니다.
> 토큰 이식 시 원본을 복사해서 시작할 것.

## 1. 파일 구성

| 파일 | 형식 | 용도 |
|---|---|---|
| `tokens/tokens.css` | CSS Custom Properties | 프로젝트에 직접 복사해서 쓰는 실행 가능한 토큰. 라이트(기본)/다크(`prefers-color-scheme` 또는 `data-theme`) 자동 전환 포함 |
| `tokens/tokens.json` | JSON | 빌드 도구, Tailwind config, Style Dictionary, Figma 플러그인 등에서 프로그래밍적으로 읽기 위한 동일 값의 평문 버전 |

## 2. 브랜드 컬러

| 토큰 | 값 |
|---|---|
| `--brand-indigo` | `#5B5FEE` |
| `--brand-indigo-hover` | `#4A4DD6` |
| `--brand-indigo-strong` | `#3D3FB8` |
| `--brand-violet` | `#8B5CF6` |
| `--brand-cyan` | `#22D3EE` |
| `--brand-lime` | `#B6FF3B` |
| `--brand-gradient` | `linear-gradient(135deg, var(--brand-indigo) 0%, var(--brand-violet) 55%, var(--brand-cyan) 100%)` |

## 3. 뉴트럴 · 시맨틱 컬러 (테마별)

| 토큰 | 라이트 | 다크 |
|---|---|---|
| `--surface-0` | `#FFFFFF` | `#0B0B10` |
| `--surface-1` | `#F7F7FA` | `#131318` |
| `--surface-2` | `#EEEEF3` | `#1C1C24` |
| `--surface-elevated` | `#FFFFFF` | `#20202B` |
| `--border-subtle` | `#E3E3EA` | `#2A2A34` |
| `--border-strong` | `#C7C7D1` | `#3A3A46` |
| `--text-primary` | `#14141A` | `#F5F5F7` |
| `--text-secondary` | `#5C5C6B` | `#A0A0AE` |
| `--text-muted` | `#8B8B98` | `#6B6B7A` |
| `--text-disabled` | `rgba(20,20,26,.38)` | `rgba(245,245,247,.38)` |
| `--overlay` | `rgba(10,10,14,.4)` | `rgba(6,6,10,.6)` |
| `--focus-ring` | `var(--brand-indigo)` | `var(--brand-indigo)` |
| `--selection-bg` | `var(--brand-lime)` | `var(--brand-lime)` |
| `--color-success` | `#1F9D5C` | `#2FD180` |
| `--color-warning` | `#B57A0A` | `#F5B942` |
| `--color-danger` | `#D6303B` | `#F14F5A` |
| `--color-info` | `#1D6FC7` | `#4EA1FF` |
| `--shadow-sm` | `0 1px 2px rgba(20,20,26,.06)` | `0 1px 2px rgba(0,0,0,.3)` |
| `--shadow-md` | `0 4px 16px rgba(20,20,26,.08)` | `0 4px 20px rgba(0,0,0,.4)` |
| `--shadow-lg` | `0 12px 32px rgba(20,20,26,.12)` | `0 16px 40px rgba(0,0,0,.5)` |

## 4. 라운드

| 토큰 | 값 | 허용 대상 |
|---|---|---|
| `--radius-xs` | `2px` | 컴팩트 버튼/컨트롤 |
| `--radius-sm` | `4px` | **기본값** — 버튼, 인풋, 카드, 패널, 모달, 알림 |
| `--radius-lg` | `8px` | 배지·태그 전용 |
| `--radius-full` | `999px` | 필(pill) 배지·태그, 아바타 전용 |

## 5. 타이포그래피

`--font-sans`: `'Pretendard Var', -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Malgun Gothic', sans-serif`
`--font-mono`: `'JetBrains Mono', ui-monospace, Consolas, monospace`

| 스케일 | size | line | weight |
|---|---|---|---|
| `display` | 56px | 1.1 | 700 |
| `h1` | 40px | 1.15 | 700 |
| `h2` | 30px | 1.2 | 600 |
| `h3` | 22px | 1.3 | 600 |
| `body-lg` | 18px | 1.6 | 400 |
| `body` | 16px | 1.6 | 400 |
| `sm` | 14px | 1.5 | 400 |
| `xs` | 12px | 1.4 | 500 |

## 6. 스페이싱

4px 그리드: `4 · 8 · 12 · 16 · 24 · 32 · 48 · 64 · 96 · 128` (px) → `--space-4` ~ `--space-128`

## 7. 모션

| 토큰 | 값 |
|---|---|
| `--ease-standard` | `cubic-bezier(0.16, 1, 0.3, 1)` |
| `--duration-micro` | `180ms` (호버, 포커스 등 150–200ms 범위의 대표값) |
| `--duration-layout` | `300ms` (레이아웃 전환 250–350ms 범위의 대표값) |

## 8. 폼 컨트롤 & 버튼 높이 스케일

| 크기 | 높이 | 인풋 좌우 패딩 | 버튼 좌우 패딩 |
|---|---|---|---|
| `xs` | 28px | 8px | 10px |
| `sm` | 35px | 10px | 14px |
| `md` | 40px (기본) | 12px | 18px |
| `lg` | 48px | 16px | 24px |

## 9. 아이콘

Remixicon, `-line` 기본 / `-fill`은 활성 상태 전용. 크기: `--icon-sm 16px` · `--icon-md 20px` · `--icon-lg 24px`

## 10. Z-Index 레이어

`agent-dev-guide.md` §13에서 "레이어 체계를 정의한다"고만 되어 있던 부분을 여기서 확정합니다.

| 토큰 | 값 | 레이어 |
|---|---|---|
| `--z-dropdown` | 100 | 드롭다운, 셀렉트 옵션 |
| `--z-sticky` | 200 | sticky 헤더/테이블 헤더 |
| `--z-tooltip` | 300 | 툴팁 |
| `--z-drawer` | 400 | 드로어/사이드 패널 |
| `--z-modal` | 500 | 모달/다이얼로그 |
| `--z-toast` | 600 | 토스트 (항상 최상단) |

## 11. 브레이크포인트

CSS 커스텀 프로퍼티는 `@media` 조건 안에서 직접 쓸 수 없으므로, 이 값들은 `tokens.json`에만 존재하고
Tailwind `screens` 설정이나 JS 반응형 로직(`matchMedia`)에서 사용합니다.

| 이름 | 최소 너비 |
|---|---|
| `mobile` | 0px |
| `tablet` | 640px |
| `desktop` | 1024px |
| `wide` | 1440px |

## 12. 유지보수 원칙

- 새 토큰이 필요해지면(예: 새 시맨틱 컬러, 새 컴포넌트 크기) 먼저 `design-guide.md`(또는 해당 기능이
  속한 가이드)에 원칙과 함께 정의한 뒤, 이 문서와 `tokens/*.css`·`tokens/*.json`에 반영합니다. 코드에서
  토큰을 먼저 추가하고 문서화를 나중으로 미루지 않습니다.
- 토큰 이름을 바꿀 때는 이 저장소의 `samples/*.html` 6개 파일에서도 같은 이름을 쓰는지 검색해 확인합니다.
