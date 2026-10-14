# Quality, Security & Tooling

Accessibility, discoverability, tests, application security, and developer workflows.

[← Home](../README.md) · [A–Z index](../INDEX.md) · [Comparisons](../COMPARISONS.md) · [Sources](../REFERENCES.md)


## Accessibility & semantics

| Term | Definition | Example |
| --- | --- | --- |
| <a id="a11y"></a>**a11y** | An abbreviation for accessibility; designing interfaces usable by people with varied abilities. | Keyboard-operable controls |
| <a id="wcag"></a>**WCAG** | Web Content Accessibility Guidelines; criteria for making web content more accessible. | Contrast and keyboard support |
| <a id="aria"></a>**ARIA** | Accessible Rich Internet Applications; attributes and roles that convey semantics to assistive technology. | aria-expanded |
| <a id="accessible-name"></a>**Accessible Name** | The name by which assistive technology identifies a UI element. | Label for icon-only button |
| <a id="screen-reader"></a>**Screen Reader** | Assistive software that presents interface content as speech or braille. | VoiceOver |
| <a id="tab-order"></a>**Tab Order** | The sequence in which keyboard focus advances through controls. | Logical form navigation |
| <a id="landmark"></a>**Landmark** | A semantically marked major region that aids page navigation. | main and navigation |
| <a id="semantic-role"></a>**Semantic Role** | The purpose or function an element conveys in the accessibility tree. | button role |
| <a id="color-contrast-ratio"></a>**Color Contrast Ratio** | A numerical comparison of relative luminance between two colors. | Text contrast of 4.5:1 |
| <a id="alt-text"></a>**Alt Text** | A text alternative conveying the meaning of an image. | Descriptive alt attribute |

## Search discovery

| Term | Definition | Example |
| --- | --- | --- |
| <a id="seo"></a>**SEO** | Search Engine Optimization; improving how search engines discover and understand content. | Useful titles and internal links |
| <a id="canonical-url"></a>**Canonical URL** | A signal indicating a preferred URL for equivalent or near-duplicate content. | rel=canonical |
| <a id="open-graph"></a>**Open Graph** | Metadata conventions used to describe a page when shared on social platforms. | og:title and og:image |
| <a id="sitemap"></a>**Sitemap** | A file listing discoverable URLs and optional metadata for crawlers. | sitemap.xml |
| <a id="robotstxt"></a>**Robots.txt** | A standard file expressing crawl permissions to cooperating robots; not an access-control mechanism. | Disallow a staging path |
| <a id="structured-data"></a>**Structured Data** | Machine-readable data that identifies entities and relationships in content. | JSON-LD for products |

## Testing

| Term | Definition | Example |
| --- | --- | --- |
| <a id="unit-test"></a>**Unit Test** | A test checking a small isolated unit of behavior. | Price formatter |
| <a id="integration-test"></a>**Integration Test** | A test checking behavior across multiple connected parts. | Form with mocked API |
| <a id="e2e-test"></a>**E2E Test** | End-to-End test; checks an application flow from the user's perspective. | Login to checkout |
| <a id="visual-regression"></a>**Visual Regression** | A test comparing rendered visuals to catch unintended appearance changes. | Screenshot diff |
| <a id="snapshot-test"></a>**Snapshot Test** | A test comparing current serialized output against a stored reference. | Rendered component snapshot |
| <a id="mock"></a>**Mock** | A substitute for a real dependency, often configurable for interactions and assertions. | Mock HTTP client |
| <a id="stub"></a>**Stub** | A substitute that returns predetermined results. | Fixed clock response |
| <a id="fixture"></a>**Fixture** | Reusable input or environment data prepared for tests. | Sample user JSON |
| <a id="test-pyramid"></a>**Test Pyramid** | A strategy balancing fast, focused tests against slower, broad end-to-end tests. | More unit tests than E2E tests |
| <a id="flaky-test"></a>**Flaky Test** | A test whose outcome varies without a meaningful change in the code under test. | Timing-sensitive async test |

## Security & identity

| Term | Definition | Example |
| --- | --- | --- |
| <a id="xss"></a>**XSS** | Cross-Site Scripting; execution of attacker-controlled content in a trusted page context. | Unsafe HTML injection |
| <a id="csrf"></a>**CSRF** | Cross-Site Request Forgery; tricking an authenticated browser into sending unintended requests. | Forged state-changing form |
| <a id="csp"></a>**CSP** | Content Security Policy; rules restricting what resources and scripts a page may load or execute. | script-src |
| <a id="sri"></a>**SRI** | Subresource Integrity; checking external resource bytes against a declared cryptographic hash. | integrity attribute |
| <a id="authentication"></a>**Authentication** | The process of verifying who a user or system is. | Sign-in |
| <a id="authorization"></a>**Authorization** | Determining which actions a user or system is allowed to perform. | Admin-only settings |
| <a id="oauth-20"></a>**OAuth 2.0** | An authorization framework for delegating limited access to resources. | Connect an external account |
| <a id="oidc"></a>**OIDC** | OpenID Connect; an identity layer on top of OAuth 2.0 for authentication. | ID token |
| <a id="jwt"></a>**JWT** | JSON Web Token; a compact, signed or encrypted claims format. | Signed access token |
| <a id="samesite-cookie"></a>**SameSite Cookie** | A cookie attribute restricting its use in cross-site request contexts. | SameSite=Lax |
| <a id="httponly-cookie"></a>**HttpOnly Cookie** | A cookie attribute preventing access through document.cookie. | Session cookie |
| <a id="secure-cookie"></a>**Secure Cookie** | A cookie attribute limiting transmission to secure channels. | Secure session cookie |

## Build tools & operations

| Term | Definition | Example |
| --- | --- | --- |
| <a id="bundler"></a>**Bundler** | A tool that resolves and packages code modules and assets for deployment. | Vite or Webpack |
| <a id="transpiler"></a>**Transpiler** | A tool that transforms source code into another source-level representation. | TypeScript to JavaScript |
| <a id="polyfill"></a>**Polyfill** | Code providing support for a platform feature missing in an environment. | Legacy browser fallback |
| <a id="hmr"></a>**HMR** | Hot Module Replacement; updating modules in development without a full page reload. | Instant CSS changes |
| <a id="source-map"></a>**Source Map** | Metadata mapping generated code positions back to original source code. | Debug minified stack trace |
| <a id="lint"></a>**Lint** | Static analysis to catch suspicious patterns and enforce code conventions. | ESLint |
| <a id="formatter"></a>**Formatter** | A tool that standardizes code layout automatically. | Prettier |
| <a id="ci"></a>**CI** | Continuous Integration; automatic validation when changes are merged or proposed. | PR test pipeline |
| <a id="cd"></a>**CD** | Continuous Delivery or Deployment; automating release readiness or actual rollout. | Production deployment workflow |
| <a id="feature-flag"></a>**Feature Flag** | A configuration switch used to control feature availability without new deployment. | Gradual launch |
| <a id="observability"></a>**Observability** | The ability to infer system behavior from telemetry such as logs, traces, and metrics. | Investigate frontend errors |
| <a id="sentry"></a>**Sentry** | An example of a service for collecting application errors and performance events. | Track production crashes |

For related articles and official documentation, see [References](../REFERENCES.md).
