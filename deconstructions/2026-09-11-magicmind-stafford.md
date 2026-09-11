# Teardown: Magic Mind, Matthew Stafford partner LP

Source: https://magicmind.com/pages/matthew-stafford-partner
Captured: 2026-09-11, desktop viewport 1024px, Shopify theme (section IDs prefixed
`shopify-section-template--18710747119750__`). Measured values are computed styles, not guesses.

## Global system

| Property | Measured |
|---|---|
| Body font | Circular / Circular Std (geometric sans), weights 450 book, 500, 600, 700 |
| Mono accent | Akkurat Mono 12 to 14px, letter-spacing 1.2px (pills, feature body copy) |
| Display h2 | 67px / 73px line height / weight 600 / tracking -0.67px, second line italic 450 |
| Serif subhead | 35px / 700 ("Trusted by Matthew Stafford") |
| Body | 18px / 450 |
| Card copy | 14px / 450 / 1.2 |
| Ink | #000 on white; body text #000 |
| Neutral surface | #EFEFEF (review block, product grid tiles) |
| Header | rgb(28,27,27), 60px tall, white wordmark, links Shop / Science / Reviews, account, cart |
| Footer | #000, text rgb(240,240,235) |
| Primary CTA | Black pill (radius 90px), 14px, uppercase, white text, full card width |
| Secondary CTA | Outline pill, black 1px, 14px bold, inline arrow |
| Card radius | 10px |
| Section max width | 1024 at this viewport, fluid |
| Popup on load | "Find your formula" quiz modal (3 questions), brand mark, dismissable |

Aesthetic: bright, playful clinical. Clean white, one saturated accent per section
(pink, yellow-to-green gradient, deep teal), rounded cards, scalloped photo mask, hand-drawn
logo. Copy is confident and short. Headline pairs bold + italic lines.

## Section map (top to bottom)

| # | Block | Job | Layout | Notes |
|---|---|---|---|---|
| 0 | Announcement bar | Reassure | Full width strip, white bg, 12px caps bold | "Boost mental performance, clinically-backed ingredients" |
| 1 | Header | Nav | Dark bar, logo left, 3 links center, account + cart right | |
| 2 | Hero video | Attention, partner proof | 16:9 YouTube embed, 576px tall, partner name in title | "Matthew Stafford: The Mind Behind the MVP" |
| 3 | Split hero | Position + partner | 50/50. Left white: h2 67px bold "Sharper Mind." + italic "Sustained Energy.", serif 35px "Trusted by Matthew Stafford", 18px bio paragraph. Right: pink field with hand holding product (Hand-Gradient_original_2.png) | 723px tall. No CTA in hero. |
| 4 | Pull-quote testimonial | Proof | #EFEFEF. Left: scalloped B&W photo (404px). Right: 24px/500 quote, 24px/700 name, 18px/400 credential, small hand-drawn arrow | 524px tall. Quote verbatim from athlete. |
| 5 | What is it | Mechanism, ingredients | Gradient 130deg #FDD76E to #00A087. Left: 39px "What is Magic Mind?", right 18px intro. Then 3 white cards (radius 10, ~276px wide, 23px padding): ingredient photo, 22px title with italic keyword, 18px body, 14px bold ingredient list | 1337px tall |
| 5b | Certification badges | Trust | 4 circular black-ring badges (Vegan, Kosher, No BPA, Third party tested) on the same gradient | |
| 6 | Product grid | Offer | 2x2 tiles on #EFEFEF, radius 10, padding 24. Each: 22px title (italic or caps), mono pill label with caffeine mg (colored tint), product image, 14px description, black pill CTA "TRY X" | 1256px tall. Four SKUs. |
| 7 | Mechanism split | Differentiate | 50/50. Left: full-bleed teal photo, huge white "5x" display, "more effective absorption". Right: 24px lead, outline pill "LEARN MORE", 4 rows with hairline dividers: 23px/700 title + 14px mono body | 944px tall |
| 8 | Advisory board | Authority | 45px "Scientific / Advisory Board" (second line italic), 18px intro, horizontal carousel of 6 circular headshots (200px), 18px/500 name, 14px credential, prev/next arrows, "SEE THE SCIENCE" CTA | 1178px tall |
| 9 | Footer | Capture + nav | Black. Logo, 30px tagline with italic, email capture with white pill button, 4 link columns, socials, address, legal | |

## Conversion mechanics worth keeping

1. Partner proof is front-loaded twice (video, then split hero) before any product talk.
2. Every claim block is followed by an offer block or a CTA. Rhythm: proof, mechanism, offer, mechanism, authority, capture.
3. The product grid removes choice anxiety with one variable per tile (caffeine mg) in a mono pill.
4. The mechanism split gives one big number and four short rows. Skimmable, screenshot-able.
5. Authority section is faces plus credentials, not logos.

## Mapping to Graymatter

| MM block | Graymatter block | Content source | Status |
|---|---|---|---|
| Announcement | Subscriber offer strip | Live site announcement bar | Verbatim, sentence case |
| Header | Tarmac header, Lucid wordmark, Shop / Science / Ingredients, cart | Live site nav | Done |
| Hero video | Full-width 16:9 click-to-play facade, local maxres thumbnail, iframe injected on click | Graymatter channel, "Scanning My Brain And Crossing $20M ARR, Building The Brand Ep. 3" (kKZX1vOoWsk), Jim on the frame | Done |
| Split hero | Lucid left, Powder Blue (surface.cool) right with hand-and-sachets photo | Headline from ICP 1 mechanism (Notion page 10). Bio kept factual. | Bio needs partner sign-off |
| Pull quote | Linen block, tick-ring framed photo, verbatim quote | Homepage testimonial, Rayshawn Jenkins, Starting NFL Safety | Verbatim |
| What is it + 3 cards | Olive (surface.nature) full-bleed, Tarmac text, 4 blend cards | Brand foundation overview; homepage blend lists | Blend icons are geometric placeholders |
| Badges | Four long-dashed-ring certification badges (line icon + curved label), then the bag's mono attribute row | Icon Library: GMP Certified, Sugar Free, Plant-Based; site trust bar: Third-Party Tested. Attribute row: PhD Formulated, Nootropic Drink Mix, 40 Servings | Badge art is a placeholder for the official files. No "750+ doctors" (unsubstantiated) |
| Product grid | 2x2: Bag, Travel Packs, Twin Pack, Flavor Variety Pack; one variable per tile (servings) | Shopify Admin (titles, list prices, images) | List price only, promo TBD |
| Mechanism split | Tarmac panel, pouring photo, big "4 to 8 hours" display; right: timeline rows | Homepage timeline copy, asterisked | Done |
| Advisory board | "Trusted by top performers." people rail with verbatim quotes | Homepage carousel (4 people), ambassador page (Dr. Wiegers) | Ambassador quotes with "Bright Mind" excluded |
| Footer | Tarmac footer, Lucid wordmark, email capture, columns, boxed FDA disclaimer | Live site footer | Disclaimer string is the statutory reference pending approval |

## Aesthetic devices borrowed in the second pass

- Ring badge row after the ingredient cards (theirs solid black rings; ours the brand's long-dashed certification ring with text-on-a-path labels).
- One saturated impact moment per dark section (their white "5x" on teal; our Meadow "4 to 8" on Tarmac via text.highlight).
- Product-tinted micro labels (their caffeine pills tinted per SKU; ours flavor swatch dots on approximate flavor tokens, since a filled flavor pill is limited to one per surface).
- Textured neutral surface behind the pull quote (their flat #EFEFEF; ours Linen with the bag's halftone dot pattern at 9% ink).
- Quiet product lift on tile hover, no shadow.

## Things we deliberately did not copy

- The yellow-to-green gradient (brand forbids gradients; Olive full-bleed does the same pacing job).
- The scalloped photo mask (replaced with the brand's radial tick-ring motif).
- The hand-drawn arrow doodle beside the quote (brand: no decorative flourishes).
- The hand-lettered wordmark energy in general; Graymatter's slab wordmark and mono do the personality work.
- "5x" efficacy number (no substantiated equivalent; used the timeline duration instead, asterisked).
- The advisory board framing (Graymatter has no advisory board to cite; used testimonials).
- The quiz popup (out of scope, noted as a follow-up experiment).
- Uppercase CTA labels (brand rule: sentence case).

## Bright Mind flags found in source material

- Shopify product titles: "Graymatter Bright Mind", "Graymatter Bright Mind Travel Packs", twin pack titles.
- Homepage accordion copy and CEO letter reference "Bright Mind".
- Ambassador page quotes from Michael Chernow, Grayson Goldin, Rayshawn Jenkins use "Bright Mind".
- All packaging photography carries "BRIGHT MIND" under the wordmark.
