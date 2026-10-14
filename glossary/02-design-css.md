# Design & CSS

The visual language, layout mechanics, and responsive styling of web interfaces.

[← Home](../README.md) · [A–Z index](../INDEX.md) · [Comparisons](../COMPARISONS.md) · [Sources](../REFERENCES.md)


## Spacing, surfaces & typography

| Term | Definition | Example |
| --- | --- | --- |
| <a id="box-model"></a>**Box Model** | The CSS model describing content, padding, border, and margin areas. | Debugging an element's width |
| <a id="content-box"></a>**Content Box** | A box-sizing mode where declared width excludes padding and border. | box-sizing: content-box |
| <a id="border-box"></a>**Border Box** | A box-sizing mode where declared width includes padding and border. | box-sizing: border-box |
| <a id="margin"></a>**Margin** | Space outside an element's border. | margin-top: 16px |
| <a id="padding"></a>**Padding** | Space between an element's content and its border. | padding-inline: 12px |
| <a id="gap"></a>**Gap** | Space between items in a flex or grid layout. | gap: 1rem |
| <a id="border"></a>**Border** | The visible edge around an element's padding and content. | border: 1px solid |
| <a id="border-radius"></a>**Border Radius** | The curvature of an element's corners. | border-radius: 8px |
| <a id="shadow"></a>**Shadow** | A visual shadow cast around or inside a box. | box-shadow |
| <a id="elevation"></a>**Elevation** | A visual system suggesting surfaces at different depths. | Raised card surface |
| <a id="opacity"></a>**Opacity** | The degree to which an element is transparent. | opacity: 0.5 |
| <a id="typography"></a>**Typography** | The system for choosing and arranging typefaces, sizes, and spacing. | Body text at 16px |
| <a id="line-height"></a>**Line Height** | The height of a line box used for text layout. | line-height: 1.5 |
| <a id="letter-spacing"></a>**Letter Spacing** | The additional space inserted between characters. | letter-spacing: .02em |
| <a id="font-weight"></a>**Font Weight** | The thickness or weight of a typeface's strokes. | font-weight: 600 |
| <a id="color-palette"></a>**Color Palette** | A defined collection of colors used throughout a design. | Primary and neutral colors |
| <a id="contrast"></a>**Contrast** | The visual difference between elements, particularly foreground and background. | Readable text contrast |
| <a id="design-token"></a>**Design Token** | A named design decision represented as a reusable value. | --color-primary |
| <a id="spacing-scale"></a>**Spacing Scale** | A consistent set of allowed spacing values. | 4, 8, 12, 16 |

## Layout & positioning

| Term | Definition | Example |
| --- | --- | --- |
| <a id="flexbox"></a>**Flexbox** | A CSS layout system that aligns items along a main and cross axis. | Horizontal button row |
| <a id="grid"></a>**Grid** | A CSS layout system for arranging items in rows and columns. | Responsive card grid |
| <a id="inline"></a>**Inline** | A display mode that flows within a line of text. | display: inline |
| <a id="block"></a>**Block** | A display mode that creates a block-level box. | display: block |
| <a id="inline-block"></a>**Inline-block** | An inline-level box that can take explicit dimensions. | display: inline-block |
| <a id="position-relative"></a>**Position Relative** | Positioning that offsets an element relative to its normal position. | position: relative |
| <a id="position-absolute"></a>**Position Absolute** | Positioning removed from normal flow and placed relative to a containing block. | Badge over an image |
| <a id="position-fixed"></a>**Position Fixed** | Positioning anchored to a fixed containing block, commonly the viewport. | Floating support button |
| <a id="position-sticky"></a>**Position Sticky** | Positioning that sticks to a threshold while staying within its scroll container. | Sticky section heading |
| <a id="z-index"></a>**Z-index** | A property controlling stack order within a stacking context. | Popup above content |
| <a id="stacking-context"></a>**Stacking Context** | A group whose descendants are stacked independently of outside elements. | Unexpected overlay ordering |
| <a id="overflow"></a>**Overflow** | How content extending beyond an element's box is handled. | overflow: auto |
| <a id="viewport"></a>**Viewport** | The visible area used to display a web page. | Mobile browser viewport |

## Responsive design

| Term | Definition | Example |
| --- | --- | --- |
| <a id="breakpoint"></a>**Breakpoint** | A condition at which a responsive design changes layout. | Two columns above 768px |
| <a id="media-query"></a>**Media Query** | A conditional CSS rule based on media or user-environment features. | @media (min-width: 768px) |
| <a id="container-query"></a>**Container Query** | A CSS rule based on a container's size or style rather than the viewport. | Adaptive sidebar card |
| <a id="responsive-design"></a>**Responsive Design** | A design approach that flexibly adapts to available space. | Fluid columns |
| <a id="adaptive-design"></a>**Adaptive Design** | A design approach that selects among intentionally defined layouts. | Separate mobile and desktop layouts |
| <a id="aspect-ratio"></a>**Aspect Ratio** | The proportional relationship between width and height. | aspect-ratio: 16 / 9 |

## CSS rules & units

| Term | Definition | Example |
| --- | --- | --- |
| <a id="specificity"></a>**Specificity** | A part of the CSS cascade used to prioritize competing selectors. | ID versus class selectors |
| <a id="cascade"></a>**Cascade** | The CSS process for resolving competing declarations using origin, importance, layers, specificity, and order. | Why a rule wins |
| <a id="inheritance"></a>**Inheritance** | The propagation of certain CSS property values from parent to child. | Inherited text color |
| <a id="pseudo-class"></a>**Pseudo-class** | A selector matching a state or structural condition of an element. | :hover or :focus-visible |
| <a id="pseudo-element"></a>**Pseudo-element** | A selector addressing a represented part of an element. | ::before |
| <a id="css-variable"></a>**CSS Variable** | A CSS custom property that can be reused with var(). | --space-md |
| <a id="logical-properties"></a>**Logical Properties** | CSS properties expressed relative to writing direction and flow. | margin-inline-start |
| <a id="unit-px"></a>**Unit px** | A CSS pixel, the standard reference-length unit. | width: 320px |
| <a id="unit-rem"></a>**Unit rem** | A length relative to the root element's font size. | padding: 1rem |
| <a id="unit-em"></a>**Unit em** | A length relative to the relevant element's font size, depending on property. | font-size: 1.2em |
| <a id="unit-vwvh"></a>**Unit vw/vh** | Units equal to 1% of the viewport width or height. | width: 100vw |
| <a id="unit-dvh"></a>**Unit dvh** | A unit based on the dynamic viewport height. | min-height: 100dvh |
| <a id="object-fit"></a>**Object-fit** | How replaced content fits inside its allocated box. | object-fit: cover |
| <a id="css-reset"></a>**CSS Reset** | Styles that remove or standardize browser defaults. | Reset margin and padding |
| <a id="utility-first-css"></a>**Utility-first CSS** | A styling approach built from small, single-purpose classes. | Tailwind utilities |
| <a id="bem"></a>**BEM** | Block Element Modifier; a naming convention for CSS classes. | card__title--large |

For related articles and official documentation, see [References](../REFERENCES.md).
