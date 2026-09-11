# sessions

## 2026-09-11, session 1: Magic Mind Stafford LP teardown and Graymatter rebuild

Done
- Captured and deconstructed https://magicmind.com/pages/matthew-stafford-partner (computed styles,
  section heights, fonts, colors, image URLs). Written up in deconstructions/2026-09-11-magicmind-stafford.md
  with a block-by-block mapping to Graymatter.
- Transcribed Notion Brand Intake into src/brand/tokens.css (8 primitives, 15 semantics, two type
  families with the live-site woff2 files, 4pt spacing scale, radii, hairline rule) and built a small
  component layer in src/brand/base.css (type styles, buttons, pills, cards, tick-ring frame, FDA box,
  todo chip).
- Built pages/partner-athlete/ as the Graymatter mirror: film frame, split hero (ICP 1 mechanism
  headline), verbatim pull quote (Rayshawn Jenkins), Olive blends section with 4 blend cards and the
  bag's attribute row, 2x2 format grid from Shopify data, Tarmac mechanism split with the homepage
  timeline, people rail with verbatim quotes, Tarmac footer with boxed disclaimer.
- Pulled every asset from the Shopify CDN into assets/ with provenance in assets/SOURCES.md.
- Verified in the in-app browser at 1024 and 375 wide. No console errors, no horizontal overflow.

Surprises
- Notion query-data-sources quota capped after two tables. Worked around it (see tasks/lessons.md).
- Shopify featured media for the products are marketing composites with prices and exclamation
  marks baked in. Swapped to clean cutouts from the homepage.
- The live site's "750+ doctors" claim is flagged unsubstantiated in Notion page 10. Not used.

Next
- Items in tasks/todo.md. Then a second teardown to prove the workflow generalizes.
- Consider an extraction script (Playwright) that writes the measured-styles table automatically so
  step 1 of the workflow is one command.

## 2026-09-11, session 1 addendum
- Film slot now embeds a real Graymatter YouTube video (pkBchO9WTT8, Michael Chernow) via
  youtube-nocookie, centered in the content width on a Tarmac band with radius 16. Meta chips
  moved below the frame so they never collide with YouTube's title overlay. Verified at 1024 and 375.
- That video is shot vertical, so YouTube pillarboxes it in the 16:9 frame. A landscape upload
  would fill the slot better. Candidate IDs are in tasks/todo.md.
- Film slot changed again: founders story video (SxXwW0h3VTk, Novi and Jim on the thumbnail), full-bleed like the source, click-to-play facade so YouTube loads nothing until clicked.
- Film swapped to Building the Brand Ep. 3 (kKZX1vOoWsk) at Matt's call. SxXwW0h3VTk stays in assets/video as the both-founders alternate.
- Second aesthetic pass from the Stafford LP: dashed-ring certification badges, Meadow stat highlight, flavor swatches (approximate tokens, flagged in tokens.css), halftone texture on the quote block, tile hover. Verified at 1024.
- Added root index.html (Pages landing) and .nojekyll. All paths relative, so the site works under a
  project subpath. Not committed: Matt is creating the GitHub repo.
