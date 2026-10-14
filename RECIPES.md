# 실전 패턴: 언제 어떤 용어를 적용할까?

[← README](README.md) · [인터랙션 용어](glossary/03-interaction.md)

## 1. 검색어 입력: Debounce + AbortController

- 매 키 입력마다 API를 호출하지 않고 입력이 일정 시간 멈춘 뒤 요청합니다.
- 이전 요청이 아직 끝나지 않았다면 취소하거나 요청 식별자를 비교해 오래된 응답을 무시합니다.
- 취소만으로 모든 경쟁 상태를 완전히 피할 수 있는 것은 아닙니다.

## 2. 스크롤 위치 추적: Throttle 또는 requestAnimationFrame

- 고빈도 이벤트를 그대로 무거운 계산에 연결하지 않습니다.
- 화면 갱신 관련 작업은 requestAnimationFrame을 고려하고, 부가 분석 이벤트는 Throttle을 검토합니다.
- 스크롤 중 가시성 감지는 IntersectionObserver도 대안입니다.

## 3. 저장·결제 버튼의 따닥 방지: In-flight Guard + 서버 멱등성

1. 첫 클릭 시 즉시 작업 중 상태로 전환합니다.
2. 요청 진행 중 같은 행동을 반복 실행하지 않도록 막습니다.
3. 서버는 동일한 작업 식별자(Idempotency Key)를 재사용한 중복 요청의 효과를 중복 적용하지 않아야 합니다.
4. 성공·실패·재시도 상태와 접근성 메시지를 제공합니다.

> **주의:** 단순 Throttle/Debounce만으로는 네트워크 재시도, 여러 탭, 서로 다른 기기에서 발생한 중복 결제를 보장할 수 없습니다.

## 4. 목록 성능: Pagination + Virtualization + Lazy Loading

- 서버가 내려주는 데이터 양은 페이지나 커서로 제한합니다.
- DOM 항목이 매우 많다면 화면에 보이는 항목만 렌더링합니다.
- 이미지 등 화면 밖 자원은 필요해질 때 로드합니다.

## 5. 모달 접근성: Dialog + Focus Management

- 모달 다이얼로그는 열린 동안 포커스 이동 범위를 관리하고 Escape·닫기 버튼을 제공합니다.
- 닫으면 가능하면 원래 트리거로 포커스를 돌립니다.
- 적절한 역할·이름과 배경 상호작용 차단을 함께 점검합니다.

## 더 읽기

- [CSS-Tricks: Debounce & Throttle](https://css-tricks.com/debouncing-throttling-explained-examples/)
- [MDN: AbortController](https://developer.mozilla.org/en-US/docs/Web/API/AbortController)
- [Stripe: Idempotent requests](https://docs.stripe.com/api/idempotent_requests)
- [WAI-ARIA Dialog Pattern](https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/)
