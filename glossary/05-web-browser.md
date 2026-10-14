# 웹·브라우저

> 웹 플랫폼·JavaScript 런타임·네트워크·보안 모델

[← 전체 목차](../README.md) · [알파벳 색인](../INDEX.md)

| 용어 | 설명 | 예시·주의점 |
| --- | --- | --- |
| **HTML** | 웹 문서의 의미와 구조를 표현하는 마크업 언어 | h1, main, button. |
| **Semantic HTML** | 요소의 의미에 맞게 HTML을 사용하는 방식 | div 대신 nav. |
| **DOM** | HTML 문서를 객체 트리로 표현한 모델 | document.querySelector. |
| **CSSOM** | 브라우저가 CSS를 해석한 스타일 객체 모델 | 스타일 계산. |
| **Render Tree** | 표시 대상 요소와 계산된 스타일을 기반으로 구성되는 렌더링 구조 | 레이아웃 계산. |
| **JavaScript Engine** | JavaScript를 실행하는 엔진 | V8, JavaScriptCore. |
| **Event Loop** | 태스크·마이크로태스크 등의 실행을 조정하는 메커니즘 | 비동기 콜백 스케줄링. |
| **Task (Macrotask)** | 이벤트 루프의 일반 태스크 | setTimeout 콜백. |
| **Microtask** | 현재 실행이 끝난 뒤 우선 처리되는 작업 큐 | Promise.then. |
| **Closure** | 함수가 선언된 주변 렉시컬 환경을 참조하는 성질 | 상태를 기억하는 핸들러. |
| **Hoisting** | 선언이 스코프 처리 단계에서 바인딩되는 동작 | var와 let의 초기화 차이. |
| **Prototype** | JavaScript 객체 간 속성 상속을 형성하는 연결 | 프로토타입 체인. |
| **Module** | 기능을 파일 단위로 분리하고 내보내기·가져오기 | ESM import/export. |
| **HTTP** | 웹에서 요청과 응답을 주고받는 응용 계층 프로토콜 | GET /api. |
| **HTTPS** | TLS로 보호되는 HTTP 통신 | https:// 주소. |
| **DNS** | 도메인 이름을 IP 주소 등으로 해석하는 시스템 | example.com 조회. |
| **URL** | 리소스 위치를 나타내는 주소 | scheme://host/path. |
| **HTTP Method** | 요청의 의미를 나타내는 메서드 | GET, POST, PUT, PATCH, DELETE. |
| **HTTP Status Code** | 응답 처리 결과를 나타내는 숫자 코드 | 200, 404, 500. |
| **HTTP Header** | 요청·응답의 메타데이터 필드 | Authorization, Content-Type. |
| **Cookie** | 브라우저가 도메인 정책에 따라 저장·전송하는 작은 데이터 | 세션 식별자. |
| **Local Storage** | 출처별 문자열을 지속적으로 보관하는 웹 스토리지 | 로컬 설정. |
| **Session Storage** | 탭 단위 세션 동안 데이터를 보관하는 웹 스토리지 | 일시적 폼 상태. |
| **IndexedDB** | 브라우저의 구조화된 비동기 로컬 데이터베이스 | 오프라인 문서. |
| **Service Worker** | 페이지와 별개로 동작하며 네트워크·푸시 등에 관여하는 워커 | 오프라인 캐시. |
| **Web Worker** | 메인 스레드 바깥에서 스크립트를 실행하는 수단 | 무거운 계산 분리. |
| **CORS** | 교차 출처 요청에서 브라우저가 적용하는 서버 허용 정책 | Access-Control-Allow-Origin. |
| **Same-Origin Policy** | 서로 다른 출처 간 접근을 제한하는 브라우저 보안 원칙 | 타 도메인 DOM 접근 차단. |
| **CSP (Content Security Policy)** | 허용할 콘텐츠 출처 등을 선언해 공격을 완화하는 정책 | script-src. |
| **CSRF** | 사용자의 인증 상태를 이용해 의도하지 않은 요청을 보내는 공격 | 송금 폼 위조. |
| **XSS** | 공격자 스크립트가 신뢰 경계 내에서 실행되는 취약점 | 검증 없는 HTML 삽입. |
| **SameSite** | 쿠키의 교차 사이트 전송을 제어하는 속성 | Lax, Strict, None. |
| **TLS** | 전송 데이터의 기밀성·무결성 등을 제공하는 프로토콜 | HTTPS 보안 계층. |
| **Content Negotiation** | 클라이언트와 서버가 응답 표현을 협상하는 과정 | Accept: application/json. |

---

관련 참고 문헌은 [REFERENCES.md](../REFERENCES.md)에서 확인할 수 있습니다.
