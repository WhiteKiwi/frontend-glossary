# 상태·데이터

> 상태의 소유권·서버 통신·동시성·캐시

[← 전체 목차](../README.md) · [알파벳 색인](../INDEX.md)

| 용어 | 설명 | 예시·주의점 |
| --- | --- | --- |
| **State** | UI 표시나 동작에 영향을 주는 변경 가능한 값 | 열린 메뉴 여부. |
| **Props** | 부모에서 자식 컴포넌트로 전달하는 입력 값 | 제목·콜백. |
| **Local State** | 특정 컴포넌트 내부에 보관하는 상태 | 아코디언 열림. |
| **Global State** | 여러 화면·컴포넌트가 공유하는 상태 | 테마·계정 정보. |
| **Server State** | 서버가 원본을 소유하는 비동기 데이터 상태 | 상품 목록. |
| **Derived State** | 기존 상태로 계산 가능한 값 | 총액 = 단가×수량. |
| **State Management** | 상태 변경·공유·동기화를 설계하는 방식 | Reducer·외부 스토어. |
| **Controlled Component** | 입력값을 외부 상태가 제어하는 컴포넌트 | React value+onChange. |
| **Uncontrolled Component** | 입력값 등을 DOM 내부에 맡기는 컴포넌트 | defaultValue+ref. |
| **Reducer** | 현재 상태와 액션으로 다음 상태를 계산하는 함수 | 복잡한 폼 흐름. |
| **Context** | 컴포넌트 트리를 통해 값을 전달하는 메커니즘 | 테마 공유. |
| **Immutability** | 기존 객체를 직접 바꾸지 않고 새 값을 만드는 원칙 | 배열 복사 후 갱신. |
| **Promise** | 비동기 작업의 최종 완료 또는 실패를 표현하는 객체 | fetch 결과. |
| **async / await** | Promise 기반 비동기 로직을 순차식으로 표현하는 구문 | await fetch(). |
| **Callback** | 다른 함수에 전달되어 이후 실행되는 함수 | onClick 처리기. |
| **Fetch API** | HTTP 요청을 수행하는 웹 API | fetch('/api'). |
| **REST** | 리소스와 HTTP 의미 체계를 사용하는 API 스타일 | GET /products. |
| **GraphQL** | 클라이언트가 필요한 데이터 구조를 질의하는 API 방식 | 상품과 리뷰를 요청. |
| **WebSocket** | 양방향 지속 연결 통신 프로토콜 | 실시간 채팅. |
| **SSE (Server-Sent Events)** | 서버에서 클라이언트로 이벤트를 스트리밍하는 HTTP 기반 방식 | 알림 스트림. |
| **Polling** | 일정 간격으로 서버에 반복 조회 | 상태 5초마다 확인. |
| **Long Polling** | 서버가 결과를 기다렸다가 응답하면 다시 요청 | 실시간성 보완. |
| **Cache** | 반복 조회 비용을 줄이기 위해 결과를 저장 | 상품 목록 캐시. |
| **Cache Invalidation** | 오래된 캐시가 유효하지 않음을 판정·무효화 | 상품 수정 후 목록 갱신. |
| **Stale-While-Revalidate** | 오래된 캐시를 우선 보여주고 백그라운드 재검증 | 목록 즉시 표시. |
| **TTL (Time to Live)** | 캐시 데이터의 유효 시간 | 5분 TTL. |
| **Optimistic Update** | 요청 성공 전에 UI·캐시를 먼저 변경 | 좋아요 선반영 후 실패 시 롤백. |
| **Pessimistic Update** | 서버 성공 응답 후 UI를 갱신 | 계좌 이체 완료 후 반영. |
| **Rollback** | 실패 시 잠정 상태를 이전 값으로 복구 | 좋아요 취소. |
| **Mutation** | 서버 데이터의 변경 작업 | POST·PATCH·DELETE. |
| **Pagination** | 데이터를 여러 페이지로 나눠 요청 | page=2. |
| **Cursor Pagination** | 마지막 항목의 위치를 가리키는 커서로 다음 결과 조회 | nextCursor. |
| **Offset Pagination** | 건너뛸 개수로 페이지를 구분 | offset=20. |
| **Race Condition** | 동시 작업 순서로 결과가 의도와 달라지는 상황 | 검색 요청 응답 역전. |
| **Request Deduplication** | 동일 데이터 요청을 공유하거나 중복 제거 | 동시 API 요청 단일화. |
| **Idempotency Key** | 중복 요청을 같은 작업으로 식별하는 키 | 결제·주문 생성. |

---

관련 참고 문헌은 [REFERENCES.md](../REFERENCES.md)에서 확인할 수 있습니다.
