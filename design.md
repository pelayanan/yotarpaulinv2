# YO TERPAL NUSANTARA RAYA — locked design system

Locked by a Hallmark `redesign` run (full depth, brand kept). Every page of
`yoterpal.com` and `v2.yoterpal.com` reads this file. Pages share the theme, the
type and the accent, and differ only in shape.

## Files

| File | Holds |
| --- | --- |
| `assets/css/tokens.css` | every colour, face, space and duration. No literal colour past this file. |
| `assets/css/base.css` | what the Floor decided: reset, `overflow-x: clip`, focus ring, display heads, container, reduced motion. |
| `assets/css/site.css` | the components: stamp, strip, masthead, opening, ladder, colophon, wa. Every page class lives here. |
| `assets/css/styles.scss` | the old system. Still linked for pages not yet rebuilt, shrinking as pages migrate. Never add to it. |

Loaded in `_includes/head.html` in this order: `styles.css`, `tokens.css`,
`base.css`, `site.css`. Later files win on equal specificity.

## Palette

| Token | Value | Use |
| --- | --- | --- |
| `--color-paper` | `#f5f9fe` | page ground |
| `--color-paper-2` | `#eaf3fc` | inset ground, table track |
| `--color-paper-3` | `#ffffff` | raised surface |
| `--color-ink` | `#12263f` | body text |
| `--color-ink-2` | `#072a5c` | figures, secondary head |
| `--color-muted` | `#4a6075` | captions, labels |
| `--color-rule` | `#cfdeee` | hairlines |
| `--color-accent` | `#ff8a1f` | the one primary action per screen |
| `--color-accent-ink` | `#041630` | text on the accent |
| `--color-deep` | `#041630` | the dark band (strip, colophon) |
| `--color-focus` | `#0f4ba3` | focus ring on light |
| `--color-focus-deep` | `#ff8a1f` | focus ring on the dark band |
| `--prod-*` | seven values | the tarpaulins' own colours, from `_data/products.yml` |

The navy scale and the orange are the brand's, read from the old `styles.scss`;
they are not restyled. The `--prod-*` set is new and is material, not brand.

## Type

- Display: **Barlow Condensed 700**, headings only. Uppercase is the brand's voice; keep it for `h1`/`h2` display heads.
- Body: **Plus Jakarta Sans 400 / 600**. Three weights in total. Never a fourth.
- Labels, captions, table heads and nav links are the body face, one step smaller, sentence case, untracked. Never tracked capitals, never an eyebrow.
- Body never below 16px. Running text 13px only for figures and labels.

## Shape

Square by default: `--radius-card: 3px`. Hairlines instead of shadows
(`--shadow-card: none`). One primary button (`.act`), one quiet variant
(`.act--quiet`). One container (`--container: 1440px`), gutters grow at 1920.
Bands are separated by a hairline and `--section-gap`, never by colour alone.

## Rules every remaining page follows

1. No eyebrow above a heading. The plain label becomes the heading.
2. No coloured word inside a heading.
3. No emoji as an icon; the language pair is the text `ID` / `EN`.
4. No card inside a card, no floating badge over a photograph.
5. A number or range is only printed if it is in the page's own content. The
   catalogue's GSM ranges are real; nothing else is invented.
6. Every value that repeats the catalogue (GSM, size) is set in tabular figures.
7. The action sits where the page's job puts it, and the page ends on it.

## Contract kept from the old site

Front matter (`layout`, `permalink`, `lang`, `lang_other`, `title`,
`description`, `image`), the include/layout split, `#wa-form` and the field
names `nama` / `kebutuhan` / `jumlah` / `lokal` / `pesan` read by `main.js`,
every product slug, and the EN mirror at 1:1.
