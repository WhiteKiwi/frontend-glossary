# 웹·브라우저 · 플랫폼 기본기

> [전체 목차](../README.md) · [알파벳 색인](../INDEX.md) · [참고 자료](../REFERENCES.md)

이 문서의 용어는 이해하기 쉬운 요약 정의입니다. 구체적인 동작은 공식 명세·디자인 시스템에 따라 달라질 수 있습니다.

| 용어 | 설명 | 예시·활용 |
| --- | --- | --- |
| **HTML** | 웹 문서의 구조와 의미를 표현하는 마크업 언어. | <main> |
| **Semantic HTML** | 요소의 본래 의미에 맞는 HTML 사용. | <nav>·<button> |
| **DOM** | 문서 요소를 객체 트리로 표현한 인터페이스. | document.querySelector |
| **CSSOM** | 파싱된 CSS 규칙을 객체 모델로 표현. | 스타일 규칙 |
| **Render Tree** | 화면에 필요한 DOM·스타일 정보를 바탕으로 구성되는 렌더링 구조. | 레이아웃 계산 |
| **JavaScript** | 웹에서 동적 동작을 구현하는 프로그래밍 언어. | 이벤트 핸들러 |
| **TypeScript** | JavaScript에 정적 타입 검사를 더한 언어. | interface User |
| **Event Loop** | 작업·이벤트 처리의 실행 순서를 조율하는 런타임 모델. | 비동기 콜백 |
| **Call Stack** | 현재 실행 중인 함수 호출의 스택. | 함수 중첩 호출 |
| **Task Queue** | 실행을 기다리는 작업을 관리하는 큐. | setTimeout 콜백 |
| **Microtask** | 현재 작업 이후 우선 처리되는 큐의 작업. | Promise.then |
| **Promise** | 비동기 작업의 미래 완료·실패를 표현하는 객체. | fetch().then |
| **async/await** | Promise 기반 비동기를 순차 코드처럼 작성하는 문법. | await fetch() |
| **Closure** | 함수가 생성 당시의 외부 변수 환경을 참조하는 특성. | 카운터 함수 |
| **Callback** | 다른 함수에 전달되어 나중에 호출되는 함수. | onClick |
| **Hoisting** | 선언이 실행 전 환경에 등록되어 참조 방식에 영향을 주는 동작. | var·function 선언 |
| **Scope** | 식별자 접근 가능 범위. | 블록 스코프 |
| **Garbage Collection** | 도달할 수 없는 메모리를 회수하는 자동 관리. | 객체 참조 해제 |
| **HTTP** | 클라이언트와 서버 사이의 요청·응답 프로토콜. | GET /products |
| **HTTPS** | TLS로 보호되는 HTTP 통신. | https:// |
| **Request** | 클라이언트가 서버로 보내는 요청. | POST /orders |
| **Response** | 서버가 요청에 반환하는 응답. | 200 OK |
| **HTTP Method** | 요청 의도를 나타내는 메서드. | GET·POST·PUT·PATCH·DELETE |
| **Status Code** | HTTP 응답 결과 분류 코드. | 200·404·500 |
| **REST** | 자원을 중심으로 HTTP 인터페이스를 설계하는 아키텍처 스타일. | /users/42 |
| **GraphQL** | 클라이언트가 필요한 데이터 형태를 질의하는 API 언어/실행 체계. | query User |
| **Fetch API** | 네트워크 요청을 수행하는 웹 API. | fetch('/api') |
| **CORS** | 브라우저의 교차 출처 리소스 접근 허용을 통제하는 메커니즘. | Access-Control-Allow-Origin |
| **Same-origin Policy** | 기본적으로 서로 다른 출처 간 스크립트 접근을 제한하는 보안 정책. | 프로토콜·호스트·포트 비교 |
| **Cookie** | 서버·브라우저가 주고받고 저장하는 작은 상태 정보. | 세션 쿠키 |
| **Local Storage** | 같은 출처에서 지속 보관하는 키·값 저장소. | 테마 설정 |
| **Session Storage** | 탭의 페이지 세션 범위로 저장하는 키·값 저장소. | 임시 폼 상태 |
| **IndexedDB** | 브라우저의 구조화된 비동기 로컬 데이터베이스. | 오프라인 캐시 |
| **Service Worker** | 페이지와 별개로 실행되며 요청·푸시 등을 처리할 수 있는 워커. | 오프라인 앱 |
| **Web Worker** | 메인 UI 스레드와 분리된 스크립트 실행 환경. | 무거운 계산 |
| **Web API** | 브라우저가 제공하는 플랫폼 기능 인터페이스. | IntersectionObserver |
| **Intersection Observer** | 대상이 뷰포트·조상과 교차하는 정도를 관찰하는 API. | 지연 로딩 |
| **Resize Observer** | 요소 크기 변화를 관찰하는 API. | 반응형 차트 |
| **Mutation Observer** | DOM 변경을 관찰하는 API. | 외부 위젯 변화 감지 |
| **History API** | 브라우저 세션 기록을 제어하는 인터페이스. | pushState |
| **URL** | 인터넷 자원의 주소 식별 표현. | https://example.com/path |
| **Query String** | URL의 ? 뒤에 붙는 매개변수 문자열. | ?page=2 |
| **Fragment** | URL에서 # 뒤에 붙는 문서 내 참조. | #installation |
| **DNS** | 도메인 이름을 IP 주소 등에 연결하는 시스템. | example.com 조회 |
| **TLS** | 전송 구간 암호화·인증을 제공하는 프로토콜. | HTTPS 연결 |
| **CDN** | 여러 지역에서 리소스를 가까이 전달하는 콘텐츠 배포망. | 정적 이미지 전송 |
| **Web Storage** | localStorage·sessionStorage 저장 인터페이스 집합. | 사용자 설정 |
| **Content Security Policy** | 허용된 리소스 출처·동작을 제한하는 브라우저 보안 정책. | script-src |

## 참고 자료

전체 참고 링크와 영역별 자료는 [REFERENCES.md](../REFERENCES.md)에 정리했습니다.
