# 상태·데이터 · 흐름과 동시성

> [전체 목차](../README.md) · [알파벳 색인](../INDEX.md) · [참고 자료](../REFERENCES.md)

이 문서의 용어는 이해하기 쉬운 요약 정의입니다. 구체적인 동작은 공식 명세·디자인 시스템에 따라 달라질 수 있습니다.

| 용어 | 설명 | 예시·활용 |
| --- | --- | --- |
| **State** | UI나 애플리케이션의 현재 값을 나타내는 데이터. | isOpen |
| **Props** | 상위 컴포넌트가 하위에 전달하는 입력 값. | title prop |
| **Local State** | 한 컴포넌트 주변에서 관리하는 상태. | 모달 열림 여부 |
| **Global State** | 여러 영역이 공유하는 애플리케이션 상태. | 인증 사용자 |
| **Server State** | 서버가 소유하며 클라이언트가 조회·동기화하는 데이터. | 상품 목록 |
| **Derived State** | 기존 데이터에서 계산해 얻는 상태. | 필터링한 목록 |
| **State Machine** | 가능한 상태와 전이 규칙을 명시한 모델. | idle→loading→success |
| **Reducer** | 이전 상태와 액션을 받아 다음 상태를 계산하는 함수. | useReducer |
| **Controlled Component** | 입력의 현재 값을 외부 상태로 제어하는 컴포넌트. | value + onChange |
| **Uncontrolled Component** | DOM 등 내부에 입력 값을 보관하는 컴포넌트. | ref로 읽는 input |
| **Single Source of Truth** | 동일 사실의 기준 데이터를 한 곳으로 정하는 원칙. | 중복 상태 제거 |
| **Prop Drilling** | 중간 계층을 거쳐 props를 연속 전달하는 현상. | 깊은 트리 전달 |
| **Context** | 하위 트리에서 값을 공유하는 React 등의 메커니즘. | Theme Context |
| **Store** | 상태와 변경 동작을 모아 제공하는 저장소. | Redux store |
| **Immutable Update** | 기존 값 직접 변경 대신 새 값을 만들어 상태 갱신. | 배열 복사 후 교체 |
| **Optimistic Update** | 요청 성공 전에 성공을 가정하고 화면부터 갱신. | 좋아요 즉시 반영 |
| **Rollback** | 예측 반영이 실패하면 이전 상태로 되돌림. | 좋아요 취소 |
| **Pessimistic Update** | 서버 응답 후에만 화면을 갱신. | 승인 후 결과 표시 |
| **Cache** | 반복 접근 비용을 줄이기 위해 결과를 보관하는 저장. | API 결과 캐시 |
| **Cache Invalidation** | 캐시가 더 이상 유효하지 않음을 판정·무효화. | 상품 수정 후 갱신 |
| **Stale Data** | 최신 원본보다 오래된 데이터. | 이전 검색 결과 |
| **Stale-While-Revalidate** | 캐시 값을 먼저 제공하고 백그라운드에서 최신 데이터를 다시 조회. | 목록 즉시 표시 |
| **TTL** | Time to Live; 캐시 항목 등의 유효 시간. | 캐시 5분 |
| **Polling** | 일정 주기로 데이터를 반복 조회. | 작업 상태 확인 |
| **Long Polling** | 서버가 새 이벤트까지 HTTP 응답을 대기시키는 통신. | 메시지 알림 |
| **SSE** | 서버에서 클라이언트로 이벤트를 지속 전송하는 방식. | 실시간 진행률 |
| **WebSocket** | 연결 하나로 양방향 메시지를 지속 송수신하는 프로토콜. | 채팅 |
| **Request Deduplication** | 동일·동등 요청의 불필요한 중복 수행을 줄이는 기술. | 중복 조회 병합 |
| **Single-flight** | 동일 키의 진행 중 작업을 하나로 공유하는 패턴. | 중복 토큰 갱신 |
| **Idempotency** | 동일 연산을 반복 적용해도 최종 효과가 같다는 성질. | 멱등 키를 이용한 주문 처리 |
| **Race Condition** | 비동기 작업 순서에 따라 결과가 잘못 달라지는 문제. | 옛 검색 결과가 덮어쓰기 |
| **AbortController** | 요청 등 취소 가능한 작업에 중단 신호를 전달하는 웹 API. | 검색 요청 취소 |
| **Retry** | 실패한 작업을 다시 시도하는 전략. | 일시적 네트워크 장애 |
| **Exponential Backoff** | 재시도 간 대기 시간을 지수적으로 늘리는 전략. | 1초→2초→4초 |
| **Jitter** | 동시 재시도 폭주를 막기 위해 대기 시간에 무작위 편차를 추가. | 백오프 분산 |
| **Rate Limiting** | 일정 구간의 허용 요청 수를 제한하는 정책. | 초당 API 요청 10회 |
| **Infinite Query** | 페이지 데이터를 이어 붙여 조회하는 데이터 패턴. | 무한 스크롤 목록 |
| **Cursor Pagination** | 마지막 조회 위치를 나타내는 커서로 다음 묶음을 조회. | nextCursor |
| **Offset Pagination** | 건너뛸 개수와 크기로 페이지를 조회. | offset=20&limit=10 |
| **Normalization** | 데이터를 정규화해 중복을 줄이고 참조를 일관되게 유지. | id별 엔터티 캐시 |
| **Serialization** | 데이터를 저장·전송 가능한 표현으로 변환. | 객체→JSON |
| **Deserialization** | 전송된 표현을 프로그램 데이터로 복원. | JSON→객체 |
| **Validation** | 입력이나 데이터가 제약을 만족하는지 검사. | 이메일 형식 검사 |
| **Hydration Mismatch** | 서버 HTML과 클라이언트 첫 렌더 결과가 달라 발생하는 문제. | 시간·랜덤 값 불일치 |
| **Error Boundary** | 렌더링 오류를 잡아 대체 UI를 제공하는 경계. | React fallback |

## 참고 자료

전체 참고 링크와 영역별 자료는 [REFERENCES.md](../REFERENCES.md)에 정리했습니다.
