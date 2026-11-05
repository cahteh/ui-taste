# Tokens

Two parts. Founders is Folio's theme and is exact: use these values and names, never approximations. The generic tokens after it are Damir Sokolovsky's starting points from unslop, for client work and other products.

## Founders (Folio)

Source of truth: `src/themes/founders.ts` and `src/themes/index.ts` in the Folio repo. Views read these as theme tokens, never as hex values, so other themes can be added beside Founders.

| Token | Dark | Light | Use |
| --- | --- | --- | --- |
| bg | #0f0f10 | #f5f5f7 | page |
| side | #131315 | #fafafb | sidebar |
| panel | #17171a | #ffffff | framed panels |
| raised | #1d1d21 | #f2f2f5 | raised rows, menus |
| field | #141416 | #fafafb | inputs |
| active | #202024 | #ececf1 | active row |
| chip | #2a2a30 | #e4e4ea | chips, keycaps |
| line | #232327 | #e6e6ec | rules inside panels |
| border | #26262b | #e2e2e9 | control borders |
| frame | #2c2c32 | #cfcfd9 | panel frame |
| ink | #ededef | #202029 | primary text |
| soft | #c4c4cc | #3d3d48 | strong secondary |
| mid | #a3a3ad | #55555f | secondary text |
| navInk | #b4b4bd | #45454f | nav labels |
| muted | #8a8a95 | #5f5f6c | meta, icons |
| dim | #5a5a64 | #9a9aa6 | disabled, faint marks |
| green | #7fc29b | #287855 | positive |
| red | #e88f8f | #b44343 | negative |
| tintBg | #141a26 | #e8eefc | accent-tinted surface |
| tintLine | #26324a | #c9d6f5 | accent-tinted border |

- **Accent:** Clarity blue `#87a7f5` with `accentInk` #141414 (dark text on blue) in dark, white in light. The workspace owner may pick another accent; views read it from the theme.
- **Lab dot:** `#f2c94c` in dark, `#c99a06` in light.
- **Radius:** panel 12, control 8, chip 6.
- **Icons:** Phosphor paths from `src/shell/icons.ts`, one size and weight, colored by text role.
- **Type:** Instrument Sans for everything, weights 400 and 500, 600 rarely. `font-variant-numeric: tabular-nums` on every number. No monospace, no serif.
- **Shell:** sidebar with the workspace switcher, Search with a keycap, flat groups split by rules, Lab items with the yellow dot, the person at the bottom. Top bar with the sidebar toggle, breadcrumb, Ask Folio with its keycap, planner, help and notifications.
- **Shadow:** only on floating layers (menus, sheets): `0 12px 32px rgba(0,0,0,0.45)` dark, `0 12px 32px rgba(32,32,41,0.14)` light.
- **Motion:** hover and color changes 140 to 160ms ease-out; panels, sheets and slides 200 to 220ms `cubic-bezier(0.2, 0.7, 0.2, 1)`; one-time draw-ins up to 900ms. Everything has a reduced-motion version.

## Generic starting points

Starting values for each pass. When the project already has a good system, keep its values and only fix how they are used. These are starting points, not a house style, so let the direction move them.

### Spacing scale

4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96, 128

- Inside a control: 4 to 12
- Between related items, like rows in a list: 2 to 8
- Between groups, like a label and its list or two cards: 12 to 24
- Between sections: 32 to 64, landing sections 80 to 128
- Row heights: 32 compact, 36 default, 40 to 44 touch
- Hero: 96 to 128 from the navigation to the headline on desktop, 48 to 64 on mobile

### App layout

- Sidebar 240 to 280 wide, content fluid with page padding 24 to 32, capped around 1440 to 1600.
- Top bar or page header 56 to 64 tall.
- Navigation rows 32 to 36, gap 2 to 4, section labels 24 above and 8 below.
- Stat cards in a row share one height, usually 3 or 4 compact cards per row on desktop, numbers only.
- The main chart spans at least two thirds of the content width and is 280 to 360 tall. A second data block next to it is a list or table, narrower, not another chart.

### Neutral ramps

For apps and dashboards use graphite, or a ramp just as grey, for every surface. For landing pages pick the ramp whose tint matches the world in the direction. Warm suits paper, wood, food, craft and anything human. Ink suits night, sky, water and anything technical. You can tint your own ramp the same way, keeping saturation very low, so a surface never reads as a color on its own.

#### Dark

| Role | Graphite | Warm | Ink |
| --- | --- | --- | --- |
| Deepest surface, like a sidebar | #0f0f10 | #12110f | #07080d |
| Page background | #141415 | #161513 | #0b0d14 |
| Card | #19191b | #1c1a18 | #11141c |
| Raised, like an active row or input | #232325 | #262421 | #1a1e28 |
| Hairline | primary text at 8% | primary text at 8% | primary text at 8% |
| Primary text | #ededed | #efe9de | #eef0f5 |
| Secondary text | #a1a1a6 | #aaa398 | #a3a9b8 |
| Muted text and icons | #85858b | #8a847a | #7a8296 |

#### Light

| Role | Graphite | Warm | Ink |
| --- | --- | --- | --- |
| Page background | #fafafa | #f7f4ee | #f5f7fa |
| Card | #ffffff | #fdfbf7 | #ffffff |
| Raised, like an active row or input | #f4f4f5 | #efe9df | #eceff4 |
| Hairline | primary text at 8% | primary text at 8% | primary text at 8% |
| Primary text | #171717 | #1f1b16 | #111827 |
| Secondary text | #525252 | #5e554a | #4b5565 |
| Muted text and icons | #737373 | #7b7266 | #6b7487 |

Muted text is for meta and captions only and stays near 4.5 to 1 on its surface. Body text uses primary or secondary.

Semantic colors, toned to sit inside any ramp: positive #4cc38a on dark and #16a34a on light, negative #e5484d on dark and #dc2626 on light.

### Accent

- Keep a real brand color. A violet to blue or any other hue to hue glow gradient is slop, not a brand color, unless the user says otherwise.
- Without a brand color, take it from the world. Warm worlds suit amber, coral or ember orange. Cool worlds suit cobalt, teal or a clear sky blue. Natural worlds suit moss or sage. Avoid the purple to blue family unless the brand really is purple.
- Text on the accent reaches 4.5 to 1 contrast. Darken the accent or use dark text when it does not.
- The accent covers a few percent of the screen, like the primary action, the selection and one key figure.

### Buttons

- Hero buttons 44 to 48 tall, navigation buttons 32 to 36, padding 16 to 20 on the sides.
- Primary on dark: an off white from the ramp with dark text, or the accent. Primary on light: the primary text color as a fill with white text, or the accent.
- Secondary: the raised surface with a hairline, primary text.
- A soft top highlight like `inset 0 1px 0 rgba(255,255,255,0.12)` on dark buttons gives depth without a glow.

### Type families

Pick by the character in the direction. All of these are free. Carter avoids monospace unless the product is about code.

| Character | Interface family | Optional partner |
| --- | --- | --- |
| Precise, technical, calm | Geist, Inter, IBM Plex Sans | none, tabular figures instead of a mono |
| Warm, friendly, human | Instrument Sans, DM Sans, Figtree | Instrument Serif or Newsreader for the hero headline only |
| Editorial, literary, crafted | Inter or Instrument Sans for the interface | Newsreader, Instrument Serif or Fraunces for headlines |
| Playful, bold | Space Grotesk, Bricolage Grotesque | none |

A display serif belongs to large headlines only, never to labels or buttons.

### Type scale

| Use | Size | Line height | Weight |
| --- | --- | --- | --- |
| Small labels, meta, counts | 12 | 16 | 400, muted, tabular |
| Secondary text, captions | 13 to 14 | 20 | 400 |
| Body, nav items | 14 to 15 | 20 to 22 | 400 to 500 |
| Logo wordmark | 16 to 18 | 1 | 500 to 600 |
| Hero subhead | 18 to 20 | 28 to 30 | 400, secondary color, at most 36rem wide |
| Card figures | 28 to 32 | 1 | 500, tabular |
| Page title | 28 to 36 | 1.15 | 400 to 500 |
| Hero headline | 56 to 72 desktop, 36 to 44 mobile | 1.02 to 1.08 | 400 to 500 |

Letter spacing is 0 for anything under 16px, slightly positive like 0.01em is fine for small muted text. Display text from 40px can go to -0.02em, and from 56px to -0.03em.

### Radius

| Element | Radius |
| --- | --- |
| Keycap, tag, small button | 4 to 6 |
| Row, input, button | 8 to 10 |
| Card | 12 to 16 |
| Panel or window | 14 to 20 |

Nested radius: inner = outer − padding, never below 4. A 16px card with 8px padding holds items with an 8px radius.

### Icons

lucide, 16 or 18px, stroke 1.5, color of the muted or secondary text role, 8 to 10px gap to the label.

### Depth

- Dark: surface steps plus a hairline. An active row can carry `inset 0 1px 0 rgba(255,255,255,0.12)` as a top highlight.
- Light: `0 1px 2px rgba(0,0,0,0.05)` for small things, `0 8px 24px rgba(0,0,0,0.06)` for floating ones.

### Motion

One easing curve for everything, `cubic-bezier(0.22, 1, 0.36, 1)`.

| Use | Duration |
| --- | --- |
| Hover, press, toggles | 120 to 180ms |
| Menus, popovers, tooltips | 160 to 220ms |
| Entrances, sheets, layout changes | 300 to 500ms |
| Stagger between items | 40 to 60ms, at most six items |

- Rise distance on enter: 6 to 12px. Press scale: 0.97 to 0.98.
- Transition color, background, border, opacity and transform only.

---

The generic tokens are adapted by Carter Long from unslop by Damir Sokolovsky ([@heydamir](https://x.com/heydamir)), CC BY 4.0. Keep this credit in copies and adaptations.
