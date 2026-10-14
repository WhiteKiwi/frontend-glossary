# State & Data

State ownership, network data, caching, asynchronous work, and concurrency.

[← Home](../README.md) · [A–Z index](../INDEX.md) · [Comparisons](../COMPARISONS.md) · [Sources](../REFERENCES.md)


## State models & ownership

| Term | Definition | Example |
| --- | --- | --- |
| <a id="state"></a>**State** | Data representing the current condition of an interface or application. | isDialogOpen |
| <a id="props"></a>**Props** | Inputs passed from a parent component to a child. | title prop |
| <a id="local-state"></a>**Local State** | State managed within a component or its close subtree. | Expanded accordion |
| <a id="global-state"></a>**Global State** | State shared across distant parts of an application. | Signed-in user |
| <a id="server-state"></a>**Server State** | Data whose authoritative source is a remote server. | Product catalog |
| <a id="derived-state"></a>**Derived State** | Values computed from other state instead of separately stored. | Filtered item count |
| <a id="state-machine"></a>**State Machine** | A model listing valid states and transitions between them. | idle → loading → success |
| <a id="reducer"></a>**Reducer** | A function computing the next state from the current state and an action. | React useReducer |
| <a id="controlled-component"></a>**Controlled Component** | A component whose current input value is controlled by external state. | value and onChange |
| <a id="uncontrolled-component"></a>**Uncontrolled Component** | A component that keeps its input value in an internal or DOM-managed state. | ref to an input |
| <a id="single-source-of-truth"></a>**Single Source of Truth** | A design principle that assigns one authoritative representation to each fact. | Avoid duplicated totals |
| <a id="prop-drilling"></a>**Prop Drilling** | Passing props through intermediate components that do not otherwise need them. | Deeply nested theme prop |
| <a id="context"></a>**Context** | A mechanism for sharing values with a component subtree. | React ThemeContext |
| <a id="store"></a>**Store** | A container holding application state and providing update mechanisms. | Redux store |
| <a id="immutable-update"></a>**Immutable Update** | Producing a new value instead of mutating an existing state object in place. | Copy array before changing |

## Updates, caching & communication

| Term | Definition | Example |
| --- | --- | --- |
| <a id="optimistic-update"></a>**Optimistic Update** | Updating the UI immediately, then confirming or reverting based on server outcome. | Like button updates instantly |
| <a id="rollback"></a>**Rollback** | Reverting a tentative update when it fails. | Undo failed optimistic Like |
| <a id="pessimistic-update"></a>**Pessimistic Update** | Updating the UI only after the server confirms the action. | Display transfer after approval |
| <a id="cache"></a>**Cache** | Stored results reused to avoid repeated work or network requests. | Cached product list |
| <a id="cache-invalidation"></a>**Cache Invalidation** | Marking cached data invalid when it may no longer match the source. | Refetch after editing item |
| <a id="stale-data"></a>**Stale Data** | Cached information that is no longer the most recent available version. | Old search results |
| <a id="stale-while-revalidate"></a>**Stale-While-Revalidate** | Showing available cached data while fetching a newer version in the background. | Instant list plus refresh |
| <a id="ttl"></a>**TTL** | Time to Live; the duration for which stored data is considered valid or retained. | Five-minute cache TTL |
| <a id="polling"></a>**Polling** | Requesting fresh data repeatedly at a configured interval. | Check job status every 5 seconds |
| <a id="long-polling"></a>**Long Polling** | An HTTP request the server holds until data is available or a timeout occurs. | Near-real-time notifications |
| <a id="sse"></a>**SSE** | Server-Sent Events; a one-way event stream from server to browser over HTTP. | Live progress events |
| <a id="websocket"></a>**WebSocket** | A protocol for continuous, bidirectional messages over one connection. | Realtime collaboration |
| <a id="request-deduplication"></a>**Request Deduplication** | Avoiding redundant requests by merging, sharing, or discarding equivalent work. | Share identical GET requests |
| <a id="single-flight"></a>**Single-flight** | Ensuring concurrent calls for the same key share one in-progress operation. | One token refresh for many callers |
| <a id="idempotency"></a>**Idempotency** | A property whereby repeating an operation has no additional effect after the first application. | Payment request with an idempotency key |
| <a id="race-condition"></a>**Race Condition** | A bug or hazard in which outcome depends on the ordering of concurrent operations. | Out-of-order search responses |
| <a id="abortcontroller"></a>**AbortController** | A Web API that sends abort signals to supporting asynchronous operations. | Cancel a previous fetch |
| <a id="retry"></a>**Retry** | Attempting a failed operation again according to defined conditions. | Retry transient network failure |
| <a id="exponential-backoff"></a>**Exponential Backoff** | Increasing retry delays exponentially after successive failures. | 1s, 2s, 4s |
| <a id="jitter"></a>**Jitter** | Adding random variation to delays to reduce synchronized retry spikes. | Randomized retry wait |
| <a id="rate-limiting"></a>**Rate Limiting** | Restricting the number of operations allowed in a time interval. | 100 API requests per minute |

## Pagination & representation

| Term | Definition | Example |
| --- | --- | --- |
| <a id="infinite-query"></a>**Infinite Query** | A pattern that fetches and accumulates successive result pages. | Infinite scrolling feed |
| <a id="cursor-pagination"></a>**Cursor Pagination** | Fetching the next results relative to an opaque or ordered cursor. | nextCursor token |
| <a id="offset-pagination"></a>**Offset Pagination** | Fetching results by a skip count and page size. | offset=20&limit=10 |
| <a id="normalization"></a>**Normalization** | Organizing data to reduce duplication and allow consistent references. | Entities keyed by ID |
| <a id="serialization"></a>**Serialization** | Converting a value into a format suitable for transport or storage. | Object to JSON |
| <a id="deserialization"></a>**Deserialization** | Reconstructing a value from its stored or transmitted representation. | JSON into an object |
| <a id="validation"></a>**Validation** | Checking that data satisfies defined constraints. | Validate email format |
| <a id="hydration-mismatch"></a>**Hydration Mismatch** | A discrepancy between server HTML and the client's initial render result. | Rendering a random number on both sides |
| <a id="error-boundary"></a>**Error Boundary** | A component boundary that catches supported rendering errors and displays fallback UI. | React error fallback |

For related articles and official documentation, see [References](../REFERENCES.md).
