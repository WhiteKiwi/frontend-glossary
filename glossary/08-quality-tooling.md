# 품질·개발 · 접근성·보안·도구

> [전체 목차](../README.md) · [알파벳 색인](../INDEX.md) · [참고 자료](../REFERENCES.md)

이 문서의 용어는 이해하기 쉬운 요약 정의입니다. 구체적인 동작은 공식 명세·디자인 시스템에 따라 달라질 수 있습니다.

| 용어 | 설명 | 예시·활용 |
| --- | --- | --- |
| **a11y** | Accessibility의 약어; 다양한 사용자가 서비스를 이용할 수 있도록 하는 접근성. | 키보드 조작 |
| **WCAG** | 웹 콘텐츠 접근성 지침. | 대비·포커스 기준 |
| **ARIA** | 접근성 트리 의미·상태·관계를 보완하는 속성 체계. | aria-expanded |
| **Accessible Name** | 보조기술이 요소를 식별할 때 읽는 이름. | 버튼 텍스트 |
| **Screen Reader** | 화면 내용을 음성 등으로 전달하는 보조기술. | VoiceOver |
| **Tab Order** | Tab 키로 이동하는 포커스 순서. | 논리적 순회 |
| **Landmark** | 문서 주요 구역을 표현하는 접근성 구조. | main·navigation |
| **Semantic Role** | 요소의 역할을 나타내는 접근성 정보. | button role |
| **Color Contrast Ratio** | 전경·배경의 상대 휘도 대비 비율. | 본문 4.5:1 기준 |
| **Alt Text** | 이미지의 의미를 설명하는 대체 텍스트. | alt 속성 |
| **SEO** | 검색엔진이 콘텐츠를 발견·이해하도록 돕는 최적화. | 메타데이터 |
| **Canonical URL** | 중복·유사 페이지의 대표 URL 신호. | rel=canonical |
| **Open Graph** | 링크 공유 미리보기 정보를 표현하는 메타데이터 규격. | og:title |
| **Sitemap** | 검색엔진 등에 URL 구조를 제공하는 파일. | sitemap.xml |
| **Robots.txt** | 크롤러 접근 권장 규칙을 담는 파일. | Disallow |
| **Structured Data** | 콘텐츠 의미를 기계가 이해할 수 있게 표현한 데이터. | JSON-LD |
| **Unit Test** | 작은 함수·컴포넌트 단위를 검증하는 테스트. | 가격 포맷 함수 |
| **Integration Test** | 여러 단위가 연결된 동작을 검증하는 테스트. | 폼과 API mock |
| **E2E Test** | 실제 사용자 경로에 가까운 끝단 흐름 테스트. | 로그인→주문 |
| **Visual Regression** | 화면 스냅샷 비교로 시각 변화를 감지하는 테스트. | 컴포넌트 이미지 diff |
| **Snapshot Test** | 기대 직렬화 결과의 변화 여부를 비교하는 테스트. | 렌더 구조 snapshot |
| **Mock** | 실제 의존 대상을 대체한 테스트 객체·동작. | 가짜 API |
| **Stub** | 미리 정한 응답을 반환하도록 만든 대체 구현. | 고정 시간 반환 |
| **Fixture** | 테스트 조건을 구성하는 사전 준비 데이터. | 샘플 사용자 |
| **Test Pyramid** | 단위·통합·E2E 테스트 비중을 설계하는 관점. | 빠른 테스트 다수 |
| **Flaky Test** | 코드 변화 없이도 성공·실패가 불안정한 테스트. | 비동기 타이밍 |
| **XSS** | 악성 스크립트가 웹 페이지 맥락에서 실행되는 취약점. | 사용자 HTML 삽입 |
| **CSRF** | 사용자 인증 상태를 악용해 의도치 않은 요청을 유도하는 공격. | 위조 폼 요청 |
| **CSP** | 브라우저 리소스 실행·로드 출처를 제한하는 보안 정책. | script-src |
| **SRI** | 외부 리소스 무결성을 해시로 검증하는 기술. | integrity 속성 |
| **Authentication** | 사용자가 누구인지 확인하는 절차. | 로그인 |
| **Authorization** | 인증된 주체의 자원 접근 권한을 판단하는 절차. | 관리자 권한 |
| **OAuth 2.0** | 제한된 리소스 접근을 위임하기 위한 권한 부여 프레임워크. | 외부 계정 연동 |
| **OIDC** | OAuth 2.0 위에서 사용자 인증 정보를 제공하는 프로토콜. | ID Token |
| **JWT** | JSON 기반 클레임을 서명·암호화 등의 방식으로 표현하는 토큰 형식. | 액세스 토큰 |
| **SameSite Cookie** | 사이트 간 쿠키 전송을 제어하는 속성. | SameSite=Lax |
| **HttpOnly Cookie** | JavaScript에서 쿠키 값 접근을 막는 속성. | 세션 쿠키 |
| **Secure Cookie** | 안전한 채널에서만 쿠키를 보내도록 하는 속성. | Secure |
| **Bundler** | 의존 모듈·자산을 배포 단위로 묶는 도구. | Vite·Webpack |
| **Transpiler** | 소스코드를 다른 표현·문법 수준으로 변환하는 도구. | TS→JS |
| **Polyfill** | 환경에 없는 표준 기능을 코드로 보완하는 구현. | 구형 브라우저 대응 |
| **HMR** | Hot Module Replacement; 페이지 전체 새로고침 없이 일부 모듈을 교체. | 개발 중 스타일 즉시 반영 |
| **Source Map** | 변환된 코드 위치를 원본 소스에 대응시키는 정보. | 번들 디버깅 |
| **Lint** | 정적 규칙으로 스타일·잠재 오류를 검사. | ESLint |
| **Formatter** | 코드 형식을 일관되게 자동 정렬하는 도구. | Prettier |
| **CI** | Continuous Integration; 변경사항을 자동 검증·통합하는 과정. | PR 테스트 |
| **CD** | Continuous Delivery/Deployment; 배포 준비 또는 실제 배포를 자동화. | 릴리스 파이프라인 |
| **Feature Flag** | 기능 공개 여부를 설정으로 제어하는 장치. | 점진 배포 |
| **Observability** | 로그·메트릭·트레이스 등으로 시스템 동작을 이해하는 능력. | 오류 추적 |
| **Sentry** | 클라이언트 오류·성능 데이터를 수집하는 서비스의 대표 예. | 프론트 오류 알림 |

## 참고 자료

전체 참고 링크와 영역별 자료는 [REFERENCES.md](../REFERENCES.md)에 정리했습니다.
