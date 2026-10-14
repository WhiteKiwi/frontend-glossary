# 품질·개발 도구

> 접근성·SEO·보안·테스트·빌드 환경

[← 전체 목차](../README.md) · [알파벳 색인](../INDEX.md)

| 용어 | 설명 | 예시·주의점 |
| --- | --- | --- |
| **Accessibility (a11y)** | 장애 유무와 관계없이 이용할 수 있도록 설계·구현하는 품질 | 키보드와 스크린리더 지원. |
| **WCAG** | 웹 콘텐츠 접근성 권고 지침 | 색 대비·키보드 접근. |
| **ARIA** | 의미·상태·속성을 보완해 접근성 정보를 제공하는 기술 | aria-expanded. |
| **Accessible Name** | 보조 기술이 컨트롤을 식별하는 이름 | 아이콘 버튼의 aria-label. |
| **Screen Reader** | 화면 정보를 음성 등으로 전달하는 보조 기술 | VoiceOver. |
| **Tab Order** | 키보드 탭 키로 이동하는 포커스 순서 | 자연스러운 DOM 순서 유지. |
| **Focus Management** | 화면 변경 후 올바른 위치에 포커스를 배치하는 처리 | 모달 닫고 원래 버튼 복귀. |
| **Live Region** | 동적으로 바뀐 콘텐츠를 보조 기술에 알리는 영역 | aria-live 상태 안내. |
| **Semantic HTML** | HTML의 원래 의미를 살려 사용하는 방식 | button을 div 대신 사용. |
| **SEO** | 검색엔진이 콘텐츠를 발견·이해할 수 있게 최적화 | title·내부 링크. |
| **Meta Description** | 페이지 요약을 제공하는 메타 태그 | 검색 결과 설명 후보. |
| **Canonical URL** | 중복 URL에서 대표 URL을 안내 | rel=canonical. |
| **Open Graph** | 링크 공유 미리보기에 쓰는 메타데이터 규약 | og:title, og:image. |
| **Structured Data** | 페이지 정보를 기계가 해석할 수 있게 기술한 데이터 | JSON-LD. |
| **Sitemap** | 크롤러에 URL 목록을 제공하는 파일 | sitemap.xml. |
| **Robots.txt** | 크롤러 접근 정책을 안내하는 파일 | Disallow 규칙; 보안 통제가 아니다. |
| **Unit Test** | 작은 단위의 로직 동작을 검증하는 테스트 | 유틸 함수. |
| **Integration Test** | 여러 구성요소의 연동 동작을 검증 | 컴포넌트와 API 통합. |
| **E2E Test** | 사용자 관점에서 처음부터 끝까지 검증 | 로그인→주문. |
| **Visual Regression Test** | UI 스크린샷 등의 시각적 차이를 비교 | CSS 회귀 검출. |
| **Snapshot Test** | 저장된 출력 결과와 현재 결과를 비교 | 컴포넌트 구조 변화. |
| **Mock** | 테스트에서 외부 의존성을 대체하는 객체·동작 | API 응답 모의. |
| **Stub** | 정해진 응답을 제공하는 테스트 대역 | 항상 성공 리턴. |
| **Fixture** | 테스트에서 재사용하는 준비 데이터 | 가짜 사용자 JSON. |
| **Test Coverage** | 테스트가 코드 영역을 얼마나 실행했는지 나타내는 측정값 | 분기 커버리지. |
| **XSS** | 악성 스크립트를 페이지에 주입하는 공격 | 출력 인코딩·안전한 DOM API. |
| **CSRF** | 인증된 사용자의 의도치 않은 요청을 유도하는 공격 | CSRF 토큰. |
| **CSP** | 스크립트 등의 출처를 제한하는 브라우저 정책 | script-src. |
| **Dependency** | 프로젝트가 사용하는 외부 라이브러리·패키지 | react. |
| **Package Manager** | 의존성 설치와 버전 관리를 수행하는 도구 | npm, pnpm. |
| **Bundler** | 소스 모듈을 처리해 배포 자산을 생성하는 도구 | Vite/Rollup/Webpack. |
| **Transpiler** | 코드 문법을 다른 형태의 코드로 변환 | TypeScript→JavaScript. |
| **Polyfill** | 환경에 없는 웹 API의 동작을 보완하는 코드 | 필요한 구형 브라우저 지원. |
| **HMR (Hot Module Replacement)** | 페이지 전체 새로고침 없이 개발 중 모듈 교체 | CSS 변경 즉시 확인. |
| **Source Map** | 빌드된 코드와 원본 코드 위치를 연결하는 파일 | 프로덕션 에러 역추적. |
| **Linting** | 코드 규칙 위반이나 잠재 문제를 정적으로 찾는 작업 | ESLint. |
| **Formatting** | 코드의 표기 형식을 일관되게 자동 정리 | Prettier. |
| **CI/CD** | 검증·빌드·배포 작업을 자동화하는 파이프라인 | PR 테스트. |
| **Feature Flag** | 기능 노출을 설정으로 제어하는 방식 | 점진적 출시. |
| **A/B Testing** | 사용자 집단별 변형을 비교하는 실험 | 전환율 비교. |

---

관련 참고 문헌은 [REFERENCES.md](../REFERENCES.md)에서 확인할 수 있습니다.
