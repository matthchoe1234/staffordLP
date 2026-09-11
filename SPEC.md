# lp-lab: competitor landing page teardown and Graymatter rebuild

Owner: Matt Choe (AI Engineer). Reviewer for anything that ships: Yoshua (brand system),
Jim / Novi / Simon (claims and copy), compliance doctor (anything near the disease line).

## What this is

A local, static lab for one repeatable job: take a competitor landing page, deconstruct
its structure and conversion mechanics into a written spec, then rebuild that structure
with Graymatter's brand system, assets, and compliant copy. Output is a static HTML page
you can open in a browser, review, and hand to Shopify / Replo / a designer.

This is not production. Nothing here deploys. No customer data, no secrets, no backend.
It exists so the team stops guessing at styling (see Notion, "Web Design System, Code-Level
Component Library": the Triple Whale LP landed flat because agents had nothing machine
readable to pull from). Every page here is built on `src/brand/tokens.css`, which is a
code transcription of Notion Brand Intake, so the rebuilds are on-brand by construction.

## Workflow (one page, end to end)

1. **Capture.** Open the competitor URL in the in-app browser. Screenshot every section.
   Pull computed styles with JS (font family, size, weight, colors, radii, section
   heights, image URLs). Save the raw notes to `deconstructions/<date>-<slug>.md`.
2. **Deconstruct.** Write the section-by-section teardown: what each block is for
   (attention, proof, offer, mechanism, authority, capture), its layout, its measured
   type and color, and the conversion job it does.
3. **Map.** For each competitor block, decide the Graymatter equivalent. Same job,
   same position, native content. Never copy their copy. Never invent a fact we do not
   have. Anything we cannot source gets a visible placeholder chip, not filler.
4. **Build.** `pages/<slug>/index.html` + `page.css`. Only `src/brand/tokens.css` and
   `src/brand/base.css` for tokens and components. Page CSS is layout only.
5. **Check.** Run the pre-ship check from Notion page 10 (Copy compliance and brand voice
   standard) before calling it done. Then preview at `http://127.0.0.1:8787/pages/<slug>/`.

## Brand system, as transcribed (source: Notion Brand Intake, Sep 2026)

Colors (Primitives): Lucid #FFFFFF, Linen #F5F5F5, Tarmac #161616, Meadow #E6FDA5,
Brainwave #FF567F, Olive #8AA665, Powder Blue #CDD9E8, Sky Blue #7197C3.
Reference Semantics, not primitives: surface.base, surface.subtle, surface.inverse,
surface.accent (CTA fill), surface.urgent, surface.cool, surface.nature, surface.blue,
text.primary, text.inverse, text.inverse-subtle, text.highlight, highlight.focus,
highlight.inverse, highlight.urgent. Proportion rule: 70 surface / 25 text / 5 accent.
Meadow and Brainwave are never large fields. Support colors go full-bleed only, with
Tarmac text.

Type: exactly two families. Exposure (205TF, variable optical axis; -40 for bold display,
+40 for light display) for headlines. ABC Monument Grotesk Mono for everything else.
Web fallbacks: Fraunces, Roboto Mono. Web/UI scale is 48px h1 down to 12px small, all on
the 4pt grid. Sentence case for headlines and subheads, period at the end. Title Case
only for product names, labels, nav. Italics for quotations only. Bold for emphasis only.
Highlight (Meadow behind a word) reserved for one impact moment per headline.

Layout: 4pt grid everywhere. Spacing scale space.xs to space.2xl on systematic surfaces.
Radii 8 / 16 / 24 / pill 99. Almost shadowless: a 1px Tarmac hairline does structural
work. No gradient or mesh backgrounds. Product always upright. No emoji, no glyph
decoration, no new fonts.

Marks: Wordmark Heavy Slab (primary), Wordmark Serif (secondary), Emblem Circular G
(tertiary). Tarmac marks on Lucid/Linen, Lucid marks on Tarmac. Never recolor, distort,
add effects, or retype. Files live in Drive folders linked from the Notion Marks table.

Copy: no em dashes, no exclamation marks, no wellness cliches, no all caps in headlines.
Problem, then solution, then proof. Every structure/function claim carries `*` and
resolves to the boxed FDA disclaimer on the same page. Nitrosigine® carries the mark.
Testimonials are verbatim and never lifted into brand voice. Never name a competitor.
Bright Mind is legacy: never introduce it into new copy, flag it where it appears.

## Open items that block a real ship (not this lab)

- Exact approved FDA disclaimer string (pending compliance doctor and Jim).
- Any doctor-endorsement count ("750+ doctors" on the live site is unsubstantiated per
  Notion page 10; do not reuse).
- Ingredient count claim ("27 active ingredients") pending Jim / Novi / Simon.
- Official on-dark wordmark SVG from Drive (this repo derives one by fill swap).
- Official Blend Icons from the Icon Library (this repo uses geometric placeholders).
- Partner bio and film for any athlete page need partner-team sign-off.

## Repo layout

```
SPEC.md                  this file
AGENTS.md                how agents should work in here
assets/                  brand marks, fonts, product, people, icons, refs (all pulled from
                         trygraymatter.com CDN or Shopify; see assets/SOURCES.md)
src/brand/tokens.css     Notion Brand Intake as CSS custom properties
src/brand/base.css       reset, type classes, buttons, pills, cards, badges, hairlines
deconstructions/         one teardown per competitor page
pages/<slug>/            one rebuilt page per teardown
tasks/                   todo, lessons, sessions
.claude/launch.json      python http.server on 8787 for preview
```
