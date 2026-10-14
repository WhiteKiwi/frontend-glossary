# Contributing to Frontend Glossary

Thanks for helping make frontend vocabulary clearer. Contributions of all sizes are welcome: new terms, corrected definitions, examples, cross-links, and primary sources.

## Editorial rules

1. **Use English throughout the repository.** Term labels should use widely recognized English names, and definitions and examples must also be in English.
2. **Be concise and concrete.** Prefer a one-sentence definition plus a short real-world example.
3. **Choose one primary category.** Cross-reference other categories when the concept overlaps.
4. **Differentiate similarly named terms.** Note when component naming depends on a particular platform or design system.
5. **Ground uncertain claims.** Add a reliable reference, preferably official documentation or a standard.
6. **Avoid copy/paste.** Write original summaries instead of reproducing large sections of external articles.
7. **Respect security and accessibility implications.** Avoid presenting UI-only prevention as a guarantee of server-side safety.

## Adding a glossary term

Add a new row beneath the appropriate subsection in `glossary/*.md`:

```md
| <a id="debounce"></a>**Debounce** | Delay execution until a quiet period follows the latest event. | Search input |
```

Use a unique, lowercase, hyphenated anchor based on the term. For example, `Bottom Sheet` uses `bottom-sheet`.

Update the [A–Z index](INDEX.md) and the term count in [README.md](README.md). If the term changes a comparison or implementation recommendation, update [COMPARISONS.md](COMPARISONS.md) or [RECIPES.md](RECIPES.md). New source material belongs in [REFERENCES.md](REFERENCES.md).

## Style guide

- Write **JavaScript**, **TypeScript**, **CSS**, **HTTP**, and other canonical names with conventional capitalization.
- Expand less-common acronyms in the definition.
- Explain *what* a concept means; use the example to show *when* it is useful.
- Avoid assuming one framework or component library defines every frontend convention.
- Keep links relative for files inside this repository.
- Preserve Markdown table structure and avoid unescaped pipe characters (`\\|`) in cells.

## Pull request checklist

- [ ] The definition is accurate and understandable on its own.
- [ ] The example illustrates a genuine use case.
- [ ] Similar terms are distinguished or cross-linked.
- [ ] The new term has an anchor and is linked from `INDEX.md`.
- [ ] The total in `README.md` is up to date.
- [ ] Markdown renders correctly and links resolve.
- [ ] External sources are cited where relevant.

For discussion or uncertain terminology, start with an [issue](https://github.com/WhiteKiwi/frontend-glossary/issues).
