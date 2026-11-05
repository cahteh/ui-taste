# Rubric

Carter Long's "Adjudicating Beauty" framework, turned into questions about an interface. Score before the passes and again after. The score measures the screen; the direction shapes it. Never change a screen only to raise a number.

## The idea

Beauty is a signal of fertility: a thing looks beautiful when it shows that it could make more good things, that it is alive, cared for and able to grow. Three ways a screen can show it:

- **Craft = medium × execution.** Is it made of good material, and made well?
- **Design = temperature × harmony.** Is there enough life in it, and is that life ordered? (After Nikos Salingaros.)
- **Content = resonance × value.** Does it reach the person, and is it worth reaching them with?

Each is a product, not a sum. A beautifully executed screen in the wrong medium is still weak. A warm screen with no order is noise. A legible screen that says nothing is empty.

Two more ideas from the framework. Work built to human scale reads as right, so sizes, densities and touch targets follow the hand and the eye. And the sublime, magnitude beyond what we can take in at once, belongs to a few moments like a painting or a huge figure, never to chrome.

Near perfect beats perfect. A screen with every value exact and no life left in it scores high on execution and low on temperature, and should.

## How to score

Score each criterion 0 to 4.

- **0** absent or actively wrong
- **1** weak, a few accidental good moments
- **2** adequate, what a careful template gives
- **3** good, clearly decided
- **4** exceptional, you would show it to someone

Write one line of evidence for each score: what you saw and where. A score with no evidence does not count.

Scores are calibrated low on purpose. All 2s give a pillar of 25 and all 3s give 56, so read pillars like this: under 30 template or worse, 30 to 50 careful, 50 to 70 clearly designed, over 70 rare.

**Template cap.** Run the template check from SKILL.md. If the screen would still fit another product with the name swapped, cap T4, T5, R3 and V3 at 2.

Each pillar is the product of its two halves, each half the mean of its criteria, normalised to 0 to 100: `pillar = (mean(first) / 4) × (mean(second) / 4) × 100`. Report all three pillars and their mean as the overall score.

## Scale cap

Order has to exist on human scales. Count k, the number of distinct scale levels the eye picks out on the screen at one viewing distance, like panel → row → label. Count levels that are clearly different in size, not every element.

If k is outside 2 to 5, cap T1, T2, H1 and H2 at half marks (2 of 4). One level reads as blank, six or more as noise. Say in the report that the cap applied and how you counted.

## Craft: medium

**M1 Quality.** Is the material authentic and hard to fake? On a screen: real data shapes, a real typeface used well, real images or paintings rather than stock, components that would survive real content (long names, empty states, errors). Low: lorem ipsum, stock illustrations, one-size-fits-all components.

**M2 Suitability.** Is the medium right for the job? Dense tables for dense work, a side panel where the list stays useful, a phone layout that is a phone layout and not a shrunken desktop. Low: a card grid for something that should be a table, a modal for something people keep open.

## Craft: execution

**E1 Mastery.** Precision, and keeping entropy out. Spacing on the grid, alignment to one column, nested radii, numbers in one format, no stray values. Count the defects; three or more visible ones cap this at 2.

**E2 Integrity.** Structural soundness and reliability. It holds under real conditions: loading, empty, error, long names, slow networks, both themes. Controls that look clickable are clickable, preview features are marked as preview, a sandbox never reaches real people. Low: dead buttons, layouts that break on real data, a screen that only works with the demo.

**E3 Endurance.** Will it still hold in a year, and under load? Tokens instead of hardcoded colors, so themes can be added. Layout that survives 10× the data. Style that is not this season's trend. Low: glassmorphism, neon, anything that dates the screen to a month.

## Design: temperature

Temperature is how much perceivable life the screen carries. Too cold reads as sterile; too hot reads as noise. Score how well the temperature fits the screen's job, not the raw amount: a dense data table should run cooler than a sign-in page.

**T1 Detail intensity.** Is there detail to find at each distance? From across the room the page has a shape; up close, figures, small marks and states reward attention.

**T2 Differentiation density.** How many meaningful distinctions per area: states, roles, kinds of row. Distinctions that carry meaning raise it; decoration does not.

**T3 Curvature.** Is there some softness, like radii, curves in charts or an organic image, set against the grid? All right angles reads as cold; everything a pill reads as a toy.

**T4 Hue intensity.** Is there saturated color where it matters, held in one or two moments? Grey everywhere is cold; saturated chrome is hot.

**T5 Hue contrast.** Are there contrasting hues that mean something, like the accent against the neutral ramp, or green and red for change, or a painting's own palette?

## Design: harmony

Harmony is the order that holds the temperature together.

**H1 Reflectional symmetry on all scales.** Balance within a row, a panel, the page. Not mirror symmetry everywhere, but local balance the eye can rest on.

**H2 Translational and rotational symmetry.** Repetition: rows of one height, cards of one padding, a rhythm the eye can predict.

**H3 Self-similarity.** The same proportions and treatments at different scales: a panel's radius and padding echo the control's, the page grid echoes the panel grid.

**H4 Geometric linkage.** Things line up across the screen. An edge in the sidebar continues into the content. Columns align between panels.

**H5 Color harmony.** The palette is one family: one ramp, one accent, semantic colors toned to sit in it, images matched to the page.

## Content: resonance

**R1 Legibility.** Can it be read at a glance? Contrast, size, the hierarchy reading in the right order, numbers easy to compare.

**R2 Salience.** Does the thing that matters most stand out first? On Today, what needs the person; on a lead, the next step.

**R3 Depth.** Does it reward a second look? A figure that opens into its trend, a painting worth looking at, a record that holds its whole history.

## Content: value

**V1 Warrant.** Does it live up to its promise, given its purpose, context and cost? Every element earns its place. Count lines that explain the interface: callouts, subtitles, helper notes, panel titles that repeat the section. Real constraints, consequences and one line for an unfamiliar Lab feature do not count (see Copy in SKILL.md). On Folio, three to five such lines cap V1 at 2, six or more at 1.

**V2 Contribution.** Does the screen move the person's work forward, or only report on it? Actions next to the thing they act on.

**V3 Reach.** Who does it serve: the individual at the keyboard, the team or client around them, or something wider? A screen that helps an agency serve its clients reaches further than one that only tidies a list.

## Report format

```
                 Before  After
Craft              42     71    medium 2.5 → 3.0, execution 2.7 → 3.8
Design             38     66    temperature 2.4 → 2.8, harmony 2.5 → 3.8
Content            35     72    resonance 2.7 → 3.3, value 2.1 → 3.5
Overall            38     70
Scale cap        applied (k = 7 in the sidebar) → not applied (k = 4)
```

Then one line per criterion that moved by 2 or more, with the evidence.
