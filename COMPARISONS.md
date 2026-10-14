# 헷갈리는 프론트엔드 용어 비교

[← README](README.md)

| 비교 | 차이 | 선택 기준 |
| --- | --- | --- |
| **Debounce vs Throttle** | Debounce는 연속 입력이 멈춘 후 실행, Throttle은 일정 주기로 실행을 제한 | 검색 입력 vs 스크롤 처리 |
| **Throttle vs In-flight Guard** | Throttle은 빈도 제한, Guard는 진행 중인 작업의 재실행 차단 | 스크롤 이벤트 vs 저장·결제 버튼 |
| **중복 클릭 방지 vs Idempotency** | UI 차단은 사용성 개선, 멱등성은 서버가 중복 효과를 막는 성질 | 금전 거래에서는 서버 멱등성 필수 |
| **Toast vs Snackbar** | 둘 다 짧은 피드백; Snackbar는 액션이 포함되는 등 시스템별 구분이 다름 | 사용 중인 디자인 시스템 규칙 우선 |
| **Dialog vs Modal** | Dialog는 대화상자라는 UI 유형, Modal은 배경 상호작용을 차단하는 동작 방식 | 비모달 Dialog도 존재 |
| **Tooltip vs Popover** | Tooltip은 짧은 도움말, Popover는 상호작용 가능한 복합 내용도 포함 | 설명 한 줄 vs 메뉴·폼 패널 |
| **Select vs Combobox** | Select는 목록 값 선택 중심, Combobox는 입력과 후보 목록의 결합 | 자유 입력·검색 필요 여부 |
| **Checkbox vs Radio vs Switch** | 다중 독립 선택 vs 단일 선택 vs 즉시 on/off | 선택 개수와 변경의 즉시성 |
| **Padding vs Margin vs Gap** | 내부 여백 vs 외부 여백 vs 레이아웃 아이템 간 간격 | 간격 책임에 따라 선택 |
| **Flexbox vs Grid** | 기본적으로 1차원 정렬 vs 2차원 격자 | 줄 단위 배치 vs 행·열 동시 제어 |
| **Hover vs Focus vs Active** | 포인터 위치 vs 키보드·입력 대상 vs 누르고 있는 순간 | 입력 장치와 접근성 모두 고려 |
| **Responsive vs Adaptive** | 조건에 유연히 적응 vs 정의된 레이아웃 간 전환 | 유동형 레이아웃과 단계형 레이아웃 |
| **CSR vs SSR vs SSG** | 브라우저에서 렌더링 vs 서버 요청 시 HTML 생성 vs 빌드 시 HTML 생성 | 인터랙션·SEO·데이터 갱신 주기 |
| **Preload vs Prefetch** | 현재 페이지의 중요 자원 선행 요청 vs 다음 탐색용 자원 예상 요청 | 즉시 필요한가, 미래에 필요한가 |
| **Unit vs Integration vs E2E** | 작은 로직 vs 결합된 구성요소 vs 전체 사용자 흐름 | 실패 위치·검증 범위 |
| **Cookie vs LocalStorage vs SessionStorage** | 요청에 실릴 수 있는 쿠키 vs 지속 출처 스토리지 vs 탭 세션 스토리지 | 보안·수명·서버 전송 필요 여부 |

**주의:** 통용되는 명칭은 디자인 시스템·프레임워크마다 다를 수 있습니다. 반드시 현재 프로젝트의 정의와 문맥을 확인하세요.
