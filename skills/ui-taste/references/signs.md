# Signs

Go through every group and note each sign you find with where it lives. Each line pairs the sign with its fix. The first group is Carter's own; the rest are Damir Sokolovsky's signs of slop from unslop, with a few changed to fit Carter's taste.

## Carter's signs

- A callout box, tip, banner or info panel explaining the screen → remove, fix the control that needed explaining
- A subtitle under a page or panel title → remove
- A panel title that repeats the section or breadcrumb → remove or name what is inside
- Several Save buttons in one view, or different labels for the same action → one save per view, one label
- Read-only values styled like editable fields → plain text
- A status dot with no label → dot plus a short label
- Helper text under form fields that restates the label → remove, keep only a real constraint like a format or limit
- Empty-state paragraphs → one short line, or the action itself
- A page title that repeats the breadcrumb → remove the title
- Flavor text, taglines or encouragement inside an app → remove
- Monospace anywhere, for figures, meta, IDs or keycaps → the interface family with tabular figures
- Hardcoded colors in a view, like `#87a7f5` or `rgb(...)` → a theme token
- Nested navigation trees or section headers in the sidebar → flat groups separated by a rule
- A panel without a frame floating on the page, or a card with a shadow on dark → panel surface, hairline border, theme radius
- A modal for something people keep open while they work → a side panel
- Two places to change the same setting → one place
- Motion with no reduced-motion version → add one that fades or does nothing
- Lab or preview features shown as if they were live → the yellow Lab dot or a `Preview` tag
- Real people's names, numbers or emails in sample data → synthetic data

## Surfaces and color

- Purple to blue or violet to pink gradients on backgrounds, cards, buttons or the active nav item → one neutral surface, accent only where it means something
- Gradient text in headings, numbers or the logo → solid primary text color
- Colored glows, like `shadow-[0_0_20px_rgba(139,92,246,0.5)]`, `drop-shadow` on emoji or glowing pills → remove, depth from surface steps and hairlines
- Radial color washes or blurred blobs behind content → remove
- Neon or high contrast colored borders → hairline at 6 to 10% opacity
- Many near identical tints of the same hue for text, like five lavenders → three text roles from one neutral ramp
- Every element highlighted, so nothing stands out → one accent used once or twice per screen
- Glass cards with a white inner highlight and a colored shadow → plain raised surface with a hairline

## Type

- Headings at weight 800 or 900 → 400 to 500 and size for hierarchy
- Uppercase labels with wide tracking, like `NAVIGATION` or `PAID THIS MONTH` → sentence case at normal or slightly open tracking
- Too many sizes and weights on one screen → a few sizes from the scale, weights 400 and 500
- Numbers in mixed formats, like `$48,210` next to `$124,860.40`, or `07` → one format, tabular figures
- Negative letter spacing on small text → zero or slightly positive
- Italic used for emphasis → color or weight instead

## Icons

- Emoji as nav icons, label decoration or status, like 🏠 📥 🚀 💰 ⚠️ 📈 🔥 😬 → one line icon set or nothing
- Emoji inside pills and counts, like `18 👤` → plain number
- Icons in many sizes and colors → one size, one stroke, text role color
- Icons nudged off the column → same icon box width in every row
- A sparkle ✨ for anything AI → remove or use a plain icon only where it explains something

## Spacing

- Arbitrary values, like `mt-[13px]`, `ml-[7px]`, `h-[31px]` → steps on the 4px scale
- Rows in one list with different heights or gaps → one height, one gap
- Groups that sit closer to their neighbours than to their own items → smaller gaps inside groups, bigger between them
- Uneven padding inside sibling cards → one padding
- Big empty gaps above a section and cramped space below it → balanced rhythm

## Copy

- Chatty greeting headlines, like `Welcome back, Damir! 👋` → the page or period as the title. A plain greeting under the date on a home screen, like Folio's Today, may stay
- Exclamation marks and `!!` → plain statement
- Changes without a reference, like `+12%!!` or `3 less!!` → `+12% vs last month`, `3 fewer vs last month`
- Wordy placeholders, like `Search anything...` → `Search`
- Hype words, like supercharge, seamless, unlock, magic, revolutionize → what the thing actually does
- Trailing periods on labels and buttons → none
- Fake looking data, like `$123,456` or `[X]` → plausible numbers

## Components

- Glowing pills for counts, plans, shortcuts or status → quiet muted text or a keycap
- `PRO`, `New ✨`, `Beta 🚀` badges everywhere → remove or one quiet text badge
- Every element a full pill, from search to buttons to cards → radius by size, nested radius math
- Charts with rainbow bars, glowing bars, pill shaped bars or uppercase day labels → one or two series, muted grid and muted labels, one highlight color
- Every chart or stack in several shades of the accent, so nothing leads → neutral steps with the accent only on the one thing that matters
- Tallies, icons or decorative mini bars added to stat cards → the number, its label and its change. A small sparkline of that figure's own trend may stay
- Equal cards side by side, each with the same chart or layout → one main chart, compact stats, varied widths
- Logo as a gradient tile with a sparkle and a gradient wordmark → product name as text plus a simple flat mark
- Logo mark as a glossy orb, a gradient ball or a glowing dot → a flat glyph in one solid color, or the wordmark alone

## Landing pages and heroes

- A pill badge above the headline, like `✨ Introducing X 2.0` → remove, or a quiet text link if it is real news
- A headline that could fit any product, like `Supercharge your workflow with AI` → say what the product does for whom
- Gradient or shimmer on the headline → solid text
- Floating blobs, orbs, grids and glowing lines behind the hero → plain background or one real product visual
- Everything stacked and centered, headline, text, buttons and a picture below → an asymmetric split or text over a large product view, see the Layout pass
- Three or more buttons, or chips and avatars stacked under the buttons → one primary and at most one secondary action
- `Trusted by 10,000+ teams`, `Loved by 10,000+`, rows of avatar dots or five stars without a source → ask if it is real, then make it quiet and specific or remove it
- Parallax and elements floating on scroll → static layout, motion only with a purpose
- Feature cards with an emoji, a bold title and a vague line each → fewer features, concrete copy, line icons or none

## Visuals

- Glossy 3D blobs, orbs, liquid chrome shapes or a purple nebula as the hero visual → the product itself or one concrete metaphor for what it does
- Stock robots, glowing brains, circuit lines or holograms for anything AI → remove, or show what the AI actually produces
- Text, fake buttons or a fake logo baked into an image → real text in the page, a clean image without text
- An image that does not blend into the page, with a hard edge and a different black → background matched to the page and a soft mask at the edges
- A visual on every section → one visual where it helps, usually only the hero

## Motion

- `animate-pulse`, `animate-ping` or breathing glows on things that are not live → static
- `transition-all` and `hover:scale` on cards and buttons → color or surface step on hover, a tiny scale down on press
- Bouncy springs and overshoot on simple UI → one ease-out curve
- Everything flying in on load from different directions → one short fade and rise with a small stagger
- Parallax, floating loops and elements that move on scroll → static layout
- Animating width, height, top or left → transform and opacity

## Template look

These are not slop, but they are what a cleaned up screen falls back to when nobody made a decision. Watch for them after the passes.

- Pure grey #161616 page, Inter, white text and the old brand color on one button, on a product whose world is warm or bright → a ramp tinted toward the world and an accent from it
- A headline that would fit another product if you swapped the name → say what this product does, with its own nouns
- A hero visual that is an empty box or a generic picture → a product preview in code or an image from the world
- Every product getting the same layout, type and palette → let the direction choose

---

Adapted by Carter Long from unslop by Damir Sokolovsky ([@heydamir](https://x.com/heydamir)), CC BY 4.0. Keep this credit in copies and adaptations.
