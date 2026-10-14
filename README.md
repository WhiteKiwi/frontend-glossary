<div align="center">

# Frontend Glossary

**A practical, English-language glossary for frontend engineering and UI/UX collaboration.**

From **Navbar**, **Toast**, **Hero**, and **Bottom Sheet** to **Debounce**, **Throttle**, **Hydration**, and **Core Web Vitals**.

[![Terms](https://img.shields.io/badge/terms-393-2563eb)](INDEX.md)
[![Categories](https://img.shields.io/badge/categories-8-0f766e)](#browse-by-category)
[![Language](https://img.shields.io/badge/language-English-334155)](#about)
[![Contributions](https://img.shields.io/badge/PRs-welcome-brightgreen)](CONTRIBUTING.md)

[Browse topics](#browse-by-category) · [A–Z index](INDEX.md) · [Commonly confused terms](COMPARISONS.md) · [Practical recipes](RECIPES.md) · [References](REFERENCES.md)

</div>

---

## About

Frontend development has a vocabulary spanning **visual UI components**, **CSS**, **user interactions**, **JavaScript and browser internals**, **state and network behavior**, **architecture**, **performance**, and **quality practices**.

This repository collects **393 terms** across **eight topic areas**. Every entry has a concise definition and a practical example. It is designed for developers, designers, QA engineers, and anyone discussing frontend implementations.

**Use it as a quick reference, not as a replacement for specifications.** Names and implementation details sometimes vary across design systems, platforms, and frameworks. The [reference library](REFERENCES.md) links to primary documentation and curated learning material.

## Browse by category

| Category | What's inside | Terms |
| --- | --- | ---: |
| 🧩 [UI & UX](glossary/01-ui-ux.md) | Interface components, navigation, forms, and product patterns | 62 |
| 🎨 [Design & CSS](glossary/02-design-css.md) | Typography, spacing, layouts, responsive CSS, and tokens | 54 |
| 🖱️ [Interaction](glossary/03-interaction.md) | Events, gestures, states, timing controls, and motion | 45 |
| 🔄 [State & Data](glossary/04-state-data.md) | State management, APIs, caching, concurrency, and updates | 45 |
| 🌐 [Web & Browser](glossary/05-web-browser.md) | JavaScript, DOM, browser APIs, HTTP, and storage | 48 |
| 🏗️ [Architecture](glossary/06-architecture.md) | Component patterns, rendering strategies, and system design | 45 |
| ⚡ [Performance & Optimization](glossary/07-performance.md) | Core Web Vitals, loading, rendering, and memory | 44 |
| ✅ [Quality, Security & Tooling](glossary/08-quality-tooling.md) | Accessibility, SEO, testing, security, and build tools | 50 |
| **Total** | **English definitions and usage examples** | **393** |

> **Looking for a specific term?** Use the [A–Z index](INDEX.md), or search this repository with GitHub search.

## Quick examples

| You want to know… | Start with |
| --- | --- |
| What is the main menu at the top of a page called? | [Navbar](glossary/01-ui-ux.md#navbar), [GNB](glossary/01-ui-ux.md#gnb), [LNB](glossary/01-ui-ux.md#lnb) |
| What's the bottom-up panel on mobile? | [Bottom Sheet](glossary/01-ui-ux.md#bottom-sheet), [Drawer](glossary/01-ui-ux.md#drawer), [Modal](glossary/01-ui-ux.md#modal) |
| How do short-lived feedback messages differ? | [Toast](glossary/01-ui-ux.md#toast), [Snackbar](glossary/01-ui-ux.md#snackbar), [Alert](glossary/01-ui-ux.md#alert) |
| How do I make rounded cards and responsive layouts? | [Border Radius](glossary/02-design-css.md#border-radius), [Flexbox](glossary/02-design-css.md#flexbox), [Grid](glossary/02-design-css.md#grid) |
| How do I avoid unnecessary search requests? | [Debounce](glossary/03-interaction.md#debounce), [AbortController](glossary/04-state-data.md#abortcontroller) |
| How do I handle double-clicks or duplicate payments? | [Throttle](glossary/03-interaction.md#throttle), [Double-submit Guard](glossary/03-interaction.md#double-submit-guard), [Idempotency](glossary/04-state-data.md#idempotency) |
| How do rendering strategies compare? | [CSR](glossary/06-architecture.md#csr), [SSR](glossary/06-architecture.md#ssr), [SSG](glossary/06-architecture.md#ssg), [Hydration](glossary/06-architecture.md#hydration) |
| Which metrics describe perceived performance? | [LCP](glossary/07-performance.md#lcp), [INP](glossary/07-performance.md#inp), [CLS](glossary/07-performance.md#cls) |

## Explore beyond definitions

- **[A–Z Term Index](INDEX.md)** — find any of the 393 entries by name and jump to its definition.
- **[Commonly Confused Terms](COMPARISONS.md)** — compare similar concepts and understand when to use each.
- **[Practical Recipes](RECIPES.md)** — common implementation problems, including double-submission safety and async races.
- **[References](REFERENCES.md)** — original docs, design systems, and reputable articles.
- **[Contributing](CONTRIBUTING.md)** — suggest a term, improve a definition, or submit a correction.

## Organization principles

1. **One primary category per term.** Related terms are cross-linked when helpful; some concepts naturally span multiple areas.
2. **Plain-English explanations first.** Short definitions should be accessible without diluting technical accuracy.
3. **Examples over buzzwords.** Each entry includes at least one concrete use case.
4. **Names are contextual.** A *Toast* in one design system may be called a *Snackbar* in another.
5. **Correctness matters.** Browser behavior, security-sensitive flows, and standards should defer to the linked official documentation.

## Contributing

Spotted a missing term or an ambiguous definition? Open an [issue](https://github.com/WhiteKiwi/frontend-glossary/issues) or submit a pull request after reading the [contributing guide](CONTRIBUTING.md).

---

<p align="center">Built as a community-friendly reference for frontend developers.</p>
