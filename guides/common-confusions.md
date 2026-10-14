# 헷갈리기 쉬운 프론트엔드 개념

> [README](../README.md) · [인터랙션 용어](../glossary/03-interaction.md) · [상태·데이터](../glossary/04-state-data.md)

## Debounce vs Throttle vs Cooldown

| 방식 | 기준 | 대표 사례 | 주의할 점 |
| --- | --- | --- | --- |
| Debounce | 마지막 이벤트 후 조용한 시간 | 검색창 자동완성 | 입력이 계속되면 실행이 계속 미뤄질 수 있음 |
| Throttle | 정해진 기간에 최대 실행 빈도 | 스크롤 위치 계산 | leading/trailing 설정에 따라 첫·마지막 이벤트 반영이 달라짐 |
| Cooldown | 동작 이후 일정 시간 잠금 | 인증번호 재전송 | 사용성·재시도 정책과 함께 설계 |

`leading`은 묶음의 시작에서 실행, `trailing`은 끝에서 실행한다는 뜻입니다. 라이브러리별 구현과 옵션을 꼭 확인하세요.

## 따닥(연속 클릭) 방지 ≠ 중복 거래 방지

사용자 경험을 위한 연타 차단과 데이터 무결성을 위한 중복 실행 방지는 층이 다릅니다.

1. UI에서 요청 진행 중 버튼을 비활성화하거나 in-flight 가드를 둡니다.
2. 중복된 같은 조회는 request deduplication 또는 single-flight로 합칠 수 있습니다.
3. 주문·결제 등 부작용이 있는 작업에는 **서버 측 멱등 키/중복 검증**을 구현합니다.
4. 실패·타임아웃·재시도에도 동일 작업이 중복 생성되지 않는지 테스트합니다.

## Modal vs Dialog vs Drawer vs Bottom Sheet

- **Dialog**는 입력·확인에 쓰이는 대화 상자 유형입니다.
- **Modal**은 배경과의 상호작용을 제한하는 표시/동작 방식입니다. Dialog가 모달일 수도 있습니다.
- **Drawer / Side Sheet**는 주로 화면 측면에서 펼쳐지는 패널입니다.
- **Bottom Sheet**는 화면 하단에서 펼쳐지는 패널입니다.

디자인 시스템마다 명칭과 실제 접근성 동작이 다를 수 있습니다.

## Hover vs Focus vs Active vs Selected

- **Hover:** 포인터가 요소 위에 있음.
- **Focus:** 키보드 입력 등의 대상이 됨.
- **Active (CSS :active):** 눌리는 등 활성화되는 순간.
- **Selected:** 목록·탭에서 선택된 값/항목의 상태.

터치에서도 작동해야 하므로 Hover만으로 중요한 기능을 노출하면 안 됩니다. 포커스 표시와 키보드 조작도 고려하세요.

## SSR vs SSG vs CSR vs Hydration

- **CSR**은 브라우저에서 주요 UI를 생성합니다.
- **SSR**은 요청 시 서버에서 HTML을 만듭니다.
- **SSG**는 빌드할 때 HTML을 미리 생성합니다.
- **Hydration**은 서버 HTML을 클라이언트의 상호작용 가능한 UI와 연결하는 과정입니다.

실제 앱에서는 라우트·컴포넌트별로 여러 전략을 섞을 수 있습니다.

## Toast vs Snackbar vs Alert

- **Toast/Snackbar**는 대체로 작업 완료 등을 간단하게 알리는 일시적 피드백입니다. 차이는 제품별 명명 규칙에 영향을 받습니다.
- **Alert**는 중요한 상태나 주의 사항 전달에 쓰이며 지속 표시되거나 즉각적인 주의를 요구할 수 있습니다.

필요한 건 이름보다 **노출 시간, 닫기 방법, 화면 차단 여부, 스크린리더 알림 방식**을 명확히 정의하는 일입니다.

## 참고

- [CSS-Tricks — Debouncing and Throttling](https://css-tricks.com/debouncing-throttling-explained-examples/)
- [Stripe — Idempotent requests](https://docs.stripe.com/api/idempotent_requests)
- [WAI — ARIA Authoring Practices](https://www.w3.org/WAI/ARIA/apg/patterns/)
