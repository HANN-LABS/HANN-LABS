# 🗂️ HANN LABS™ — 마스터 프롬프트 & 전체 진행 기록
> 최종 업데이트: 2026-07-02
> 새로운 대화 세션에 이 문서를 붙여넣어 이전 맥락을 즉시 복원할 수 있습니다.

---

## 📌 프로젝트 기본 정보

| 항목 | 내용 |
|------|------|
| **프로젝트명** | HANN LABS™ 브랜드 사이트 |
| **로컬 경로** | `c:\Users\oxoxo\Documents\HANN LABS™` |
| **기술 스택** | Vanilla HTML + CSS + JavaScript (단일 파일) |
| **폰트** | Noto Sans KR + Inter (Google Fonts CDN) |
| **배포 파일** | `index.html` (단일 파일 SPA) |
| **빌드 도구** | 없음 (순수 HTML, 빌드 불필요) |
| **로컬 열기** | `index.html` 파일 직접 브라우저 오픈 |

---

## 🏢 브랜드 기본 정보

| 항목 | 내용 |
|------|------|
| **브랜드명** | HANN LABS™ |
| **한국어 이름** | 한랩스 |
| **슬로건 (KO)** | 한 걸음 앞선 시선으로, 한 걸음 앞선 트렌드를 디자인하다. |
| **슬로건 (EN)** | Designing trends one step ahead. |
| **디자인 언어** | 설계된 단순함 (Designed Simplicity) |
| **서비스 시작일** | 2026년 3월 28일 |
| **Discord** | h4nn.exe |
| **이메일** | seop.vn@gmail.com |

### 브랜드 아이덴티티
- **로고:** H와 N 자를 기하학적으로 결합한 커스텀 SVG 마크 (HN 모노그램)
- **컬러:** 딥 블루(`#1a1de8`) + 퓨어 블랙(`#000000`) + 퓨어 화이트(`#ffffff`)
- **무드:** 미니멀리즘 × 정교함 × 트렌드

### 디자인 철학 (3대 축)
1. **미니멀리즘** — 미니멀리즘을 통해 기억하기 쉬운 시각적 효과를 만들어냅니다.
2. **정교함** — 단순하면서도 정교한 디자인으로 시각적 안정감을 줍니다.
3. **트렌드** — 트렌디한 디자인으로 새로운 느낌을 담아냅니다.

---

## 📋 서비스 목록 (What We Do)

| 서비스명 | 분류 |
|---------|------|
| 로고 디자인 | 브랜드 |
| 브랜딩 | 브랜드 |
| 배너 디자인 | 그래픽 |
| 그래픽 디자인 | 그래픽 |
| 디자인 캠페인 | 캠페인 |
| 포스터 디자인 | 그래픽 |
| 브랜드 설계 | 브랜드 |
| 디자인 강의 | 교육 |
| 상세페이지 디자인 | 그래픽 |

---

## 📊 실적 / 통계

| 지표 | 수치 | 설명 |
|------|------|------|
| 디자인·브랜딩 만족도 | **96%** | 클라이언트 만족 응답률 |
| 재의뢰율 | **90%** | 의뢰인 디자인 재의뢰 비율 |
| 완료 프로젝트 | **10+** | 성공적으로 완료된 프로젝트 수 |

---

## 🎨 디자인 시스템

### 컬러 팔레트
| 변수 | 값 | 용도 |
|------|-----|------|
| `--blue` | `#1a1de8` | 메인 브랜드 블루 |
| `--blue-light` | `#4545ff` | 강조 / hover 상태 |
| `--blue-dark` | `#0d0dcc` | 그림자 / 깊이 |
| `--blue-glow` | `rgba(26,29,232,.55)` | 글로우 이펙트 |
| `--black` | `#000000` | 배경 (S1, S3, S7, S8, S9, S10) |
| `--white` | `#ffffff` | 텍스트 / 아이콘 |
| `Blue BG` | S5, S6 섹션 전용 | `var(--blue)` 배경 |

### 타이포그래피
| 폰트 | 용도 | 우선순위 |
|------|------|---------|
| **Noto Sans KR** | 한국어 본문 | 1위 |
| **Inter** | 영문 디스플레이·헤드라인 | 2위 |
| fallback | sans-serif | - |

### 애니메이션 CSS 변수
```css
--ease: cubic-bezier(.22, 1, .36, 1); /* spring 계열 커스텀 이징 */
```

---

## 🗺️ 사이트 구조 (10 섹션)

| 섹션 | ID | 배경 | 내용 |
|------|-----|------|------|
| S1 | `#s1` | Black + HG 블롭 | 히어로 — HN 대형 로고 |
| S2 | `#s2` | Black + 블루 블롭 | 태그라인 (단어 분할 애니메이션) |
| S3 | `#s3` | Black | 브랜드 소개 / 인용구 스타일 |
| S4 | `#s4` | 다크 그라디언트 | 키체인 굿즈 목업 |
| S5 | `#s5` | Blue | What We Do (서비스 태그 그리드) |
| S6 | `#s6` | Blue | 디자인 철학 (3개 원형 카드) |
| S7 | `#s7` | Black + 블루 블롭 | iPhone 목업 + 알림 |
| S8 | `#s8` | Black + 하단 글로우 | 통계 (SVG 링 + 카운트업) |
| S9 | `#s9` | Black | 디자인 프로세스 (벤 다이어그램) |
| S10 | `#s10` | Black + HG 블롭 | CTA — 연락처 |

---

## 🎭 애니메이션 목록

### CSS Keyframes
| 이름 | 동작 | 적용 위치 |
|------|------|---------|
| `breathTop` | 위 블롭 scale pulse | S1, S10 |
| `breathBot` | 아래 블롭 scale pulse (역방향) | S1, S10 |
| `blobDrift` | 블롭 scale + rotate drift | S2, S7 |
| `heroFloat` | 위아래 부유 | S1 로고 |
| `fadeUp` | 아래→위 페이드인 | S1 로고 최초 등장 |
| `keychainSway` | 좌우 흔들림 + 그림자 변환 | S4 키체인 |
| `glowPulse` | opacity + scale pulse | S4, S8 |
| `notifSlideUp` | 위로 슬라이드인 | S7 알림 |
| `vennGlow` | box-shadow 글로우 pulse | S9 벤 중심원 |
| `ctaFloat` | 위아래 부유 | S10 텍스트 |
| `tagPop` | scale + translateY 팝인 | S5 태그 |
| `wordReveal` | translateY 단어 reveal | S2 태그라인 |

### JavaScript 인터랙션
| 기능 | 설명 |
|------|------|
| **커스텀 커서** | 7px 도트 + 38px 링, 링은 lerp(.13) 지연 추적. hover 시 파랗게 확장 |
| **스크롤 프로그레스 바** | 상단 2.5px 그라디언트 바 (파랑→라이트블루→연보라) |
| **스크롤 reveal** | IntersectionObserver → `.rv`, `.rvL`, `.rvS` 클래스에 `.on` 부여 |
| **단어 분할 애니메이션** | S2 태그라인을 단어 단위로 split → 65ms 간격 순차 reveal |
| **태그 stagger** | S5 서비스 태그 72ms 간격 순차 tagPop 애니메이션 |
| **마그네틱 태그** | mousemove → translate 0.28배 적용, mouseleave → 원위치 |
| **3D 카드 틸트** | S6 철학 카드 mousemove → perspective 700px rotateX/Y 15도 |
| **SVG 링 카운트업** | IntersectionObserver 진입 시 stroke-dashoffset 1.9s, 숫자 ease-out cubic |
| **폰 알림 슬라이드** | S7 섹션 진입 0.9s 딜레이 후 notifSlideUp 실행 |
| **NAV 스크롤 효과** | scrollY > 60 시 `.sc` 클래스 → backdrop-blur + 배경 반투명 |

### 전환 딜레이 클래스
```
.d1 → 0.1s  .d2 → 0.22s  .d3 → 0.34s  .d4 → 0.46s  .d5 → 0.58s
```

---

## 📁 파일 구조

```
HANN LABS™/
├── index.html                     # 전체 사이트 (HTML + CSS + JS 단일 파일)
└── HANNLABS_MASTER_PROMPT.md      # 이 문서
```

### index.html 내부 구조
```
<head>
  Google Fonts (Noto Sans KR + Inter)
  <style> CSS 전체 (변수, 리셋, 커서, 스크롤바, keyframes, reveal, 섹션별 스타일, 반응형) </style>
</head>
<body>
  .c-dot + .c-ring          → 커스텀 커서
  #sp                        → 스크롤 프로그레스 바
  <nav>                      → 고정 네비게이션
  <section id="s1">          → 히어로
  <section id="s2">          → 태그라인
  <section id="s3">          → 소개 / 인용구
  <section id="s4">          → 굿즈 목업
  <section id="s5">          → 서비스
  <section id="s6">          → 철학
  <section id="s7">          → iPhone 목업
  <section id="s8">          → 통계
  <section id="s9">          → 프로세스
  <section id="s10">         → CTA
  <script> JS 전체 </script>
</body>
```

---

## 🧩 컴포넌트 상세

### 네비게이션 바 (nav)
- **위치:** fixed top-0, z-index 998
- **기본:** 패딩 24px 54px, 투명 배경
- **스크롤 후 (.sc):** 패딩 15px 54px, `rgba(0,0,0,.8)` + `backdrop-blur(22px)` + 하단 보더
- **메뉴:** 소개 / 서비스 / 철학 / 실적 / 문의하기(pill CTA)
- **로고:** 인라인 SVG HN 마크 (52×30px)

### 벤 다이어그램 (S9)
| 노드 | 클래스 | 위치 | 설명 |
|------|--------|------|------|
| 의미 | `.vm` | 좌상 | 어떤 메시지를 담을지 |
| 기획 | `.vp` | 우상 | 시각 구현 방법 구체화 |
| 구성 | `.vco` | 좌하 | 의미를 표현하는 구성 |
| 피드백 | `.vf` | 우하 | 의뢰인 의견 반영 |
| 정체성 | `.vnc` | 중앙 | 모든 요소의 교집합, 글로우 pulse |

### 키체인 목업 (S4)
- 메탈 링(`.kcr`) + 클립(`.kcc`) + 블루 본체(`.kcb`)
- 본체에 HN 로고 SVG 내장
- 전체가 `keychainSway` 애니메이션 (회전 + 부유)

### iPhone 목업 (S7)
- 290×594px, border-radius 52px
- 내부 상태바, 날짜/시간, 알림 카드
- 알림: "2026 한랩스 6월 리브랜딩 작업이 완료되었습니다"
- 섹션 진입 후 0.9초 딜레이로 알림 슬라이드인

---

## 🔗 연락처 / 문의

| 채널 | 주소 |
|------|------|
| **Discord** | h4nn.exe |
| **Email** | seop.vn@gmail.com |

---

## ⚙️ 중요 규칙 & 선호도

### 절대 하지 말 것 (금지)
1. 외부 JavaScript 라이브러리 사용 — 순수 Vanilla JS 유지
2. CSS 프레임워크(Tailwind 등) 사용 — 순수 CSS 유지
3. 여러 파일로 분리 — `index.html` 단일 파일 유지
4. HN 로고를 이미지 파일로 대체 — 반드시 인라인 SVG 사용
5. 블루 컬러를 임의로 변경 — `#1a1de8` 고정

### 반드시 해야 할 것
1. 모든 마우스 인터랙션 대상에 `cursor: none` 적용 (커스텀 커서 사용)
2. 새 섹션 추가 시 `.rv` / `.rvL` / `.rvS` + `.d1~.d5` reveal 클래스 적용
3. 블롭 배경은 항상 `pointer-events: none` 유지
4. SVG 로고는 동일한 HN 마크를 전 섹션에서 일관되게 사용

### 표현 규칙
| 항목 | 올바른 표현 | 잘못된 표현 |
|------|-----------|-----------|
| 스튜디오 이름 | HANN LABS™ | HANN LABS / HannLabs |
| 디자인 언어 | 설계된 단순함 | 심플함 / 단순미 |
| 서비스 시작 | 2026년 3월 28일부터 | — |
| 만족도 표시 | 96% / 90% | 퍼센트 기호 없이 표기 금지 |

---

## 📝 진행 기록

### Phase 1 — 초기 기획 (2026-07-02)
- 10장의 브랜드 슬라이드 이미지를 분석하여 사이트 구조 설계
- 슬라이드 순서 확정: 로고 → 태그라인 → 소개 → 키체인 목업 → 서비스 → 철학 → iPhone 목업 → 통계 → 프로세스 → CTA

### Phase 2 — 기본 구현 (2026-07-02)
- 단일 `index.html` 파일로 10섹션 구현
- 기본 스크롤 reveal(IntersectionObserver) 적용
- Python 빌더 스크립트(`build_site.py`)로 워크스페이스에 파일 생성

### Phase 3 — 애니메이션 고도화 (2026-07-02)
- ✅ 커스텀 커서 (도트 + lerp 추적 링, hover 확장)
- ✅ 스크롤 프로그레스 바 (그라디언트)
- ✅ 단어 분할 태그라인 애니메이션 (S2)
- ✅ 서비스 태그 마그네틱 + stagger 팝인 (S5)
- ✅ 철학 카드 3D 틸트 (S6)
- ✅ 폰 알림 딜레이 슬라이드인 (S7)
- ✅ 통계 SVG 링 + ease-out cubic 카운트업 (S8)
- ✅ 벤 다이어그램 중심 글로우 pulse (S9)
- ✅ 살아있는 블롭 (drift + breathe 애니메이션)
- ✅ 키체인 스웨이 + 그림자 연동 (S4)
- ✅ CTA 텍스트 플로팅 (S10)
- ✅ NAV 스크롤 반투명 전환

---

## 📝 남은 잠재적 작업 목록

- [ ] 실제 작업물 포트폴리오 갤러리 섹션 추가 (이미지 그리드)
- [ ] 디스코드 Webhook 연동 — 문의 폼 → 디스코드 채널 전송
- [ ] 모바일 전용 햄버거 메뉴 구현 (현재 nav-links 숨김 처리만)
- [ ] 다국어(EN) 지원 — 토글로 KO/EN 전환
- [ ] OG 메타태그 완성 (og:image 등 SNS 공유 최적화)
- [ ] GitHub Pages 배포 설정

---

## 🆕 새 대화 세션 시작 시 붙여넣을 핵심 컨텍스트

나는 HANN LABS™ 브랜드 사이트를 만들고 있어.

[프로젝트 경로]
c:\Users\oxoxo\Documents\HANN LABS™

[기술 스택]
Vanilla HTML + CSS + JavaScript (index.html 단일 파일)
폰트: Noto Sans KR + Inter (Google Fonts CDN)

[브랜드 정보]
- 브랜드명: HANN LABS™ (한랩스)
- 슬로건: 한 걸음 앞선 시선으로, 한 걸음 앞선 트렌드를 디자인하다.
- 디자인 언어: 설계된 단순함
- 컬러: #1a1de8 (브랜드 블루) + 검정 + 흰색
- 서비스 시작: 2026년 3월 28일
- Discord: h4nn.exe / Email: seop.vn@gmail.com

[사이트 구조 — 10섹션]
S1(히어로) → S2(태그라인) → S3(소개) → S4(키체인목업) →
S5(서비스) → S6(철학) → S7(iPhone목업) → S8(통계) →
S9(프로세스/벤다이어그램) → S10(CTA)

[중요 규칙]
1. 외부 라이브러리 사용 금지 — Vanilla JS + CSS 유지
2. index.html 단일 파일 유지
3. HN 로고는 항상 인라인 SVG 사용
4. 블루 컬러 #1a1de8 고정
5. 커스텀 커서 사용 → 모든 인터랙션 대상에 cursor:none
6. 새 요소엔 .rv + .d1~.d5 reveal 클래스 적용

[완료된 애니메이션]
커스텀 커서, 스크롤 프로그레스 바, 단어 분할 태그라인,
태그 마그네틱+stagger, 3D 카드 틸트, 폰 알림 슬라이드,
SVG 링 카운트업, 벤 글로우 pulse, 살아있는 블롭,
키체인 스웨이, CTA 플로팅, NAV 반투명 전환

---
이 문서는 프로젝트와 함께 지속 업데이트되어야 합니다.
