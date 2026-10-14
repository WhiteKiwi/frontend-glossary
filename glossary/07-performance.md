# 성능·최적화 · 체감 속도

> [전체 목차](../README.md) · [알파벳 색인](../INDEX.md) · [참고 자료](../REFERENCES.md)

이 문서의 용어는 이해하기 쉬운 요약 정의입니다. 구체적인 동작은 공식 명세·디자인 시스템에 따라 달라질 수 있습니다.

| 용어 | 설명 | 예시·활용 |
| --- | --- | --- |
| **Core Web Vitals** | 실사용자 경험을 대표하는 주요 웹 성능 지표 묶음. | LCP·INP·CLS |
| **LCP** | Largest Contentful Paint; 주요 큰 콘텐츠가 표시되는 시간. | 히어로 이미지 렌더 |
| **INP** | Interaction to Next Paint; 상호작용 응답성 지표. | 클릭 후 화면 갱신 |
| **CLS** | Cumulative Layout Shift; 예기치 않은 레이아웃 이동 지표. | 이미지 로딩 시 밀림 |
| **FCP** | First Contentful Paint; 첫 콘텐츠가 나타난 시점. | 초기 텍스트 표시 |
| **TTFB** | Time to First Byte; 요청 후 첫 응답 바이트까지 시간. | 서버 응답 지연 |
| **TBT** | Total Blocking Time; 측정 구간의 메인 스레드 장시간 차단 합. | 무거운 JS 실행 |
| **RUM** | Real User Monitoring; 실제 사용자 환경에서 측정하는 성능 데이터. | 운영 LCP 수집 |
| **Synthetic Monitoring** | 정해진 환경·시나리오에서 수행하는 합성 측정. | Lighthouse 반복 실행 |
| **Lighthouse** | 성능·접근성 등 웹 품질을 진단하는 도구. | 성능 점검 |
| **Performance Budget** | 허용 가능한 크기·시간·점수의 목표 한도. | JS 200KB 이하 |
| **Lazy Loading** | 실제로 필요할 때 리소스·코드를 지연 로드. | 화면 밖 이미지 |
| **Eager Loading** | 초기부터 즉시 로딩하는 전략. | 첫 화면 로고 |
| **Preload** | 현재 페이지에서 곧 필요한 리소스를 우선 발견하도록 힌트 제공. | 핵심 폰트 |
| **Prefetch** | 추후 필요할 수 있는 리소스를 미리 가져오는 힌트. | 다음 페이지 번들 |
| **Preconnect** | 외부 출처와 연결을 미리 준비하는 힌트. | 폰트 호스트 |
| **DNS Prefetch** | 외부 도메인 DNS 조회를 앞당기는 힌트. | 외부 이미지 도메인 |
| **Resource Hint** | 브라우저 로드 최적화를 위한 힌트 집합. | preload·preconnect |
| **Critical Rendering Path** | HTML·CSS·JS가 픽셀 표시로 이어지는 핵심 처리 경로. | 렌더 차단 CSS |
| **Render Blocking** | 초기 렌더 진행을 지연시키는 리소스·작업 성질. | 동기 스타일시트 |
| **Reflow/Layout** | 요소의 크기·위치를 다시 계산하는 작업. | 너비 변경 |
| **Repaint** | 레이아웃 변경 없이 픽셀 표현을 다시 그리는 작업. | 배경색 변경 |
| **Compositing** | 여러 그래픽 레이어를 합쳐 화면을 만드는 단계. | transform 애니메이션 |
| **Layout Thrashing** | 읽기·쓰기 DOM 작업이 번갈아 강제 레이아웃을 유발하는 문제. | offsetWidth 반복 |
| **Virtualization** | 보이는 항목 주변만 DOM에 렌더링하는 최적화. | 10만 행 목록 |
| **Memoization** | 같은 입력의 계산 결과를 재사용. | useMemo |
| **Caching** | 재사용 가능한 결과를 저장해 반복 비용을 절감. | HTTP cache |
| **Image Optimization** | 이미지 크기·형식·해상도·로딩을 최적화. | AVIF·srcset |
| **Responsive Images** | 화면·밀도에 맞게 이미지 후보를 선택. | sizes·srcset |
| **WebP** | 웹에서 널리 쓰이는 이미지 압축 형식. | 사진 압축 |
| **AVIF** | 높은 압축 효율을 목표로 하는 이미지 형식. | 제품 이미지 |
| **SVG** | 벡터 그래픽을 표현하는 XML 기반 형식. | 아이콘 |
| **Font Subsetting** | 실제로 쓰는 문자만 폰트에 포함해 용량 절감. | 한글 폰트 부분집합 |
| **FOIT** | 폰트가 로드되기 전 텍스트가 보이지 않는 현상. | 웹폰트 지연 |
| **FOUT** | 처음엔 대체 폰트로 보이다 웹폰트로 바뀌는 현상. | font-display: swap |
| **Minification** | 공백·식별자 등을 줄여 코드 크기를 축소. | JS 압축 |
| **Compression** | 전송 데이터를 압축해 네트워크 비용 절감. | Brotli·gzip |
| **Bundle Analyzer** | 번들 크기·구성을 시각화해 원인을 찾는 도구. | 큰 라이브러리 발견 |
| **Long Task** | 메인 스레드를 오래 점유하는 작업. | 50ms 초과 작업 |
| **Main Thread** | DOM·스타일·이벤트 등의 주요 작업이 수행되는 스레드. | 클릭 지연 |
| **requestAnimationFrame** | 다음 화면 갱신 직전에 콜백 실행을 요청하는 API. | 스크롤 애니메이션 |
| **requestIdleCallback** | 브라우저 유휴 시간에 낮은 우선순위 작업을 요청하는 API. | 비긴급 계산 |
| **Memory Leak** | 불필요한 객체가 계속 참조되어 메모리가 회수되지 않는 문제. | 이벤트 리스너 정리 누락 |
| **Backpressure** | 생산·전송 속도가 소비 속도를 넘을 때 압력을 조절하는 개념. | 스트림 처리 속도 제한 |

## 참고 자료

전체 참고 링크와 영역별 자료는 [REFERENCES.md](../REFERENCES.md)에 정리했습니다.
