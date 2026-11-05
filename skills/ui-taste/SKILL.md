---
name: ui-taste
description: Carter Long's design review and polish pass for interfaces. Scores a screen on craft, design and content, finds what reads as unconsidered or AI-made, sets a direction, then fixes spacing, color, icons, copy, type, layout, details, visuals and motion in that order and scores it again. Use whenever the user asks to review, critique, score, polish, unslop, clean up or redesign a screen, page, board or mockup, asks whether something looks good or "has taste", or shares a screenshot of UI for feedback. Covers Folio (app.claritysoftware.ai, the Founders theme), client websites and design canvas boards. Works on React, Tailwind, HTML and CSS.
license: CC-BY-4.0
metadata:
  author: Carter Long
  adapted-from: unslop by Damir Sokolovsky (https://github.com/heydamir/unslop)
---

# UI taste

ui-taste is Carter Long's adaptation of unslop by Damir Sokolovsky ([@heydamir](https://x.com/heydamir)), licensed under CC BY 4.0. Keep both credits in any copy or adaptation.

A screen has taste when every size, color and word is a decision, when the chrome is quiet, and when the richness sits in the content people came for. A screen without taste spreads effort over the chrome, explains itself in callouts and could belong to any product.

The job has two halves. Removing what is unconsidered is the first half. The second is making a screen only this product could have. A clean screen that fits any product is the next template.

Work like a designer doing a redline pass, one layer at a time, across the whole screen. Judge with the rubric before and after, so the change is measured and not only felt.

## What good looks like

- **Bare and tactical.** Labels only where needed. No callout boxes, subtitles, helper notes or flavor text. Pages carry no title that repeats the breadcrumb. People use these screens for hours, so every line of text has to earn its place.
- **Quiet chrome.** Navigation, buttons and text use the neutral ramp and one accent. Panels are framed with hairlines, not shadows or glows.
- **One rich moment.** Each screen has one place that carries color and care: a chart drawn well, figures set beautifully, a painting, a real object, real content.
- **Human scale and order.** Structure on every scale, from the page grid down to the gap between an icon and its label, so the eye always finds the next level of order (see the rubric's harmony criteria).
- **Near perfect, not perfect.** Precision in the craft, a little life in the content. A screen that is sterile everywhere reads as a template.

## Which screen, which tokens

- **Folio**, the agency platform at app.claritysoftware.ai, and its design canvas boards: Founders theme. Use [references/tokens.md](references/tokens.md) exactly. Do not invent a direction. Founders is the direction, and new work fits inside it.
- **Client sites and other products:** derive a direction from the product, like unslop does, and use the generic ramps in tokens.md as a starting point. A real brand color, logo or typeface stays.

## Run it

1. **Look at the screen.** Find the files that render it, run it and take a screenshot, so you judge what people see and not only the code.
   - Only a link to a live site? `node <skill folder>/scripts/snapshot.mjs <url> taste/original.html` saves the page and a screenshot (`--dark` or `--light` to match the theme). Work on a copy.
   - Only a screenshot? Rebuild it as one static HTML file and treat that as the original.
2. **Score it.** Score the screen with [references/rubric.md](references/rubric.md). Note one line of evidence per criterion and apply the scale cap. This is the baseline.
3. **Audit.** Go through [references/signs.md](references/signs.md) and list every sign you find, one line each with where it lives.
4. **Decide how much to change.**
   - **Heavy**, many signs across color, type, icons and copy: run the full process.
   - **Light**, mostly designed with a few signs left: polish mode. Fix only what the audit found and keep the palette, type, layout and visual. Bigger ideas go into the report as suggestions.
   - **None**: say so plainly and suggest two or three refinements with exact values. Apply them only if the user agrees. Never change a good screen just to make it different.
5. **Set the direction and stop.** Write the five lines below, show the score, the audit and the direction, and wait for the user before editing. If you have a tool for asking questions, use it. Skip the wait only when the user said to just do it.
6. **Fix in nine passes, in order.** Finish a pass across the whole screen before the next. Spacing first, because everything reads differently once the rhythm is right. Copy before type and layout, because its length sets size and placement. Visuals and motion last.
7. **Check and score again.** Run the checklist, render again, compare with the audit and score with the rubric. Anything still on the audit list gets fixed.
8. **Report.** The before and after scores side by side, the direction, a few lines per pass, and suggestions you did not apply.

Render to check at most three times in a run.

## Direction

Five short lines, derived from what the product does and who uses it, never from what is trending.

- **Product.** What it does and for whom, in one plain sentence.
- **Character.** Two or three concrete words. Clean, modern, sleek, minimal and premium are not allowed, because they describe every template.
- **World.** The place or material the product belongs to. It sets the accent, the moments and the visual.
- **Moments.** One or two places that get rich color and detail, chosen from what the product shows.
- **Signature.** One small detail only this product would have, used consistently.

For Folio the direction is fixed, so restate it rather than invent one:

- **Product.** An agency platform where a small team runs leads, clients, schedule and messages from one place.
- **Character.** Calm, exact, a little old world.
- **World.** A working studio at night: maps, ledgers, a painting by the window.
- **Moments.** The Today figures, the pipeline, the schedule's now line, the painting on sign-in.
- **Signature.** The yellow Lab dot, and framed panels with a hairline.

## 1. Spacing

- Everything sits on a 4px grid. A 2px step is fine for nudges inside small controls.
- Same thing, same size. Rows in a list share one height and gap, cards in a row share one padding.
- Space shows grouping. Space inside a group is smaller than space between groups.
- Things line up. Icons in one column, labels on one line, numbers right aligned in one column.
- Padding follows density: sidebars and compact panels around 16, panels 20 to 24, page edges 24 to 32.
- Navigation rows 32 to 36 with 2 to 4 between them. A group rule sits closer to its own items than to the group above.
- Measure the sidebar after the pass. It is where spacing breaks most often.

## 2. Color

- One neutral ramp for surfaces, borders and text. On Folio this is Founders; nothing else.
- Three text roles in practice (ink, mid, muted), with soft and dim for the rare in-between.
- One accent, used rarely: the primary action, the selection, the one number that matters. On Folio, Clarity blue unless the workspace owner picked another.
- Views use theme tokens and never hardcoded colors, so another theme (Analog next) can sit beside Founders. A hex value in a view is a sign.
- Semantic colors only carry meaning, toned to sit in the ramp.
- No hue gradients, gradient text, glows, colored shadows or color washes. Depth on dark comes from surface steps and hairlines.

## 3. Icons

- One set, one size, one stroke. Folio uses Phosphor paths from `src/shell/icons.ts`; other projects use their own set, otherwise lucide.
- Icons take the color of their text role. They never get their own colors.
- Same icon box width in every row, fixed gap to the label.
- Drop icons that add nothing.

## 4. Copy

- Bare. Cut every line that explains the interface to the person using it: subtitles under titles, helper notes under fields, empty-state paragraphs, "Tip:" boxes. If a control needs a sentence to be understood, fix the control.
- No page title that repeats the breadcrumb. Today keeps its date and greeting, because they are content, not a title.
- Labels short and in sentence case. `Search`, not `Search anything...`.
- A change says what it compares to, like `+12% vs last month`.
- No exclamation marks, no trailing periods on labels and buttons, no hype words, no `AI-powered`.
- Lab and preview features are marked with the yellow dot or a small `Preview` tag, never with `Beta 🚀` or `New ✨`.
- Sample data is synthetic and plausible: real-looking names and amounts, never `[X]` or `123,456`.

## 5. Type

- Folio: Instrument Sans for everything. No monospace anywhere, not for figures, code-like meta or keycaps. No serif partner.
- Client work: one family for the interface plus at most one partner from tokens.md. Carter's preference still applies: avoid monospace unless the product is literally about code.
- A few sizes, weights 400 and 500, 600 at most for rare emphasis.
- Hierarchy from size and color, not weight.
- Sentence case everywhere. No uppercase tracked labels.
- Numbers use `tabular-nums` and one format across the screen.
- No negative tracking on small text. No italic for emphasis.

## 6. Layout

- Keep the sections and their order. Inside a section, alignment and proportions may change.
- Apps keep real app proportions: a sidebar around 240 to 264, fluid content, the page as long as its content.
- Panels are framed: panel surface, hairline border, the theme radius. A panel holds one kind of content.
- Flat grouped navigation: groups separated by a rule, no nested trees, no section headers unless the group is ambiguous.
- Detail opens in a side panel next to the list when the list is still useful, and as a route when it is not.
- On phones everything stacks in reading order, with a bottom tab bar and a More sheet. Nothing below 11px.
- Landing pages and client sites: a scene or an asymmetric split, text on calm space, one primary and one secondary action.

## 7. Details

- Nested radius: inner = outer minus padding, never below 4. On Folio: panel 12, control 8, chip 6.
- Counts and meta are quiet text, not pills.
- Keyboard shortcuts are small keycaps in the interface family.
- Charts on a muted grid, one accent per chart, one main chart per screen.
- Stat figures: a label, a big figure and a change with what it compares to. On Folio a small sparkline under a Today figure is allowed, because it shows that figure's own trend; an icon, a tally or decorative mini bars are not.
- Active state is a surface step with a hairline, not a glow.
- Hover and focus states exist and stay in the palette, with a visible focus ring.

## 8. Visuals

- Decorative filler goes: blobs, orbs, nebulas, glowing grids, robots.
- App screens almost never need generated images. Their moments come from the product itself.
- When a screen needs a picture (sign-in, empty states, a client hero), prefer a public-domain painting or a real photograph from the world over a generated scene. Credit the work on screen, quietly. How Folio picks and credits paintings is in [references/visuals.md](references/visuals.md).
- Look at [references/refs.md](references/refs.md) before this pass. Take qualities from the references, never their subject or layout.

## 9. Motion

- Motion is short and explains a change: a hover is a color or surface step, a panel slides from where it opens, a changed number tweens.
- Respect `prefers-reduced-motion`. Everything that moves has a reduced version that fades or does nothing.
- No loops on things that are not live, no `transition-all`, no `hover:scale` on cards, no bouncy springs.
- Transition color, background, border, opacity and transform only.
- Durations and curves from tokens.md.

## Story video

When the user wants something to share, `scripts/story.mjs` renders a short video of a screen fixing itself step by step. The method is unslop's, so read the Story video section of the original skill at https://github.com/heydamir/unslop before building one. Every video carries a small `unslop by @heydamir` credit, as the license asks.

## Do not

- Do not rename the product or redraw a real logo.
- Do not change what the product is, invent features, claims or data.
- Do not replace removed decoration with new decoration, or swap one trend for another.
- Do not add explanation where a better control would do.
- Do not let the scores drive the design. They measure the screen; the direction shapes it.

## Checklist

- [ ] Before and after scores are recorded with evidence, scale cap applied
- [ ] The direction is written and every pass follows it
- [ ] Every spacing value is on the 4px grid and equal things have equal sizes
- [ ] Icons, labels and numbers each sit in one aligned column
- [ ] One ramp, three text roles, one accent with enough contrast, tokens instead of hex in views
- [ ] No gradients, glows, colored shadows or washes
- [ ] No emoji, one icon set at one size and stroke
- [ ] No callouts, subtitles, helper notes or titles that repeat the breadcrumb
- [ ] Type in the right family, weights 400 to 600, sentence case, no monospace on Folio
- [ ] Numbers in one format with tabular figures
- [ ] Nested radii add up
- [ ] Motion is short, explains a change and has a reduced-motion version
- [ ] Template check: swap the product name for another product's. If the screen still fits, push the moments and the signature harder
