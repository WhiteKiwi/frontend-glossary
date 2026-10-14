# Frontend Glossary

> **프론트엔드 개발 용어를 한국어로 찾아보는 오픈 용어집**  
> UI 패턴부터 CSS, 이벤트 제어, 상태·데이터, 브라우저, 아키텍처, 성능, 품질까지.

[![Glossary](https://img.shields.io/badge/terms-335-2563eb)](INDEX.md) [![Language](https://img.shields.io/badge/language-%ED%95%9C%EA%B5%AD%EC%96%B4-0f766e)](README.md) [![Contributions](https://img.shields.io/badge/PRs-welcome-brightgreen)](CONTRIBUTING.md)

프론트엔드를 만들다 보면 **Navbar·Toast·Hero·Bottom Sheet·Radius·Hover·Debounce·Throttle** 같은 용어를 자주 접합니다. 이 저장소는 이름이 헷갈리거나 구현 시점에 다시 찾아봐야 하는 개념을 **짧은 정의 + 실무 예시·주의점**으로 정리합니다.

## 빠른 탐색

| 영역 | 무엇을 찾을 때? | 바로가기 |
| --- | --- | --- |
| 🧩 UI/UX | 화면의 구성 요소·명칭·사용자 흐름 | [UI/UX](glossary/01-ui-ux.md) |
| 🎨 디자인·CSS | 색상·간격·반응형·배치 규칙 | [디자인·CSS](glossary/02-design-css.md) |
| 👆 인터랙션 | 클릭·제스처·상태·애니메이션·따닥 방지 | [인터랙션](glossary/03-interaction.md) |
| 🔄 상태·데이터 | 비동기 요청·캐시·중복 실행·상태 관리 | [상태·데이터](glossary/04-state-data.md) |
| 🌐 웹·브라우저 | DOM·이벤트 루프·HTTP·스토리지 | [웹·브라우저](glossary/05-web-browser.md) |
| 🏗️ 아키텍처 | 컴포넌트 구조·CSR·SSR·Hydration | [아키텍처](glossary/06-architecture.md) |
| ⚡ 성능·최적화 | Web Vitals·지연 로딩·번들 최적화 | [성능·최적화](glossary/07-performance.md) |
| ✅ 품질·개발 도구 | 접근성·SEO·테스트·보안·빌드 | [품질·개발 도구](glossary/08-quality-tooling.md) |

**전체 335개 항목** · [A–Z 용어 색인](INDEX.md) · [헷갈리는 용어 비교](COMPARISONS.md) · [실전 패턴](RECIPES.md) · [참고 자료](REFERENCES.md)

## 자주 찾는 용어

| 용어 | 한 줄 설명 | 자세히 |
| --- | --- | --- |
| Navbar | 주요 화면을 이동하는 내비게이션 막대 | [UI/UX](glossary/01-ui-ux.md) |
| Hero | 랜딩 페이지 상단의 핵심 메시지 영역 | [UI/UX](glossary/01-ui-ux.md) |
| Toast | 잠시 나타났다 사라지는 비차단 알림 | [UI/UX](glossary/01-ui-ux.md) |
| Bottom Sheet | 화면 아래에서 올라오는 패널 | [UI/UX](glossary/01-ui-ux.md) |
| Border Radius | 모서리의 둥근 정도 | [디자인·CSS](glossary/02-design-css.md) |
| Hover | 포인터가 요소 위에 있는 상태 | [인터랙션](glossary/03-interaction.md) |
| Debounce | 연속 호출 후 조용해졌을 때 실행 | [인터랙션](glossary/03-interaction.md) |
| Throttle | 반복 이벤트 실행 빈도를 제한 | [인터랙션](glossary/03-interaction.md) |
| Idempotency | 동일 작업 재시도에도 효과 중복 방지 | [인터랙션](glossary/03-interaction.md) |
| Hydration | 서버 HTML에 클라이언트 상호작용 연결 | [아키텍처](glossary/06-architecture.md) |

## 사용 방법

1. **화면의 이름이 궁금하다면** UI/UX부터 살펴보세요.
2. **구현 방법을 찾는다면** 인터랙션·상태·데이터와 [실전 패턴](RECIPES.md)을 함께 보세요.
3. **비슷한 용어가 헷갈린다면** [헷갈리는 용어 비교](COMPARISONS.md)를 확인하세요.
4. **공식 정의와 상세 가이드가 필요하다면** [참고 자료](REFERENCES.md)로 이동하세요.

> **분류 원칙:** 개념당 대표 분야 하나를 정하되 관련 분야에도 등장할 수 있습니다. 예를 들어 Debounce는 인터랙션과 성능 두 관점에서 중요합니다. 같은 단어가 다른 맥락에서 쓰일 때는 차이를 설명합니다.

## 기여하기

오탈자, 부정확한 정의, 새로운 용어, 실제 사용 예시, 공식 문서 링크 모두 환영합니다. [CONTRIBUTING.md](CONTRIBUTING.md)의 작성 형식을 참고해 PR을 보내주세요.

이 용어집은 **학습·참고용**입니다. 브라우저·프레임워크 버전에 따라 정확한 동작은 달라질 수 있으므로, 중요한 구현은 연결된 공식 문서를 우선 확인해주세요.
