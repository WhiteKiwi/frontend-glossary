# Web & Browser

Core technologies, browser internals, network behavior, and platform APIs.

[← Home](../README.md) · [A–Z index](../INDEX.md) · [Comparisons](../COMPARISONS.md) · [Sources](../REFERENCES.md)


## Documents & JavaScript runtime

| Term | Definition | Example |
| --- | --- | --- |
| <a id="html"></a>**HTML** | The markup language used to structure and give meaning to web documents. | The main element |
| <a id="semantic-html"></a>**Semantic HTML** | Using HTML elements according to their intended meaning. | Use button instead of clickable div |
| <a id="dom"></a>**DOM** | Document Object Model; a programmable tree representation of a document. | document.querySelector() |
| <a id="cssom"></a>**CSSOM** | CSS Object Model; a representation of parsed style rules and declarations. | Browser style computation |
| <a id="render-tree"></a>**Render Tree** | The browser's representation of visible content used to calculate layout and paint. | Elements prepared for rendering |
| <a id="javascript"></a>**JavaScript** | The programming language used to create dynamic behavior on the web. | Event handlers |
| <a id="typescript"></a>**TypeScript** | A typed superset of JavaScript with compile-time checking. | interface User |
| <a id="event-loop"></a>**Event Loop** | The runtime mechanism coordinating task execution and event processing. | Scheduling async callbacks |
| <a id="call-stack"></a>**Call Stack** | The stack of currently executing function calls. | Nested function calls |
| <a id="task-queue"></a>**Task Queue** | A scheduling queue for tasks ready to run on an event loop. | setTimeout callbacks |
| <a id="microtask"></a>**Microtask** | A high-priority queued job processed at microtask checkpoints. | Promise.then callback |
| <a id="promise"></a>**Promise** | An object representing eventual completion or failure of an asynchronous operation. | fetch().then() |
| <a id="asyncawait"></a>**async/await** | Syntax for working with promises in a sequential-looking form. | await fetch() |
| <a id="closure"></a>**Closure** | A function's ability to retain access to variables from its lexical scope. | Private counter function |
| <a id="callback"></a>**Callback** | A function passed to other code for later execution. | onClick handler |
| <a id="hoisting"></a>**Hoisting** | How declarations are registered before code execution, affecting when names are accessible. | Function versus let declarations |
| <a id="scope"></a>**Scope** | The region of code in which a binding can be accessed. | Block-scoped variable |
| <a id="garbage-collection"></a>**Garbage Collection** | Automatic reclamation of memory that is no longer reachable. | Reclaim an unreferenced object |

## HTTP, APIs & storage

| Term | Definition | Example |
| --- | --- | --- |
| <a id="http"></a>**HTTP** | The request–response application protocol used by the web. | GET /products |
| <a id="https"></a>**HTTPS** | HTTP transported over a secure TLS connection. | https:// URL |
| <a id="request"></a>**Request** | A message from a client asking a server to perform or return something. | POST /orders |
| <a id="response"></a>**Response** | A server message providing status, headers, and optionally content. | 200 OK with JSON |
| <a id="http-method"></a>**HTTP Method** | A verb indicating intended HTTP request semantics. | GET, POST, PUT, PATCH, DELETE |
| <a id="status-code"></a>**Status Code** | A three-digit HTTP response code indicating the result. | 200, 404, 500 |
| <a id="rest"></a>**REST** | An architectural style for stateless, resource-oriented distributed interfaces. | Resource URL /users/42 |
| <a id="graphql"></a>**GraphQL** | A query language and runtime for APIs where clients specify requested fields. | query User |
| <a id="fetch-api"></a>**Fetch API** | A browser API for making and handling network requests. | fetch('/api') |
| <a id="cors"></a>**CORS** | Cross-Origin Resource Sharing; a browser-enforced protocol for permitted cross-origin responses. | Access-Control-Allow-Origin |
| <a id="same-origin-policy"></a>**Same-origin Policy** | A browser security policy limiting interactions between documents from different origins. | Scheme, host, and port boundaries |
| <a id="cookie"></a>**Cookie** | A small piece of state stored and often sent with matching HTTP requests. | Session cookie |
| <a id="local-storage"></a>**Local Storage** | Persistent, origin-scoped browser key–value storage. | Saved theme setting |
| <a id="session-storage"></a>**Session Storage** | Key–value storage scoped to an origin and a tab's page session. | Temporary form data |
| <a id="indexeddb"></a>**IndexedDB** | An asynchronous browser database for structured data. | Offline documents |
| <a id="service-worker"></a>**Service Worker** | A worker that can intercept requests and support caching, push, and offline behavior. | Offline app shell |
| <a id="web-worker"></a>**Web Worker** | A script running in a separate execution context from the main page thread. | Heavy parsing job |
| <a id="web-api"></a>**Web API** | A feature exposed by browsers through a programmable interface. | IntersectionObserver |

## Browser observers & navigation

| Term | Definition | Example |
| --- | --- | --- |
| <a id="intersection-observer"></a>**Intersection Observer** | An API that observes how a target intersects a root or viewport. | Load images when visible |
| <a id="resize-observer"></a>**Resize Observer** | An API that observes changes to an element's dimensions. | Resize a chart with its container |
| <a id="mutation-observer"></a>**Mutation Observer** | An API that observes changes to DOM nodes and their descendants. | Detect inserted widgets |
| <a id="history-api"></a>**History API** | Browser APIs for navigating or changing the session history. | history.pushState() |
| <a id="url"></a>**URL** | Uniform Resource Locator; an address identifying a resource and its access scheme. | https://example.com/path |
| <a id="query-string"></a>**Query String** | The part of a URL after ? containing query parameters. | ?page=2 |
| <a id="fragment"></a>**Fragment** | The part of a URL after # referring to a location or state. | #installation |
| <a id="dns"></a>**DNS** | Domain Name System; resolves domain names to IP addresses and other records. | Lookup example.com |
| <a id="tls"></a>**TLS** | Transport Layer Security; the protocol securing data in transit. | HTTPS handshake |
| <a id="cdn"></a>**CDN** | Content Delivery Network; distributed infrastructure serving content closer to users. | Static image delivery |
| <a id="web-storage"></a>**Web Storage** | The set of localStorage and sessionStorage storage APIs. | Store UI preferences |
| <a id="content-security-policy"></a>**Content Security Policy** | A security policy that restricts allowed resource loads and execution contexts. | script-src directive |

For related articles and official documentation, see [References](../REFERENCES.md).
