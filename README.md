# ui-taste

Carter Long's design review skill for Claude. It scores a screen on craft, design and content, finds what reads as unconsidered, sets a direction, fixes the screen in nine passes and scores it again.

ui-taste is an adaptation of [unslop](https://github.com/heydamir/unslop) by Damir Sokolovsky ([@heydamir](https://x.com/heydamir)), used under CC BY 4.0. The nine-pass method, most of the signs, the generic tokens, the visuals guide, `effects.md` and both scripts come from unslop.

## What changed from unslop

- **Scoring.** Every run scores the screen before and after with Carter's "Adjudicating Beauty" rubric: craft (medium × execution), design (temperature × harmony, after Nikos Salingaros) and content (resonance × value), with a scale cap. See `references/rubric.md`.
- **Bare UI.** Callouts, subtitles, helper notes, flavor text and titles that repeat the breadcrumb are signs to remove.
- **Folio's Founders theme** is a fixed direction with exact tokens. Client work still gets a direction from the product.
- **No monospace.** Figures use tabular numerals in the interface family.
- **Paintings first.** Public-domain paintings and real photographs come before generated images.
- **Reduced motion** is part of every motion pass.
- **Carter's own references:** Folio screens and the Vermeer from sign-in, plus an `inspiration/` folder.

## Layout

```
skills/ui-taste/
  SKILL.md               method
  references/
    rubric.md            scoring
    signs.md             what to look for
    tokens.md            Founders and generic values
    visuals.md           paintings, scenes, objects
    refs.md, refs/       reference screens
    inspiration/         images Carter adds
    effects.md           code treatments (unslop)
  scripts/
    snapshot.mjs         save a live page (unslop)
    story.mjs            render a story video (unslop)
```

## Install

Claude Code, for one person:

```bash
mkdir -p ~/.claude/skills && ln -s "$PWD/skills/ui-taste" ~/.claude/skills/ui-taste
```

Or copy `skills/ui-taste` into a project's `.claude/skills/`. Then ask Claude to review, score or polish a screen.

The scripts need Node and Playwright, and `story.mjs` also needs ffmpeg.

## License

CC BY 4.0, see `LICENSE`. Credit both Carter Long and Damir Sokolovsky in copies and adaptations. The Vermeer is public domain. Folio screenshots show synthetic sample data.
