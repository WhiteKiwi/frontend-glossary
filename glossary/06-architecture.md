# 아키텍처 · 설계와 렌더링

> [전체 목차](../README.md) · [알파벳 색인](../INDEX.md) · [참고 자료](../REFERENCES.md)

이 문서의 용어는 이해하기 쉬운 요약 정의입니다. 구체적인 동작은 공식 명세·디자인 시스템에 따라 달라질 수 있습니다.

| 용어 | 설명 | 예시·활용 |
| --- | --- | --- |
| **Component** | UI를 재사용 가능한 독립 단위로 나눈 구성 요소. | Button |
| **Composition** | 작은 단위를 조합해 복잡한 UI를 만드는 방법. | Card 내부 Avatar·Title |
| **Container/Presentational** | 데이터·로직과 화면 표현 책임을 나누는 패턴. | 목록 로더 + 리스트 |
| **Custom Hook** | 반복되는 상태·효과 로직을 재사용하도록 추출한 React 훅. | useDebounce |
| **Hook** | 함수 컴포넌트에 상태·생명주기 등의 기능을 연결하는 API. | useState |
| **Lifecycle** | 컴포넌트 생성·업데이트·제거 등의 수명 흐름. | mount/unmount |
| **Side Effect** | 순수한 값 계산 외에 외부 시스템에 영향을 주는 작업. | 구독·요청 |
| **Dependency Injection** | 필요한 의존 객체를 외부에서 주입하는 설계. | API client 주입 |
| **Separation of Concerns** | 서로 다른 관심사를 나누어 관리하는 원칙. | 화면·통신 로직 분리 |
| **SOLID** | 객체지향 설계를 돕는 다섯 가지 원칙 묶음. | 단일 책임 원칙 |
| **Atomic Design** | UI를 atoms·molecules·organisms 등 계층으로 분해하는 방법. | Button→SearchBar |
| **Design System** | 컴포넌트·패턴·토큰·사용 규칙의 일관된 체계. | 사내 UI 키트 |
| **Monorepo** | 여러 패키지·프로젝트를 하나의 저장소에서 관리. | 앱 + 공유 UI |
| **Microfrontend** | 여러 팀의 프론트 기능을 독립적으로 개발·배포·조합하는 구조. | 도메인별 앱 |
| **SPA** | 페이지 이동을 대체로 클라이언트에서 처리하는 Single Page Application. | 앱 셸 |
| **MPA** | 여러 문서를 서버로부터 탐색·전환하는 Multi Page Application. | 전통적인 다중 페이지 |
| **CSR** | 브라우저가 JavaScript로 주요 UI를 렌더링하는 전략. | 클라이언트 렌더 |
| **SSR** | 요청 시 서버에서 HTML을 생성하는 렌더링 전략. | 서버 렌더 |
| **SSG** | 빌드 시점에 HTML을 미리 생성하는 전략. | 정적 블로그 |
| **ISR** | 배포 후 정적 페이지를 갱신하는 특정 프레임워크의 점진적 재생성 전략. | Next.js ISR |
| **Hydration** | 서버가 만든 HTML에 클라이언트 이벤트·상태를 연결하는 과정. | React hydrate |
| **Streaming SSR** | HTML을 준비되는 순서대로 나눠 전송하는 서버 렌더링. | 점진적 콘텐츠 표시 |
| **React Server Components** | 일부 컴포넌트를 서버에서 실행·직렬화하는 React 모델. | RSC |
| **Islands Architecture** | 정적 HTML에서 필요한 작은 부분만 개별적으로 활성화하는 구조. | 아일랜드 인터랙션 |
| **Routing** | URL에 따라 화면·리소스를 연결하는 체계. | /users/:id |
| **Client-side Routing** | 전체 문서를 다시 로드하지 않고 브라우저에서 화면 전환. | SPA 링크 |
| **Nested Routing** | 부모·자식 경로의 UI를 계층적으로 구성. | 설정 공통 레이아웃 |
| **Dynamic Route** | URL 경로 일부를 변수로 다루는 라우팅. | /posts/[id] |
| **Layout Route** | 여러 하위 화면에서 공통 레이아웃을 공유하는 라우트. | 대시보드 셸 |
| **Middleware** | 요청·응답 등의 처리 흐름 사이에 끼어드는 공통 로직. | 인증 검사 |
| **BFF** | Backend for Frontend; 특정 클라이언트 요구에 맞춘 서버 계층. | 모바일 전용 응답 |
| **API Gateway** | 여러 백엔드 진입점을 하나로 통합·제어하는 관문. | 라우팅·인증 |
| **Feature Flag** | 배포와 별개로 기능 노출을 켜고 끄는 설정. | 점진적 공개 |
| **A/B Testing** | 실험군을 나누어 서로 다른 경험의 효과를 비교. | CTA 문구 실험 |
| **Dependency Graph** | 모듈 간 의존 관계를 나타내는 그래프. | 번들 의존성 |
| **Tree Shaking** | 사용되지 않는 모듈 내보내기를 번들에서 제거하는 최적화. | ES module |
| **Code Splitting** | 번들을 필요한 단위로 분리해 로드. | 라우트별 청크 |
| **Module Federation** | 런타임에 별도 빌드된 모듈을 공유·연결하는 방식. | 원격 UI 모듈 |
| **ESM** | import/export 기반 ECMAScript 모듈 시스템. | import x from |
| **CommonJS** | require/module.exports 기반 Node.js 모듈 시스템. | require('x') |
| **Reconciliation** | 기존 UI와 새 결과를 비교해 필요한 변경을 적용하는 과정. | React 갱신 |
| **Virtual DOM** | UI를 메모리상의 구조로 표현해 변경 계산에 활용하는 모델. | React 요소 트리 |
| **Declarative UI** | 원하는 화면 상태를 기술하고 변경 적용을 런타임에 맡기는 방식. | 상태→화면 |
| **Imperative UI** | DOM 조작 등 화면 변경 절차를 직접 명령하는 방식. | element.append |
| **Architecture Decision Record** | 설계 결정의 배경·대안·결과를 기록한 문서. | ADR-001 |

## 참고 자료

전체 참고 링크와 영역별 자료는 [REFERENCES.md](../REFERENCES.md)에 정리했습니다.
