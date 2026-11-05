# Clarity Software / Folio — concept planning brief

Captured November 5, 2026. This document records the owner's direction and proposed concepts, not a commitment that features are implemented.

## Current scope

Focus on UI, product concepts, and demonstrable workflows for the next public claritysoftware.ai revamp. Collect visual references before deciding layouts or implementation. The site should use motion graphics and showcase Folio alongside Clarity Software's other offerings.

Original canvas: https://claude.ai/artifact/RkEDydbAhF3eE2gHLsH66x#page-dcb81aee8d83

Private working duplicate: https://claude.ai/artifact/HGNUJNm3Q5w13dLvfgt64e#page-dcb81aee8d83

Reference repository: https://github.com/cahteh/ui-taste

## Owner's product direction

### Founders experience

Founders reflects the owner's personal taste: effective, premium, sleek, and fast. References should help define typography, spacing, navigation, interaction, visual hierarchy, and motion in addition to color.

### Analog experience

Analog currently changes the color scheme. The intended evolution is a simpler experience that is easier for older users: larger text and icons, clearer controls, and less complexity. Treat this as a possible interaction and accessibility variant, rather than only a palette.

### Mobile

Retain the current mobile setup as an accessible “legacy view.” Explore a new streamlined mobile experience for quick shortcuts and selected functions while on the go. The exact default actions and navigation remain to be chosen from the reference and workflow review.

Develop the mobile sign-in experience alongside desktop sign-in. Desired concepts include Sign in with Google and Face ID. Technical authentication design and device support remain to be validated later; do not present these concepts as implemented capabilities.

### Prospecting

Explore a prospecting scraper / AI function using the Google Places API on Google Cloud. Candidate showcase flow: discover businesses, review and qualify results, and add selected prospects to Folio. Data access, storage, permitted use, and production implementation remain future decisions.

### Knowledge base

Add a knowledge base. Its content structure, editing experience, retrieval behavior, and relationship to Folio's AI features remain open concept questions.

### Marketing manager

Explore linked marketing accounts and campaign deployment across multiple platforms. Candidate showcase flow: link accounts, create a campaign, preview platform-specific variants, review, and deploy. Supported platforms, actual publishing capabilities, approvals, and reporting remain to be defined.

### Wellness pack

A healthcare client conversation may lead to a wellness pack. HIPAA compliance is a future requirement to assess, not a current product claim. For this phase, explore UI concepts only, using fictional data. Do not describe the concept as HIPAA compliant or imply that design alone establishes compliance.

## Proposed public showcase candidates

These are planning suggestions for review, not approved scope or finished capabilities.

| Showcase | Demonstration concept |
| --- | --- |
| Folio overview | A short motion-led tour of the core workspace and connected workflows |
| Mobile quick actions | Complete a few useful tasks through the new streamlined experience |
| Sign-in | Desktop and mobile concepts, including Google and biometric sign-in states |
| Prospecting | Discovery → qualification → selected prospect added to CRM |
| Marketing manager | Campaign creation → channel previews → review → deployment status |
| Knowledge base | Find or maintain information used by the team and AI |
| Themes | Founders presentation and Analog's simpler, larger-control experience |
| Wellness pack | Optional fictional workflow concept, without compliance claims |

## Reference intake plan

Accept images, videos, websites, component libraries, and short notes. For each reference, capture:

- Source link or file and a short descriptive name.
- What the owner likes, dislikes, or wants to explore; leave uncertain preferences unconfirmed.
- Applicable surface: public site, desktop app, mobile, sign-in, marketing, prospecting, knowledge base, wellness, or themes.
- Relevant qualities: layout, typography, color, density, components, interactions, motion, or accessibility.
- Status: incoming, approved inspiration, rejected, or needs review.

Suggested repository organization after inspecting its existing structure:

```text
README.md
briefs/folio-concept.md
references/incoming/
references/approved/
references/index.md
decisions/
```

Keep source attribution. Distinguish inspiration from code or assets cleared for reuse. Existing repository references may be removed as authorized by the owner once inspected; preserve unrelated project content. Repository access and changes have not yet been verified or completed.

## Next planning steps

1. Collect the owner's reference dump without requiring it to be pre-sorted.
2. Review references and record explicit preferences and recurring visual patterns.
3. Define a shared design direction, including Founders and Analog differences.
4. Select the public showcase stories and the mobile shortcuts worth prototyping.
5. Develop screen concepts and motion storyboards, then define implementation scope.

## Open decisions for later

- Which audience and primary workflow should lead the public Folio story?
- Which offerings beyond Folio should the site showcase?
- Which mobile actions deserve immediate access?
- Which marketing platforms should appear in the first concept?
- What information belongs in the knowledge base, and who maintains it?
- How much should Analog simplify navigation and workflows?
- What parts of the wellness pack are appropriate for the public showcase?

Do not block reference collection on these questions.
