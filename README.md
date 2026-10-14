<div align="center">

# 📚 Frontend Glossary

**프론트엔드 개발과 UI/UX 협업에 필요한 용어를 한국어로 찾아보는 오픈 용어집**

UI 컴포넌트 · 디자인/CSS · 인터랙션 · 데이터 · 브라우저 · 아키텍처 · 성능 · 품질

[📖 분야별 용어](#분야별-용어) · [🔤 A–Z 색인](INDEX.md) · [🔗 참고 자료](REFERENCES.md) · [🤝 기여하기](CONTRIBUTING.md)

</div>

## 소개

`Navbar`, `Toast`, `Hero`, `Hover`, `Border Radius`, `Bottom Sheet`부터 `Debounce`, `Throttle`, `SSR`, `LCP`까지 **393개 용어**를 8개 대분류로 정리했습니다. 한 줄 정의와 짧은 실무 예시를 곁들였습니다.

이 저장소는 **입문자를 위한 빠른 찾아보기 자료**이지 특정 프레임워크의 공식 명세를 대체하지 않습니다. 같은 명칭도 디자인 시스템·플랫폼에 따라 용법이 다를 수 있습니다. 정확한 구현 판단은 [원문 레퍼런스](REFERENCES.md)를 함께 확인하세요.

## 분야별 용어

| 분류 | 내용 | 용어 수 |
| --- | --- | ---: |
| [1. UI/UX · 화면과 컴포넌트](glossary/01-ui-ux.md) | 화면 구조, 내비게이션, UI 구성요소, UX 패턴 | 62 |
| [2. 디자인·CSS · 외형과 배치](glossary/02-design-css.md) | 스타일, 박스 모델, 레이아웃, 반응형, 토큰 | 54 |
| [3. 인터랙션 · 행동과 반응](glossary/03-interaction.md) | 입력·제스처, 상태, 이벤트 제어, 모션 | 45 |
| [4. 상태·데이터 · 흐름과 동시성](glossary/04-state-data.md) | 상태 관리, 비동기, 캐시, 중복 요청, 동시성 | 45 |
| [5. 웹·브라우저 · 플랫폼 기본기](glossary/05-web-browser.md) | HTML, JS, DOM, 브라우저 API, 네트워크 | 48 |
| [6. 아키텍처 · 설계와 렌더링](glossary/06-architecture.md) | 컴포넌트, 렌더링 전략, 구조와 패턴 | 45 |
| [7. 성능·최적화 · 체감 속도](glossary/07-performance.md) | 로딩, 브라우저 렌더링, 웹 성능 지표 | 44 |
| [8. 품질·개발 · 접근성·보안·도구](glossary/08-quality-tooling.md) | 접근성, SEO, 테스트, 보안, 빌드 도구 | 50 |
| **합계** | | **393** |

## 자주 찾는 개념

| 질문 | 읽어볼 용어 | 분류 |
| --- | --- | --- |
| 화면 아래에서 올라오는 선택 UI 이름은? | Bottom Sheet, Modal, Drawer | [UI/UX](glossary/01-ui-ux.md) |
| 저장 성공 후 잠깐 뜨는 알림은? | Toast, Snackbar, Alert | [UI/UX](glossary/01-ui-ux.md) |
| 버튼 모서리를 둥글게 만드는 값은? | Border Radius, Design Token | [디자인·CSS](glossary/02-design-css.md) |
| 클릭 연타·검색 입력을 제어하려면? | Debounce, Throttle, Cooldown | [인터랙션](glossary/03-interaction.md) |
| 결제 중복 호출을 안전하게 막으려면? | Double-submit Guard, Idempotency, Single-flight | [인터랙션](glossary/03-interaction.md) · [상태·데이터](glossary/04-state-data.md) |
| 서버와 클라이언트 렌더링 차이는? | CSR, SSR, SSG, Hydration | [아키텍처](glossary/06-architecture.md) |
| 화면이 느릴 때 보는 지표는? | LCP, INP, CLS, TTFB | [성능](glossary/07-performance.md) |

## 혼동하기 쉬운 용어

- **Toast vs. Snackbar**: 제품/디자인 시스템에 따라 사실상 비슷한 알림을 가리키기도 합니다. 이름만으로 구현 동작을 단정하지 마세요.
- **Modal vs. Dialog**: Modal은 다른 작업을 막는 상호작용 방식, Dialog는 대화 상자 유형입니다. Dialog는 모달일 수도 비모달일 수도 있습니다.
- **Hover vs. Focus**: 포인터가 올라온 상태와 키보드 등 입력 대상이 된 상태는 다릅니다. 터치에서는 hover를 전제로 설계하면 안 됩니다.
- **Debounce vs. Throttle**: 이벤트 종료 후 실행을 미루는 것과 일정 구간 내 실행 횟수를 제한하는 것은 다릅니다. [비교 가이드](guides/common-confusions.md)
- **Throttle/Disable vs. Idempotency**: UI에서 연타를 제한하는 것만으로 주문·결제 중복 처리는 보장되지 않습니다.

## 용어 찾기와 기여하기

- [A–Z 전체 색인](INDEX.md)에서 영문 명칭으로 빠르게 검색하세요. GitHub의 **파일 내 찾기**(`⌘F` / `Ctrl+F`)도 편리합니다.
- [자주 혼동하는 개념](guides/common-confusions.md)은 비교·선택 기준 위주로 설명합니다.
- [참고 자료 모음](REFERENCES.md)에 공식 문서·디자인 시스템·전문 아티클 링크가 있습니다.
- 추가·수정은 [CONTRIBUTING.md](CONTRIBUTING.md)를 따르세요. [Issues](https://github.com/WhiteKiwi/frontend-glossary/issues)와 Pull Request를 환영합니다.

## 작성 원칙

**영문 용어 우선 · 짧고 정확한 한국어 설명 · 실무 예시 · 원문 근거**. 모호한 개념은 억지로 하나의 정답으로 고정하지 않으며 관련 개념을 교차 연결합니다. 분류는 탐색을 위한 대표 위치일 뿐, 개념 간 경계는 겹칠 수 있습니다.

## 라이선스

문서와 설명은 [CC BY 4.0](LICENSE)으로 제공합니다. 링크로 소개한 제3자 문서는 각 출처의 저작권과 라이선스가 적용됩니다.
