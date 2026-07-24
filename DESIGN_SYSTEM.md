# HannWorks™ Design System

> 브랜드: HANN LABS™(한랩스) → **HannWorks™(한워크스)** 로 리네이밍 (2026-07-24)
> 로고(HN 마크)·컬러·폰트·모션 언어는 변경 없이 그대로 계승합니다.

---

## 1. Brand

| 항목 | 값 |
|---|---|
| 브랜드명 | HannWorks™ |
| 한국어 표기 | 한워크스 |
| 설립일 | 2026년 3월 28일 |
| Discord | h4nn.exe |
| Email | seop.vn@gmail.com |
| 도메인 | https://hannworks.kro.kr |

**표기 규칙**
- 항상 `HannWorks™` (대소문자·™ 포함) — `Hannworks`, `HANNWORKS`, `한워크스™` 등 변형 금지
- 한글 표기는 `한워크스`로 통일

---

## 2. Logo

- 마크: "HN" 모노그램 (라운드 배지 없이 순수 글자 형태만 사용 — 2026-07-24 배지 제거)
- 원본 SVG path 고정, 재해석·재드로잉 금지
- 컬러 변형: 화이트(`#ffffff`, 다크 배경용), 블루(`--lgc` 커스텀 프로퍼티로 문맥별 제어)
- 최소 여백: 마크 높이의 50% 이상

```html
<svg viewBox="48 135 324 150" fill="none" xmlns="http://www.w3.org/2000/svg">
  <g transform="translate(0,420) scale(0.1,-0.1)">
    <path d="M760 2435 l0 -265 675 0 675 0 0 265 0 265 63 0 62 0 595 -595
    c327 -327 598 -595 602 -595 5 0 8 268 8 595 l0 595 65 0 65 0 0 -600
    0 -600 -157 0 -158 0 -507 507 -508 508 0 -508 0 -507 -65 0 -65 0
    0 265 0 265 -675 0 -675 0 0 -265 0 -265 -65 0 -65 0 0 600 0 600
    65 0 65 0 0 -265z" fill="var(--lgc,#ffffff)"/>
  </g>
</svg>
```

---

## 3. Color

| 토큰 | 값 | 용도 |
|---|---|---|
| `--blue` | `#1a1de8` | 메인 브랜드 블루 |
| `--blue-light` | `#4545ff` | 강조 / hover |
| `--blue-dark` | `#0d0dcc` | 그림자 / 깊이 |
| `--blue-glow` | `rgba(26,29,232,.55)` | 글로우 이펙트 |
| `--black` | `#000000` | 기본 배경 |
| `--white` | `#ffffff` | 텍스트 / 아이콘 |

블루·블랙·화이트 3색 고정. 임의의 색 추가 금지(그레이스케일 opacity 활용은 허용: `rgba(255,255,255,.4)` 등).

---

## 4. Typography

| 폰트 | 용도 | 굵기 |
|---|---|---|
| **Noto Sans KR** | 한국어 본문 (기본) | 300/400/500/700/900 |
| **Inter** | 영문 · 대형 헤드라인 · 숫자 · UI 라벨 | 300–900 |

- 헤드라인은 항상 `Inter`, `font-weight:900`, `letter-spacing:-.02~-.03em`
- 본문은 `Noto Sans KR` 상속(기본값), 줄간격 1.8~2.05
- Google Fonts CDN 로드 고정 — 로컬 폰트 파일로 대체 금지 (라이선스 정책상 CDN 로드가 원 계약 방식)

---

## 5. Motion / Easing

```css
--ease: cubic-bezier(.22, 1, .36, 1);
```

| 클래스 | 동작 |
|---|---|
| `.rv` | 아래→위 페이드인 (translateY 38px) |
| `.rvL` | 좌→우 페이드인 (translateX -42px) |
| `.rvS` | 스케일 페이드인 (scale .88→1) |
| `.d1`~`.d5` | 순차 딜레이 (.1s / .22s / .34s / .46s / .58s) |

새 섹션·컴포넌트 추가 시 반드시 `.rv`(또는 `.rvL`/`.rvS`) + `.d1~.d5` 조합으로 스크롤 reveal 적용. `IntersectionObserver` 기반, threshold 0.12.

커스텀 커서(도트+링, lerp 0.13 추적)는 전 페이지 공통 — 인터랙션 대상 요소는 `cursor:none` + hover 시 링 확장(`.hov` 클래스) 유지.

---

## 6. Layout Tokens

- 섹션 좌우 패딩: `8%` (데스크톱) / `24px` (≤640px)
- 내부 페이지 히어로 상단 여백: `150px` (고정 nav 높이 보정)
- 반응형 브레이크포인트: `860px`(nav 햄버거 전환), `640px`(그리드 1열 전환)
- 카드/버튼 radius: 파일/버튼류 `100px`(pill), 카드류 `14~20px`

---

## 7. Site Architecture

```
hannworks.kro.kr/
├── /                    메인 (브랜드 쇼케이스, 원페이지 스크롤)
├── /about               상세 소개 페이지 (About us, 실적, 서비스 상세)
├── /partnership          파트너십 제안 페이지 (KO, 기본)
├── /partnership/en       파트너십 제안 페이지 (EN)
├── /privacy              개인정보처리방침
└── /terms                이용약관
```

내부 페이지(About/Partnership/Privacy/Terms)는 메인과 동일한 `<style>`·커서·스크롤바·nav·footer·reveal 스크립트를 공유하고, 페이지 전용 CSS(`.iph`, `.ipsec`, `.statg`, `.svg4`, `.legalArt` 등)만 추가하는 구조. 폰트·컬러·모션은 단일 소스에서 파생되므로 임의 수정 시 전 페이지에 영향이 갑니다.

---

## 8. 절대 하지 말 것

1. 외부 JS/CSS 프레임워크 도입 — Vanilla 유지
2. 로고 재드로잉·색상 임의 변경
3. 브랜드 블루(`#1a1de8`) 변경
4. 폰트를 Noto Sans KR / Inter 외 다른 것으로 교체
5. 새 섹션에 reveal 클래스 누락
