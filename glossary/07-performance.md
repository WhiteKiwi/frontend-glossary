# Performance & Optimization

Browser speed, loading strategies, user-centric metrics, and efficient rendering.

[← Home](../README.md) · [A–Z index](../INDEX.md) · [Comparisons](../COMPARISONS.md) · [Sources](../REFERENCES.md)


## User-centric metrics

| Term | Definition | Example |
| --- | --- | --- |
| <a id="core-web-vitals"></a>**Core Web Vitals** | A set of key metrics that describe real-world loading, interactivity, and visual stability. | LCP, INP, CLS |
| <a id="lcp"></a>**LCP** | Largest Contentful Paint; the time when the largest eligible visible element is rendered. | Hero image appearing |
| <a id="inp"></a>**INP** | Interaction to Next Paint; a metric of how promptly a page responds to user interactions. | Click response delay |
| <a id="cls"></a>**CLS** | Cumulative Layout Shift; a measure of unexpected layout movement. | Image loading pushes content |
| <a id="fcp"></a>**FCP** | First Contentful Paint; the time when the first piece of content is rendered. | First heading appears |
| <a id="ttfb"></a>**TTFB** | Time to First Byte; the duration until the first response byte is received. | Slow origin response |
| <a id="tbt"></a>**TBT** | Total Blocking Time; summed main-thread blocking time above a threshold during a measured loading period. | Heavy JS startup |
| <a id="rum"></a>**RUM** | Real User Monitoring; collecting performance measurements from actual visits. | Field LCP telemetry |
| <a id="synthetic-monitoring"></a>**Synthetic Monitoring** | Running predefined tests under controlled conditions. | Scheduled Lighthouse run |
| <a id="lighthouse"></a>**Lighthouse** | A tool that audits page performance, accessibility, and other quality signals. | Performance report |
| <a id="performance-budget"></a>**Performance Budget** | A defined limit for page weight, latency, or performance metrics. | Maximum JS bundle size |

## Loading & network

| Term | Definition | Example |
| --- | --- | --- |
| <a id="lazy-loading"></a>**Lazy Loading** | Loading resources or code only when needed. | Below-the-fold images |
| <a id="eager-loading"></a>**Eager Loading** | Loading resources immediately rather than deferring them. | Critical logo |
| <a id="preload"></a>**Preload** | A resource hint that gives higher priority discovery to resources needed on the current page. | Important web font |
| <a id="prefetch"></a>**Prefetch** | A resource hint for fetching content that may be needed in future navigation. | Likely next route |
| <a id="preconnect"></a>**Preconnect** | A hint to establish an early connection to another origin. | Prepare font CDN connection |
| <a id="dns-prefetch"></a>**DNS Prefetch** | A hint to resolve a domain name before a request needs it. | Third-party asset domain |
| <a id="resource-hint"></a>**Resource Hint** | A browser hint that guides early fetching or connection work. | preload, preconnect |
| <a id="critical-rendering-path"></a>**Critical Rendering Path** | The steps required for a browser to turn HTML, CSS, and JS into initial pixels. | Parse, style, layout, paint |
| <a id="render-blocking"></a>**Render Blocking** | Resources or work that delay the browser's ability to display content. | Blocking stylesheet |

## Rendering & computation

| Term | Definition | Example |
| --- | --- | --- |
| <a id="reflowlayout"></a>**Reflow/Layout** | Computing or recomputing the size and position of elements. | Recalculate after width change |
| <a id="repaint"></a>**Repaint** | Redrawing changed visual content when layout does not necessarily change. | Background color update |
| <a id="compositing"></a>**Compositing** | Combining rendered layers into the final displayed image. | Transform animation layers |
| <a id="layout-thrashing"></a>**Layout Thrashing** | Repeated alternating layout reads and writes that trigger forced synchronous layouts. | Loop calling offsetWidth |
| <a id="virtualization"></a>**Virtualization** | Rendering only currently visible or nearby items from a large collection. | 100,000-row list |
| <a id="memoization"></a>**Memoization** | Caching computation results for reuse with the same inputs. | useMemo() |
| <a id="caching"></a>**Caching** | Storing computed or downloaded data to avoid repeating the work. | HTTP response cache |
| <a id="image-optimization"></a>**Image Optimization** | Reducing image transfer and decode costs with suitable sizing and formats. | AVIF thumbnails |
| <a id="responsive-images"></a>**Responsive Images** | Providing image candidates suited to display size and pixel density. | srcset and sizes |
| <a id="webp"></a>**WebP** | An image format with lossy and lossless compression options. | Compressed product photo |
| <a id="avif"></a>**AVIF** | An image format often achieving high visual quality at relatively small sizes. | Hero image asset |
| <a id="svg"></a>**SVG** | Scalable Vector Graphics; an XML-based vector image format. | Crisp UI icon |
| <a id="font-subsetting"></a>**Font Subsetting** | Including only the glyphs needed by a product or locale in a font file. | Subset Korean font |
| <a id="foit"></a>**FOIT** | Flash of Invisible Text; text remains hidden while a web font loads. | Delayed headline |
| <a id="fout"></a>**FOUT** | Flash of Unstyled Text; fallback text appears before the web font swaps in. | font-display: swap |
| <a id="minification"></a>**Minification** | Reducing code size by removing unnecessary syntax and shortening safe identifiers. | Minified JavaScript |
| <a id="compression"></a>**Compression** | Encoding resources more compactly for transfer. | Brotli or gzip |
| <a id="bundle-analyzer"></a>**Bundle Analyzer** | A tool showing which modules contribute to bundle size. | Detect a large dependency |
| <a id="long-task"></a>**Long Task** | Main-thread work lasting long enough to risk blocking user interaction. | A task over 50 ms |
| <a id="main-thread"></a>**Main Thread** | The primary browser thread responsible for much DOM and UI work. | Click handler execution |
| <a id="requestanimationframe"></a>**requestAnimationFrame** | An API that schedules a callback before a browser repaint. | Coordinate visual updates |
| <a id="requestidlecallback"></a>**requestIdleCallback** | An API requesting callbacks during browser idle periods where supported. | Low-priority analytics work |
| <a id="memory-leak"></a>**Memory Leak** | Memory that remains reachable and therefore uncollected despite no longer being useful. | Unremoved event listener |
| <a id="backpressure"></a>**Backpressure** | Mechanisms for controlling producers when consumers cannot keep up. | Stream processing throttle |

For related articles and official documentation, see [References](../REFERENCES.md).
