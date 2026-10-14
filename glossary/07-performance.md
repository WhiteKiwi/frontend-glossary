# 성능·최적화

> 사용자 체감 속도와 리소스 효율 개선

[← 전체 목차](../README.md) · [알파벳 색인](../INDEX.md)

| 용어 | 설명 | 예시·주의점 |
| --- | --- | --- |
| **LCP (Largest Contentful Paint)** | 뷰포트의 주요 콘텐츠가 표시되기까지의 지표 | 큰 히어로 이미지 로딩. |
| **CLS (Cumulative Layout Shift)** | 예기치 않은 레이아웃 이동의 누적 정도 | 이미지 크기 미지정. |
| **INP (Interaction to Next Paint)** | 사용자 상호작용에 대한 전반적인 반응성 지표 | 느린 클릭 처리. |
| **FCP (First Contentful Paint)** | 첫 텍스트·이미지 등이 표시되는 시점 | 초기 시각 응답. |
| **TTFB (Time to First Byte)** | 요청 후 첫 응답 바이트를 받기까지의 시간 | 서버 응답 지연. |
| **Core Web Vitals** | Google의 핵심 사용자 경험 측정 지표 모음 | LCP, CLS, INP. |
| **Lazy Loading** | 필요할 때 자원을 뒤늦게 로드 | 화면 밖 이미지. |
| **Eager Loading** | 자원을 미리 적극적으로 로드 | 중요 히어로 이미지. |
| **Preload** | 현재 페이지에서 곧 필요한 리소스의 조기 로드를 알림 | 핵심 폰트. |
| **Prefetch** | 향후 필요할 가능성이 있는 리소스를 미리 가져옴 | 다음 페이지 자원. |
| **Preconnect** | 외부 출처에 사전 연결해 지연을 줄이는 힌트 | 폰트 CDN. |
| **Code Splitting** | 코드를 작은 청크로 나눠 필요 시 로드 | 라우트 단위 분할. |
| **Tree Shaking** | 사용하지 않는 정적 모듈 코드를 번들에서 제거 | 미사용 export 제거. |
| **Bundle** | 여러 코드·자원을 묶어 배포하는 결과물 | app.js. |
| **Minification** | 동작을 유지하면서 코드 표현을 줄이는 최적화 | 공백·이름 축소. |
| **Compression** | 네트워크 전송 시 자원을 압축 | gzip, Brotli. |
| **Critical Rendering Path** | 초기 화면을 그리기까지 브라우저가 수행하는 단계 | HTML→스타일→레이아웃. |
| **Reflow / Layout** | 요소의 크기·위치를 다시 계산 | 폭 변경 후 재배치. |
| **Repaint / Paint** | 시각적 내용을 다시 그림 | 배경색 변경. |
| **Compositing** | 레이어를 합성해 화면을 구성 | transform 애니메이션. |
| **Layout Thrashing** | 레이아웃 읽기와 쓰기를 반복해 동기 계산이 잦아지는 현상 | offsetWidth 반복. |
| **Virtualization** | 보이는 일부 항목만 DOM에 렌더링 | 만 건짜리 목록. |
| **Memoization** | 같은 입력의 계산 결과를 재사용 | 비싼 필터 결과 캐싱. |
| **Debounce** | 짧은 간격의 반복 이벤트를 최종 실행으로 합침 | 입력 필터 호출 감소. |
| **Throttle** | 짧은 간격의 이벤트 실행 횟수를 제한 | 스크롤 핸들러. |
| **requestAnimationFrame** | 다음 화면 갱신 직전에 콜백 실행을 요청 | 시각 업데이트 조율. |
| **requestIdleCallback** | 브라우저 유휴 구간에 낮은 우선순위 작업 요청 | 분석 작업 예약; 지원 환경 확인. |
| **Web Worker** | 메인 스레드에서 무거운 연산을 분리 | 이미지 처리. |
| **Image Optimization** | 해상도·포맷·압축을 상황에 맞게 조정 | AVIF/WebP, srcset. |
| **Responsive Images** | 표시 환경에 맞는 크기의 이미지를 선택 | srcset, sizes. |
| **Performance Budget** | 성능 상한을 팀 규칙으로 설정 | JS 200KB 이하. |
| **Lighthouse** | 페이지 성능·접근성·SEO 등을 진단하는 도구 | 정기 점검. |
| **Performance API** | 브라우저 성능 측정 정보 제공 API | performance.mark. |
| **Long Task** | 메인 스레드를 장시간 점유하는 작업 | 사용자 입력 지연. |

---

관련 참고 문헌은 [REFERENCES.md](../REFERENCES.md)에서 확인할 수 있습니다.
