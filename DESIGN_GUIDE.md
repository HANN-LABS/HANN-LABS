# HannWorks™ Design Guide

토큰·규칙 정의는 `DESIGN_SYSTEM.md` 참고. 이 문서는 실제로 새 페이지/섹션을 만들 때 따라야 할 절차입니다.

## 새 내부 페이지 추가 절차

1. `/새경로/index.html` 폴더 구조로 생성 (GitHub Pages 클린 URL 규칙 — 폴더명 = URL 경로)
2. 기존 페이지(`about/index.html`, `partnership/index.html`)의 `<head>`~`</style>`, nav, footer, `<script>` 블록을 그대로 복사 — 절대 새로 작성하지 않기 (일관성 훼손 방지)
3. 본문만 `<div class="ipg">...</div>` 안에 작성
4. 모든 텍스트/카드 요소에 `.rv` + `.d1~.d5` 클래스 부여
5. `<title>`, `og:*`, `twitter:*`, `canonical` 메타태그를 페이지에 맞게 수정
6. 완성 후 Playwright 등으로 DOM 텍스트 추출 + `pageerror` 리스너로 콘솔 에러 없는지 확인 (스크린샷 대신 텍스트 기반 검증도 가능)
7. 루트 `index.html`, `footer`의 `.ftr-nav`, 필요시 `about/index.html`·`partnership/index.html`의 nav에도 새 링크 추가

## 체크리스트 (커밋 전)

- [ ] 로고 SVG path가 원본과 동일한가
- [ ] 폰트가 Noto Sans KR / Inter 외 다른 걸로 안 바뀌었는가
- [ ] 브랜드 블루가 `#1a1de8` 그대로인가
- [ ] 새 섹션에 reveal 클래스(.rv 등)가 빠짐없이 들어갔는가
- [ ] 모바일(≤860px) 햄버거 메뉴에도 새 링크가 반영됐는가
- [ ] `<a>`/버튼에 `cursor:none` (커스텀 커서 유지) 처리됐는가
- [ ] 개인정보/약관처럼 민감 정보가 들어가는 페이지는 이메일·디스코드 등 연락처만 노출하고, 출처가 불분명한 문자열(암호로 보이는 값 등)은 임의로 게시하지 않기

## 커밋 메시지 컨벤션

```
feat(site): 메인 페이지 HannWorks™ 리브랜딩
feat(about): About 상세페이지 추가
feat(partnership): 파트너십 제안 페이지 KO/EN 추가
feat(legal): 개인정보처리방침·이용약관 추가
docs: 디자인 시스템/가이드 문서 추가
```

## 배포

- 호스팅: GitHub Pages (레포 루트 = 사이트 루트)
- 커스텀 도메인: `hannworks.kro.kr` → 레포 루트 `CNAME` 파일 필수
- kro.kr DNS: `CNAME` 레코드 `hannworks` → `<org>.github.io` (소문자)
- GitHub 레포 Settings → Pages → Custom domain 등록 + Enforce HTTPS
