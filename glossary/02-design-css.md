# 디자인·CSS

> 시각적 표현과 레이아웃을 제어하는 용어

[← 전체 목차](../README.md) · [알파벳 색인](../INDEX.md)

| 용어 | 설명 | 예시·주의점 |
| --- | --- | --- |
| **Design System** | 컴포넌트·규칙·토큰을 일관되게 운영하는 체계 | 디자인과 구현의 공동 기준. |
| **Design Token** | 색상·간격 같은 디자인 결정을 이름 있는 값으로 관리하는 단위 | color.primary, spacing.2. |
| **Typography** | 서체·크기·행간·무게 등 텍스트 시각 체계 | 본문과 제목 서체 규칙. |
| **Font Family** | 사용할 서체 목록 | system-ui, sans-serif. |
| **Font Weight** | 글자 획의 굵기 | 400 regular, 700 bold. |
| **Line Height** | 텍스트 줄 사이의 높이 | 가독성을 좌우한다. |
| **Letter Spacing** | 글자 사이 간격 | 제목 자간. |
| **Visual Hierarchy** | 요소의 중요도를 크기·대비·위치로 표현하는 구조 | 주 CTA를 눈에 띄게. |
| **Contrast** | 두 요소 간 밝기·색상·형태의 차이 | 텍스트 명암 대비. |
| **Color Palette** | 사용할 색상들의 집합 | 브랜드색·중립색. |
| **Opacity** | 요소의 불투명도 | opacity: 0.5. |
| **Elevation** | 표면이 서로 다른 높이에 있는 것처럼 표현한 단계 | 그림자와 겹침. |
| **Box Shadow** | 요소 주위에 그리는 그림자 | 카드의 깊이 표현. |
| **Border** | 요소 경계선 | 1px solid. |
| **Border Radius** | 모서리의 둥근 정도 | border-radius: 12px. |
| **Spacing** | 요소 사이 또는 내부의 간격 체계 | 4·8·16px 스케일. |
| **Margin** | 요소 경계 바깥쪽 여백 | margin-top. |
| **Padding** | 요소 경계 안쪽 여백 | padding-inline. |
| **Gap** | Flex/Grid 항목 사이 간격 | gap: 1rem. |
| **Box Model** | 콘텐츠·패딩·테두리·마진으로 구성되는 CSS 상자 모델 | 크기 계산 기본. |
| **Box Sizing** | width/height에 padding·border를 포함할지 결정 | border-box. |
| **Display** | 요소의 기본 레이아웃 동작 | block, inline, flex, grid. |
| **Flexbox** | 주 축과 교차 축을 기준으로 배치하는 1차원 레이아웃 | 가로 정렬. |
| **Grid** | 행과 열을 정의하는 2차원 레이아웃 | 카드 격자. |
| **Position** | 요소 배치의 기준과 방식을 설정 | relative, absolute, fixed, sticky. |
| **Sticky** | 스크롤 위치가 임계점에 이르면 기준 영역 안에서 붙는 배치 | 고정형 섹션 헤더. |
| **Overflow** | 내용이 상자 범위를 넘을 때의 처리 | hidden, auto, scroll. |
| **Z-index** | 동일 스태킹 맥락 안에서 겹침 순서를 제어하는 값 | 팝업 계층. |
| **Stacking Context** | 자식 요소의 쌓임 순서를 독립적으로 계산하는 맥락 | z-index가 기대와 다를 때 점검. |
| **Specificity** | CSS 선택자 우선순위 계산 규칙 | ID와 클래스 충돌. |
| **Cascade** | 출처·레이어·중요도·우선순위 등에 따라 CSS 선언을 결정하는 과정 | 마지막 선언만으로 결정되지 않는다. |
| **Inheritance** | 일부 CSS 속성이 부모에서 자식으로 전달되는 동작 | color 상속. |
| **Pseudo-class** | 요소 상태 등에 따라 선택하는 선택자 | :hover, :focus-visible. |
| **Pseudo-element** | 요소의 특정 부분이나 생성 내용을 선택 | ::before, ::after. |
| **CSS Custom Property** | CSS에서 정의하고 참조하는 사용자 지정 속성 | --space-sm. |
| **Media Query** | 미디어 특성에 따라 스타일을 분기하는 규칙 | @media (min-width: 768px). |
| **Container Query** | 부모 컨테이너 크기·스타일 등에 따라 분기 | 재사용 카드 레이아웃. |
| **Breakpoint** | 레이아웃이 전환되는 조건상의 임계점 | 768px에서 2열로 전환. |
| **Responsive Design** | 화면 크기에 유연히 적응하는 설계 | 유동 너비 레이아웃. |
| **Adaptive Design** | 조건에 따라 미리 설계한 배치 중 하나를 선택 | 특정 화면 크기별 레이아웃. |
| **Viewport** | 브라우저에서 콘텐츠가 표시되는 가시 영역 | 모바일 viewport. |
| **DPR (Device Pixel Ratio)** | CSS 픽셀과 물리 픽셀 사이 비율 | 고해상도 이미지 선택. |
| **rem** | 루트 요소 글꼴 크기에 상대적인 단위 | 1rem = 루트 font-size. |
| **em** | 해당 속성에 따라 현재 요소 또는 부모의 글꼴 크기에 상대적인 단위 | font-size: 1.2em. |
| **vh / vw** | 뷰포트 높이·너비의 1% 단위 | 100vh의 모바일 한계 주의. |
| **dvh / svh / lvh** | 동적·최소·최대 뷰포트 높이 단위 | 모바일 주소창 변화를 고려. |
| **Aspect Ratio** | 상자의 가로·세로 비율 | 16 / 9 썸네일. |
| **Logical Properties** | 쓰기 방향에 독립적인 CSS 속성 | margin-inline-start. |
| **Clamp** | 최솟값·선호값·최댓값 사이에서 값을 제한하는 함수 | clamp(1rem, 2vw, 2rem). |

---

관련 참고 문헌은 [REFERENCES.md](../REFERENCES.md)에서 확인할 수 있습니다.
