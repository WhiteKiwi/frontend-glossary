# Commonly Confused Frontend Terms

> [← Home](README.md) · [A–Z index](INDEX.md)

Several interface names and engineering techniques are similar without being interchangeable. This guide focuses on the **practical distinction** and when each applies.

## UI components & navigation

| Concepts | Key distinction | When it matters |
| --- | --- | --- |
| [Navbar](glossary/01-ui-ux.md#navbar) vs. [GNB](glossary/01-ui-ux.md#gnb) vs. [LNB](glossary/01-ui-ux.md#lnb) | Navbar is a general navigation bar; GNB is product-wide; LNB is specific to a section. | Naming a site's navigation hierarchy |
| [Modal](glossary/01-ui-ux.md#modal) vs. [Dialog](glossary/01-ui-ux.md#dialog) | Modal describes interaction that blocks the background; dialog describes a UI surface. A dialog may be modal or nonmodal. | Accessibility and dismissal behavior |
| [Drawer](glossary/01-ui-ux.md#drawer) vs. [Bottom Sheet](glossary/01-ui-ux.md#bottom-sheet) vs. [Side Sheet](glossary/01-ui-ux.md#side-sheet) | Drawers and side sheets generally emerge from a side; bottom sheets emerge from below. | Platform conventions and responsive behavior |
| [Toast](glossary/01-ui-ux.md#toast) vs. [Snackbar](glossary/01-ui-ux.md#snackbar) vs. [Alert](glossary/01-ui-ux.md#alert) | Toast and snackbar often describe transient feedback and are named differently across design systems; alerts generally demand more attention. | Duration, actions, and announcement semantics |
| [Tooltip](glossary/01-ui-ux.md#tooltip) vs. [Toggletip](glossary/01-ui-ux.md#toggletip) vs. [Popover](glossary/01-ui-ux.md#popover) | A tooltip is a brief noninteractive hint; a toggletip is deliberately opened; a popover may contain controls. | Mobile access and keyboard support |
| [Select](glossary/01-ui-ux.md#select) vs. [Combobox](glossary/01-ui-ux.md#combobox) vs. [Autocomplete](glossary/01-ui-ux.md#autocomplete) | Select is choice from a list; combobox combines an input/selection with options; autocomplete is suggestion behavior. | Searching a large list of options |
| [Checkbox](glossary/01-ui-ux.md#checkbox) vs. [Radio Button](glossary/01-ui-ux.md#radio-button) vs. [Switch](glossary/01-ui-ux.md#switch) | Independent/multiple selection, mutually exclusive choice, and immediate on/off setting. | Form semantics and expectations |

## Design & interaction

| Concepts | Key distinction | When it matters |
| --- | --- | --- |
| [Margin](glossary/02-design-css.md#margin) vs. [Padding](glossary/02-design-css.md#padding) vs. [Gap](glossary/02-design-css.md#gap) | Outer spacing, inner spacing, and spacing between layout items. | Predictable CSS layout |
| [Flexbox](glossary/02-design-css.md#flexbox) vs. [Grid](glossary/02-design-css.md#grid) | Primarily one-dimensional alignment versus two-dimensional row-and-column placement. | Choosing a layout system |
| [Position Fixed](glossary/02-design-css.md#position-fixed) vs. [Position Sticky](glossary/02-design-css.md#position-sticky) | Fixed stays anchored to a containing block; sticky is constrained by its scrolling context. | Sticky headers and floating controls |
| [Responsive Design](glossary/02-design-css.md#responsive-design) vs. [Adaptive Design](glossary/02-design-css.md#adaptive-design) | Fluid adaptation versus switching among intentional layout variants. | Breakpoint and component strategy |
| [Hover](glossary/03-interaction.md#hover) vs. [Focus](glossary/03-interaction.md#focus) vs. [Active State](glossary/03-interaction.md#active-state) vs. [Selected State](glossary/03-interaction.md#selected-state) | Pointer-over, input target, currently activated, and chosen item are distinct states. | Keyboard and touch accessibility |
| [Debounce](glossary/03-interaction.md#debounce) vs. [Throttle](glossary/03-interaction.md#throttle) vs. [Cooldown](glossary/03-interaction.md#cooldown) | Wait for a quiet period, cap execution frequency, or lock an action for a period after use. | Search input, scroll, resend-code button |

## State, network & architecture

| Concepts | Key distinction | When it matters |
| --- | --- | --- |
| [Double-submit Guard](glossary/03-interaction.md#double-submit-guard) vs. [Idempotency](glossary/04-state-data.md#idempotency) | UI guards prevent common repeat actions; server-side idempotency prevents duplicate *effects*, including retries and multiple clients. | Payments, orders, irreversible actions |
| [Request Deduplication](glossary/04-state-data.md#request-deduplication) vs. [Single-flight](glossary/04-state-data.md#single-flight) vs. [Idempotency](glossary/04-state-data.md#idempotency) | Reduce redundant work, share an in-flight keyed operation, or ensure repeat application has no additional effect. | Parallel requests and data integrity |
| [Optimistic Update](glossary/04-state-data.md#optimistic-update) vs. [Pessimistic Update](glossary/04-state-data.md#pessimistic-update) | Update before remote confirmation versus update after confirmed success. | Perceived responsiveness and rollback risk |
| [CSR](glossary/06-architecture.md#csr) vs. [SSR](glossary/06-architecture.md#ssr) vs. [SSG](glossary/06-architecture.md#ssg) vs. [ISR](glossary/06-architecture.md#isr) | Browser rendering, request-time server rendering, build-time generation, and post-deployment static regeneration. | Freshness, SEO, infrastructure cost |
| [Preload](glossary/07-performance.md#preload) vs. [Prefetch](glossary/07-performance.md#prefetch) vs. [Preconnect](glossary/07-performance.md#preconnect) | Load a current critical resource, fetch a possible future resource, or prepare an origin connection. | Loading performance |
| [Cookie](glossary/05-web-browser.md#cookie) vs. [Local Storage](glossary/05-web-browser.md#local-storage) vs. [Session Storage](glossary/05-web-browser.md#session-storage) | Cookies can be attached to HTTP requests; local storage persists per origin; session storage is scoped to a tab's session. | Auth design, persistence, and security |
| [Unit Test](glossary/08-quality-tooling.md#unit-test) vs. [Integration Test](glossary/08-quality-tooling.md#integration-test) vs. [E2E Test](glossary/08-quality-tooling.md#e2e-test) | Test a small unit, multiple integrated parts, or a full user journey. | Choosing test scope and speed |

## Key reminder: naming is not a specification

Two design systems can use the same name for components with different dismissal rules, focus behavior, or visual presentation. Define the **behavioral contract** in your own product, and consult the corresponding platform or accessibility guidelines.

See [Practical Recipes](RECIPES.md) and [References](REFERENCES.md) for deeper implementation guidance.
