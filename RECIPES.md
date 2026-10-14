# Practical Frontend Recipes

> [← Home](README.md) · [Interaction](glossary/03-interaction.md) · [State & Data](glossary/04-state-data.md)

These recipes connect glossary concepts to common problems. They describe **patterns and trade-offs**, not production-ready drop-in implementations.

## 1. Search as you type: debounce + stale-response protection

**Problem:** Calling an API for every keystroke wastes bandwidth, and earlier requests may finish after newer ones.

**Approach:**
1. Debounce the input event (for example, a 250–400 ms delay).
2. Cancel a prior supported request with `AbortController`, or ignore responses that do not match the latest request identifier.
3. Show an explicit loading and empty-result state; handle errors separately.

**Related terms:** [Debounce](glossary/03-interaction.md#debounce), [AbortController](glossary/04-state-data.md#abortcontroller), [Race Condition](glossary/04-state-data.md#race-condition), [Empty State](glossary/01-ui-ux.md#empty-state).

## 2. Scroll-heavy pages: throttle, animation frames, and observers

**Problem:** Scroll and pointer events may fire far more frequently than complex code can safely run.

**Approach:**
- Use a throttle when you need a bounded update rate.
- Use `requestAnimationFrame` for work synchronized with visual updates.
- Prefer `IntersectionObserver` over repeated scroll-position calculations when only visibility matters.
- Avoid unnecessary layout reads after writes, which can cause layout thrashing.

**Related terms:** [Throttle](glossary/03-interaction.md#throttle), [requestAnimationFrame](glossary/07-performance.md#requestanimationframe), [Intersection Observer](glossary/05-web-browser.md#intersection-observer), [Layout Thrashing](glossary/07-performance.md#layout-thrashing).

## 3. Prevent double submissions: in-flight guard + server idempotency

**Problem:** Double taps, network retries, multiple tabs, and duplicate clients may all submit the same purchase.

**Safe design:**
1. Immediately mark the UI as submitting and block accidental resubmission.
2. Reuse a unique **operation key** for retries of the *same logical transaction*.
3. Implement and enforce idempotency on the server. A client-side delay does **not** guarantee safety.
4. Distinguish successful completion from an unknown result after a timeout; confirm status before starting a new transaction.
5. Restore an accessible error/retry state when appropriate.

```text
User presses "Pay"
  → UI: submitting = true
  → Request: POST /payments (Idempotency-Key: same-operation-key)
  → Server: process the operation at most once per key
  → UI: show confirmed result; handle uncertain outcome separately
```

**Related terms:** [Double-submit Guard](glossary/03-interaction.md#double-submit-guard), [Cooldown](glossary/03-interaction.md#cooldown), [Idempotency](glossary/04-state-data.md#idempotency), [Retry](glossary/04-state-data.md#retry), [Race Condition](glossary/04-state-data.md#race-condition).

## 4. Data fetching: cache, revalidation, and optimistic updates

**Problem:** Refetching everything is slow, but stale cache entries can mislead users.

**Approach:**
- Cache data using keys that reflect the actual query.
- Use stale-while-revalidate for screens where slightly old data is acceptable.
- Invalidate or update relevant cached queries after a successful mutation.
- For optimistic updates, snapshot the previous state and roll back on failure.
- Prefer confirmed server results for irreversible or highly sensitive changes.

**Related terms:** [Cache Invalidation](glossary/04-state-data.md#cache-invalidation), [Stale-While-Revalidate](glossary/04-state-data.md#stale-while-revalidate), [Optimistic Update](glossary/04-state-data.md#optimistic-update), [Rollback](glossary/04-state-data.md#rollback).

## 5. Very large lists: pagination + virtualization + lazy loading

**Problem:** Thousands of rows and images increase network, DOM, layout, and memory costs.

**Approach:**
- Fetch bounded pages, often with cursor pagination.
- Render only visible/nearby rows when the DOM gets large.
- Lazy-load offscreen images and serve responsive image sizes.
- Keep keyboard navigation and screen-reader behavior usable.

**Related terms:** [Cursor Pagination](glossary/04-state-data.md#cursor-pagination), [Virtualization](glossary/07-performance.md#virtualization), [Lazy Loading](glossary/07-performance.md#lazy-loading), [Responsive Images](glossary/07-performance.md#responsive-images).

## 6. Accessible overlays: dialog, focus management, and announcements

**Problem:** An overlay appears visually correct but is unusable from a keyboard or screen reader.

**Approach:**
- Give the dialog an accessible name and suitable semantics.
- In a modal dialog, keep focus inside while open, then restore focus appropriately on close.
- Provide an obvious dismiss action; follow the component's documented Escape-key behavior.
- Announce meaningful dynamic feedback to assistive technologies without spamming notifications.

**Related terms:** [Dialog](glossary/01-ui-ux.md#dialog), [Modal](glossary/01-ui-ux.md#modal), [Focus Trap](glossary/03-interaction.md#focus-trap), [Accessible Name](glossary/08-quality-tooling.md#accessible-name), [ARIA](glossary/08-quality-tooling.md#aria).

## 7. SSR interfaces: avoid hydration mismatches

**Problem:** The server renders different text or structure from the browser's first render.

**Approach:**
- Use deterministic initial content on server and client.
- Do not assume browser-only APIs, local storage, random numbers, or local time are identical during server rendering.
- Move environment-specific display changes to an appropriate client-only phase if needed.

**Related terms:** [SSR](glossary/06-architecture.md#ssr), [Hydration](glossary/06-architecture.md#hydration), [Hydration Mismatch](glossary/04-state-data.md#hydration-mismatch).

## Further reading

- [CSS-Tricks: Debouncing and Throttling](https://css-tricks.com/debouncing-throttling-explained-examples/)
- [MDN: AbortController](https://developer.mozilla.org/en-US/docs/Web/API/AbortController)
- [Stripe: Idempotent requests](https://docs.stripe.com/api/idempotent_requests)
- [WAI-ARIA: Modal dialog pattern](https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/)
- [web.dev: Learn Performance](https://web.dev/learn/performance)
