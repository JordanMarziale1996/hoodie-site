# Hoodie scroll-world build brief

Use the `scroll-world` skill to add a scroll-driven video story to the Hoodie site. Everything the skill's interview asks for is already answered below, so don't ask again. Only stop for the two cost checkpoints.

## Ground rules

- **Product page stays first.** `index.html` opens on the product gallery and buy box, and that must not change. The scroll film goes directly under the product section, replacing the dark marquee and the "Ditch the wire brush" before/after split. Everything below that (comparison table, features, how it works, guarantee, FAQ, footer, sticky add-to-cart bar) stays.
- **The product must look like the real unit.** Use `images/hero.jpg` and `images/topdown.jpg` as image references in every scene that shows Hoodie: a black-and-champagne-gold body, a stainless chainmail roller, and an LED light on top. The skill normally says not to pass `--image` references for photoreal scenes. Ignore that only for the Hoodie scenes, because a made-up product design would be misleading.
- **No invented claims.** No stats, reviews, "was" prices, countdowns or low-stock lines. That would breach Australian Consumer Law.
- Match the existing site: Inter font, ink `#161616`, brass `#9A7640`.
- Commit and push to `main` when it's done and QA'd. GitHub Pages serves the site.

## Intake answers

| Field | Value |
|---|---|
| SUBJECT | Hoodie, a cordless bristle-free grill cleaner with a spinning stainless steel chainmail roller, for Australian backyard BBQs |
| BRAND_NAME | Hoodie |
| PALETTE | ink #161616, charcoal #2B2B2B, brass #B08A4E, sand #F6F4F0, gum-leaf green #5E7B5A, ember orange #D9622B |
| BG / ACCENT | page background #161616 (dark, full-bleed photoreal); accent #B08A4E |
| TONE | premium, warm, laid-back Australian |
| STYLE | Photoreal (adapt the skill's photoreal preamble): "Ultra-photorealistic cinematic photography of a single cohesive Australian backyard BBQ area at golden hour, timber deck, gum trees, warm low sun, natural materials, editorial magazine quality, shallow depth of field, no people. Cohesive palette of ink #161616, brass #B08A4E, sand #F6F4F0, gum-leaf green #5E7B5A, ember orange #D9622B. Absolutely no text, no letters, no numbers, no logos." |
| CAMERA | One continuous walkthrough: Architecture A, forward-only legs chained from each leg's actual last frame, no connectors |
| MOBILE | Yes: native 9:16 portrait chain, wired as `clipMobile` / `stillMobile` |
| VIDEO_TIER | `seedance_2_0` via Monid. Run the whole chain as a 480p previz first and show it to Jordan, then render the final at 1080p. |
| STILLS_SOURCE | Higgsfield `gpt_image_2` |
| BUDGET CAP | US$70 total, desktop + mobile, re-rolls included. Show the estimate and wait for a yes before (1) the previz and (2) the final render. |

## Sections (5 legs, in order)

1. **grime**
   - Scene: a charred, crusted grill grate at dusk on a timber deck. An old wire brush lies on the grate with bent, loose bristles.
   - Focal point: the wire brush.
   - Eyebrow: THE PROBLEM
   - Title: Your wire brush is shedding.
   - Body: Old bristles bend, loosen and can break off onto the grill.
   - Tags: none
2. **meet**
   - Scene: Hoodie resting on the grate edge, its LED light glowing warm, with the chainmail roller catching the low sun.
   - Mid-leg move: a slow half-orbit around Hoodie.
   - Eyebrow: MEET HOODIE
   - Title: Chainmail, not bristles.
   - Body: A spinning stainless steel roller that has nothing to snap off.
   - Tags: Bristle-free, Cordless
3. **clean**
   - Scene: Hoodie mid-roll along the bars. One half of the grate is clean and shining, the other half still charred.
   - Mid-leg move: a low lateral track alongside the bars.
   - Eyebrow: ONE CLICK
   - Title: The motor does the scrubbing.
   - Body: Press once, roll it along the bars and watch the grime lift.
   - Tags: Built-in LED
4. **cook**
   - Scene: the clean grill with sausages and onions sizzling, an empty outdoor table set for friends, and string lights coming on. No people.
   - Mid-leg move: rise and swoop.
   - Eyebrow: BACK TO THE GOOD PART
   - Title: Clean grill. Better barbie.
   - Body: Less time scrubbing, more time with your mates.
   - Tags: none
5. **hero** (the finale)
   - Scene: Hoodie standing on the timber bench in warm light, with a soft dark background.
   - Eyebrow: HOODIE
   - Title: A$79. Free shipping.
   - Body: 30-day returns and a 12-month warranty.
   - CTA: "Shop Hoodie", which scrolls to `#product`

Pacing: give `grime` and `hero` a higher `scroll` and some `linger`. Keep `clean` brisk.

## Watch-outs

- **Content filter:** "fire", "flame" and "smoke" can trip Seedance's filter. If a leg comes back flagged, re-roll it, then swap in softer words ("glowing coals").
- **Check every last frame:** eyeball each leg's last frame before chaining the next one.
- **QA:** run the skill's seam QA and test the page at 390px and 1440px. The sticky add-to-cart bar must still appear once you've scrolled past the buy box.
- **File sizes:** keep the encoded clips reasonably small. GitHub Pages has a 100 MB per-file limit and a soft 1 GB site limit.
