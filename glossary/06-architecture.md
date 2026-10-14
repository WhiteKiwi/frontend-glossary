# 아키텍처

> 애플리케이션 구성·렌더링·컴포넌트 설계

[← 전체 목차](../README.md) · [알파벳 색인](../INDEX.md)

| 용어 | 설명 | 예시·주의점 |
| --- | --- | --- |
| **Component** | UI를 재사용 가능한 단위로 분리한 구성 요소 | ProductCard. |
| **Component Composition** | 작은 컴포넌트를 조합해 기능을 구축 | Card 안에 Button 구성. |
| **Separation of Concerns** | 관심사를 책임별로 분리하는 설계 원칙 | 데이터 요청과 표시 분리. |
| **Single Responsibility** | 모듈이 변경될 이유를 명확하게 한정하는 원칙 | 입력 검증 분리. |
| **Custom Hook** | 반복되는 React 상태·부수효과 로직을 묶은 함수 | useDebouncedValue. |
| **Higher-Order Component** | 컴포넌트를 입력받아 확장된 컴포넌트를 반환 | 접근 제어 래퍼. |
| **Render Props** | 함수 형태의 prop으로 렌더링 제어를 위임 | 데이터를 자식 렌더 함수에 전달. |
| **Compound Component** | 서로 협력하는 하위 컴포넌트로 API를 구성 | Tabs.List, Tabs.Trigger. |
| **Headless UI** | 외형 없이 행동·접근성 로직을 제공하는 UI 방식 | 디자인 자유도가 높은 Select. |
| **Atomic Design** | UI를 작은 원자부터 조립해 분류하는 사고틀 | atoms→molecules→organisms. |
| **Design System** | UI 규칙·컴포넌트·토큰을 공동 관리하는 체계 | 팀 공통 버튼. |
| **SPA (Single-Page Application)** | 페이지 전체 재로드 없이 화면을 전환하는 애플리케이션 | 클라이언트 라우터. |
| **MPA (Multi-Page Application)** | 여러 HTML 문서를 페이지 이동으로 구성 | 전통적 서버 렌더링 사이트. |
| **CSR (Client-Side Rendering)** | 주로 브라우저에서 UI를 렌더링 | 클라이언트 JS로 화면 구성. |
| **SSR (Server-Side Rendering)** | 요청 시 서버에서 HTML을 생성 | 서버가 초기 화면 출력. |
| **SSG (Static Site Generation)** | 빌드 시점에 HTML을 미리 생성 | 문서 사이트. |
| **ISR (Incremental Static Regeneration)** | 정적 페이지를 일정 조건 아래 재생성하는 전략 | 프레임워크별 동작 차이. |
| **Hydration** | 서버가 출력한 HTML에 클라이언트 상호작용을 연결하는 과정 | React hydrate. |
| **Streaming SSR** | HTML을 한 번에 보내지 않고 준비되는 대로 스트리밍 | Suspense 경계별 전송. |
| **React Server Components** | 서버에서 실행되어 클라이언트 번들과 분리되는 React 컴포넌트 모델 | 서버 데이터 접근 컴포넌트. |
| **Islands Architecture** | 정적 HTML의 필요한 일부 영역만 대화형으로 활성화하는 구조 | 부분 하이드레이션. |
| **Routing** | URL을 화면·리소스 처리기로 연결하는 체계 | /products/:id. |
| **Nested Routing** | 라우트를 계층적으로 정의해 공통 레이아웃을 공유 | 설정 하위 페이지. |
| **Micro Frontends** | 큰 프론트엔드를 독립 배포 가능한 작은 단위로 분리 | 도메인별 앱. |
| **Monorepo** | 여러 패키지·프로젝트를 한 저장소에서 관리 | apps/와 packages/. |
| **Feature-Sliced Design** | 기능과 계층 관점으로 프론트 코드를 조직하는 방법론 | features, entities, shared. |
| **Dependency Injection** | 의존성을 내부 생성 대신 외부에서 제공하는 방식 | API 클라이언트 주입. |
| **Error Boundary** | 하위 컴포넌트의 렌더링 오류를 포착해 대체 UI 표시 | React 에러 경계. |
| **Suspense** | 비동기 준비 중인 하위 UI의 대체 표시를 선언하는 React 메커니즘 | fallback skeleton. |
| **Portal** | 컴포넌트의 논리적 부모를 유지하며 DOM 다른 위치에 렌더링 | 모달 레이어. |
| **Reconciliation** | React가 변경된 UI 트리를 비교·갱신하는 과정 | key의 중요성. |

---

관련 참고 문헌은 [REFERENCES.md](../REFERENCES.md)에서 확인할 수 있습니다.
