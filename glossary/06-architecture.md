# Architecture

Component composition, rendering strategies, code organization, and application structure.

[← Home](../README.md) · [A–Z index](../INDEX.md) · [Comparisons](../COMPARISONS.md) · [Sources](../REFERENCES.md)


## Components & design patterns

| Term | Definition | Example |
| --- | --- | --- |
| <a id="component"></a>**Component** | A reusable, encapsulated unit of UI and behavior. | Button component |
| <a id="composition"></a>**Composition** | Building complex interfaces by combining smaller units. | Card with Avatar and Title |
| <a id="containerpresentational"></a>**Container/Presentational** | A design pattern separating data orchestration from rendering responsibilities. | Loader and item list |
| <a id="custom-hook"></a>**Custom Hook** | A reusable React function that encapsulates hook-based logic. | useDebounce() |
| <a id="hook"></a>**Hook** | An API that lets compatible components access state and lifecycle-like features. | useState() |
| <a id="lifecycle"></a>**Lifecycle** | The stages of a UI component's existence and updates. | Mount, update, unmount |
| <a id="side-effect"></a>**Side Effect** | An operation that affects or interacts with systems beyond pure value computation. | Subscribe to events |
| <a id="dependency-injection"></a>**Dependency Injection** | Providing dependencies from outside a module instead of creating them internally. | Inject an API client |
| <a id="separation-of-concerns"></a>**Separation of Concerns** | Organizing code so distinct responsibilities are managed independently. | Separate data fetching from display |
| <a id="solid"></a>**SOLID** | Five object-oriented design principles for maintainable responsibilities and dependencies. | Single Responsibility Principle |
| <a id="atomic-design"></a>**Atomic Design** | A method of organizing interfaces as atoms, molecules, organisms, and larger compositions. | Button to SearchForm |
| <a id="design-system"></a>**Design System** | A coordinated library of design rules, tokens, components, and usage guidance. | Shared UI kit |
| <a id="monorepo"></a>**Monorepo** | A repository containing multiple packages or projects. | App and component library in one repo |
| <a id="microfrontend"></a>**Microfrontend** | A frontend architecture divided into independently developed and integrated application segments. | Separate checkout frontend |

## Rendering strategies

| Term | Definition | Example |
| --- | --- | --- |
| <a id="spa"></a>**SPA** | Single-Page Application; navigation generally updates one loaded document on the client. | Client-side router |
| <a id="mpa"></a>**MPA** | Multi-Page Application; navigation commonly loads different HTML documents. | Traditional server-rendered site |
| <a id="csr"></a>**CSR** | Client-Side Rendering; UI is primarily generated in the browser. | JS-rendered dashboard |
| <a id="ssr"></a>**SSR** | Server-Side Rendering; HTML is generated for a request on the server. | Server-rendered product page |
| <a id="ssg"></a>**SSG** | Static Site Generation; HTML is generated ahead of requests, typically at build time. | Static documentation site |
| <a id="isr"></a>**ISR** | Incremental Static Regeneration; a framework technique for regenerating static pages after deployment. | Next.js revalidation |
| <a id="hydration"></a>**Hydration** | Attaching client-side state and interactivity to server-rendered markup. | React hydration |
| <a id="streaming-ssr"></a>**Streaming SSR** | Sending server-rendered HTML progressively as parts become ready. | Stream content around Suspense |
| <a id="react-server-components"></a>**React Server Components** | A React component model that renders selected components on the server and sends a serialized result. | Server-side data component |
| <a id="islands-architecture"></a>**Islands Architecture** | A design that activates isolated interactive sections within mostly static HTML. | Interactive search widget on a static page |

## Routing & infrastructure

| Term | Definition | Example |
| --- | --- | --- |
| <a id="routing"></a>**Routing** | Mapping URLs to screens or resource handlers. | /users/:id |
| <a id="client-side-routing"></a>**Client-side Routing** | Changing views and browser history without a full document navigation. | SPA route transitions |
| <a id="nested-routing"></a>**Nested Routing** | Representing parent and child routes with shared UI structure. | Settings layout and subpages |
| <a id="dynamic-route"></a>**Dynamic Route** | A route whose path includes variable segments. | /posts/[id] |
| <a id="layout-route"></a>**Layout Route** | A route that supplies a layout shared by nested destinations. | Dashboard shell |
| <a id="middleware"></a>**Middleware** | Logic placed between request arrival and its final handler or response. | Authentication check |
| <a id="bff"></a>**BFF** | Backend for Frontend; a server layer tailored to a particular client interface. | Mobile-specific API composition |
| <a id="api-gateway"></a>**API Gateway** | An entry point that routes and governs access to downstream APIs. | Central authentication and routing |
| <a id="feature-flag"></a>**Feature Flag** | A configuration switch that enables or disables a feature independently of deployment. | Gradual rollout |
| <a id="ab-testing"></a>**A/B Testing** | An experiment comparing variants across user groups. | Compare CTA text |
| <a id="dependency-graph"></a>**Dependency Graph** | A graph describing how modules or packages depend on one another. | Bundle import dependencies |
| <a id="tree-shaking"></a>**Tree Shaking** | Removing unused static module exports from output bundles. | Drop unused library code |
| <a id="code-splitting"></a>**Code Splitting** | Dividing code into chunks loaded on demand. | Route-level lazy imports |
| <a id="module-federation"></a>**Module Federation** | A technique for composing separately built modules at runtime. | Remote microfrontend module |
| <a id="esm"></a>**ESM** | ECMAScript Modules; the standardized import/export module system. | import x from 'x' |
| <a id="commonjs"></a>**CommonJS** | A module system commonly used by older Node.js code. | require('x') |

## Rendering models & decisions

| Term | Definition | Example |
| --- | --- | --- |
| <a id="reconciliation"></a>**Reconciliation** | Comparing desired UI with the previous representation to decide what to update. | React rerender diff |
| <a id="virtual-dom"></a>**Virtual DOM** | An in-memory representation of a UI tree used by some libraries. | React element tree |
| <a id="declarative-ui"></a>**Declarative UI** | Describing the desired interface state rather than direct manipulation steps. | Render view from state |
| <a id="imperative-ui"></a>**Imperative UI** | Directly specifying steps that change interface elements. | element.appendChild() |
| <a id="architecture-decision-record"></a>**Architecture Decision Record** | A short document recording an architectural choice, alternatives, and rationale. | ADR-001 |

For related articles and official documentation, see [References](../REFERENCES.md).
