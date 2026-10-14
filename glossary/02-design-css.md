# 디자인·CSS · 외형과 배치

> [전체 목차](../README.md) · [알파벳 색인](../INDEX.md) · [참고 자료](../REFERENCES.md)

이 문서의 용어는 이해하기 쉬운 요약 정의입니다. 구체적인 동작은 공식 명세·디자인 시스템에 따라 달라질 수 있습니다.

| 용어 | 설명 | 예시·활용 |
| --- | --- | --- |
| **Box Model** | 요소 크기를 content·padding·border·margin으로 설명하는 CSS 모델. | 레이아웃 크기 계산 |
| **Content Box** | 패딩·보더를 제외한 콘텐츠 영역. | box-sizing: content-box |
| **Border Box** | 보더까지 지정 크기에 포함하는 박스 계산 방식. | box-sizing: border-box |
| **Margin** | 요소 경계 바깥의 간격. | margin-top |
| **Padding** | 요소 경계 안쪽의 간격. | padding-inline |
| **Gap** | Flex/Grid 자식 사이의 간격. | gap: 16px |
| **Border** | 요소 테두리. | border: 1px solid |
| **Border Radius** | 요소 모서리를 둥글게 만드는 속성. | border-radius: 8px |
| **Shadow** | 요소에 그림자 효과를 주는 표현. | box-shadow |
| **Elevation** | 요소의 시각적 높낮이·깊이 체계. | 카드 그림자 단계 |
| **Opacity** | 요소의 불투명도. | opacity: .5 |
| **Typography** | 글꼴·크기·줄 간격 등 텍스트 시각 체계. | 본문 16px/24px |
| **Line Height** | 텍스트 줄 상자의 높이. | line-height: 1.5 |
| **Letter Spacing** | 문자 사이의 간격. | letter-spacing |
| **Font Weight** | 글꼴 획 두께. | font-weight: 600 |
| **Color Palette** | UI에 쓰이는 색상 집합. | 브랜드·중립색 |
| **Contrast** | 요소 간 밝기·색 차이. | 텍스트 대비 |
| **Design Token** | 색·여백·반경 같은 디자인 값을 이름 붙여 재사용하는 변수. | --color-primary |
| **Spacing Scale** | 일관된 간격 크기 단계. | 4·8·12·16 |
| **Flexbox** | 한 방향의 요소 배치·정렬에 강한 CSS 레이아웃. | display: flex |
| **Grid** | 행과 열을 동시에 다루는 CSS 레이아웃. | display: grid |
| **Inline** | 문장 흐름 안에서 배치되는 표시 방식. | display: inline |
| **Block** | 새 줄을 차지하는 블록 배치 방식. | display: block |
| **Inline-block** | 문장 흐름을 유지하며 너비·높이를 지정할 수 있는 표시 방식. | display: inline-block |
| **Position Relative** | 자기 정상 위치를 기준으로 오프셋하는 배치. | position: relative |
| **Position Absolute** | 위치 기준이 되는 조상을 따라 배치하며 일반 흐름에서 제외. | position: absolute |
| **Position Fixed** | 대개 뷰포트를 기준으로 고정하는 배치. | 고정 액션 버튼 |
| **Position Sticky** | 스크롤 구간에서 임계 위치에 붙는 배치. | sticky header |
| **Z-index** | 같은 스태킹 문맥에서 겹침 순서를 정하는 값. | z-index: 10 |
| **Stacking Context** | z-index 우선순위가 독립적으로 계산되는 겹침 그룹. | transform이 만든 문맥 |
| **Overflow** | 요소 경계를 넘친 콘텐츠 처리 방식. | hidden·auto·scroll |
| **Viewport** | 웹 콘텐츠가 표시되는 가시 영역. | 모바일 화면 크기 |
| **Breakpoint** | 레이아웃이 바뀌는 반응형 기준 폭. | 768px 전후 |
| **Media Query** | 화면·사용자 환경 조건에 따라 CSS를 적용. | @media |
| **Container Query** | 상위 컨테이너 크기·스타일 기준으로 조건부 스타일 적용. | @container |
| **Responsive Design** | 화면 조건에 유동적으로 대응하는 설계. | 모바일·데스크톱 적응 |
| **Adaptive Design** | 정해진 몇 개 레이아웃을 조건에 따라 선택하는 설계. | 모바일 전용 시안 |
| **Aspect Ratio** | 가로·세로 비율. | aspect-ratio: 16 / 9 |
| **Specificity** | 경합하는 CSS 선택자의 우선순위를 결정하는 규칙. | #id와 .class 비교 |
| **Cascade** | 출처·중요도·계층·우선순위·선언 순서 등에 따라 스타일을 결정하는 체계. | CSS 충돌 |
| **Inheritance** | 일부 CSS 속성이 부모에서 자식으로 전달되는 동작. | color 상속 |
| **Pseudo-class** | 요소 상태·구조를 선택하는 문법. | :hover·:focus-visible |
| **Pseudo-element** | 요소의 가상 부분을 선택하는 문법. | ::before·::after |
| **CSS Variable** | CSS에서 재사용하는 사용자 정의 속성. | var(--space-md) |
| **Logical Properties** | 쓰기 방향에 대응하는 레이아웃 속성. | margin-inline-start |
| **Unit px** | CSS의 기준 픽셀 단위. | width: 320px |
| **Unit rem** | 루트 요소의 글꼴 크기를 기준으로 한 단위. | 1rem |
| **Unit em** | 해당 속성 문맥의 글꼴 크기를 기준으로 한 상대 단위. | padding: 1em |
| **Unit vw/vh** | 뷰포트 너비·높이의 1% 단위. | 100vh |
| **Unit dvh** | 동적으로 변하는 모바일 뷰포트 높이 단위. | min-height: 100dvh |
| **Object-fit** | 대체 요소 콘텐츠가 지정 상자에 맞춰지는 방식. | cover·contain |
| **CSS Reset** | 브라우저 기본 스타일을 초기화하거나 정규화. | reset stylesheet |
| **Utility-first CSS** | 작은 목적별 CSS 클래스를 조합하는 접근. | Tailwind CSS |
| **BEM** | Block Element Modifier 기반 클래스 명명 규칙. | card__title--large |

## 참고 자료

전체 참고 링크와 영역별 자료는 [REFERENCES.md](../REFERENCES.md)에 정리했습니다.
