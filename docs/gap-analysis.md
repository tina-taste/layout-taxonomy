# Gap analysis: layout patterns in the Taste Engine brand corpus

Probe date: 2026-11-23. Each pattern got one short literal query describing the first screen (`search_brands`, top_k 30, depth fast, no filters), plus a second phrasing when the top 30 held 2 hits or fewer. Every screenshot was checked by eye against the pattern's test. Captures taken while the page was still loading count as misses and are counted separately. The 10 layouts tested earlier are folded in with their best existing calibration score (top 10 only; their top-30 counts were never recorded). Full rows, queries, search_ids and hit brands are in `gap-analysis.tsv`. Contact sheets are in the scratchpad at `gap-probe/sheets/`.

Classes: **COVERED** = 6 or more hits in the top 10. **THIN** = 2–5 hits in the top 10, or 3 or more in the top 30. **MISSING** = 1 or fewer in the top 30 after two phrasings.

## Did the method work? (controls)

The controls did **not** all score as expected. Only one of the three reached COVERED. That changes how to read every other row.

| Control | Top 10 | Top 30 | Why |
|---|---|---|---|
| Full-bleed photo hero + headline overlay | 4, then **6** on second phrasing | 8 | Wording. Phrasing 1 inferred `page_type=landing_page` and drifted. |
| Centred headline hero + button | 4 (both phrasings) | 5 | Wording-independent: both phrasings returned almost the same list. The corpus leans towards studio and portfolio sites, which usually show a centred headline with no button. With the button requirement dropped it scores about 7/10. |
| 3-column card grid | 4 | 8 | Below the fold: card rows normally sit under the hero, and the corpus has only the first screen. |

Takeaways:
1. The engine retrieves reliably at about 4–7/10 even for common patterns, so THIN is the normal state, not a sign of a gap.
2. "Common on the web" does not mean "common in this corpus". The index is a curated design-studio corpus, not a sample of the web.
3. A control can fail for structural reasons (the first-screen-only capture) as well as for wording.

## MISSING (2)

| Pattern | Best | What came back instead |
|---|---|---|
| **Type Perimeter Frame** (Are.na) | 1/30 (panorama, borderline) | Phrasing 1: "border/frame" matched brand *names* (framer, frame ×2, weareframework). Phrasing 2: the Whisper Margins and centred-serif cluster. |
| **Shape-Mask Window** (device) | 1/30 per phrasing (nicktarasov arch portrait; lenkadaviesova arc crops) | Phrasing 1: About pages. Phrasing 2: "arch" matched architecture brands (archipelago, arcprojects, archiebolden, goa/clou/saltarchitecture), returning photos *of* arches rather than photos *in* an arch shape. |

## THIN (20 incl. prior layouts and 2 controls)

Grouped by why they are thin:

- **Real but rare. The pool runs out after the first few hits:** Letter Scatter 4/10 (offpixel, dondregreen, hervebaillargeon, matbold, all in the top 4), Script Ribbon 3/10, Type on a Path 3/10, Overprint Type Stack 3/10, Vertical Spine Type (L08) 2/10, Bookend Type (L07) 2/10.
- **Common, but hidden by query routing:** Bleed Photo Overprint 5/10 (and 6/10 with the plainer control wording, so effectively covered), Monumental Type Fill 5/10, Floating Archipelago 5/10, Layered Collage 4/10, Exposed Ruled Grid (L02) 5/10.
- **Mid-load captures fill the list:** Framed Small Media on Empty Stage 3/10 (9 of the top 30 were blank or loader captures), Motif Field 4/10, Whisper Margins (L05) 5/10, Lone Object in Void (L06) 5/10, Colour Block Mosaic (L09) 5/10.
- **Needs interaction, or sits below the fold:** Index list with hover preview 2→4/10 (the preview only appears on hover, so these sites are captured as a bare list), Bento grid 2→3/10 (usually a feature section below the hero), plus the centred-hero and card-grid controls.

## COVERED (11 incl. prior layouts and 1 control)

| Pattern | Top 10 | Top 30 |
|---|---|---|
| Desktop/OS window metaphor | **9** | 13 |
| Type-Image Rebus | 7 | 7 |
| 3D/WebGL scene | 7 | 15 |
| Editorial asymmetric broken grid | 7 | 10 |
| Split Field (L01) | 7 | – |
| Specimen Matrix (L04) | 7 | – |
| Centered Classical Axis | 6 | 10 |
| Sticky split screen (visible two-column state only) | 6 | 7 |
| Full-bleed photo hero (control, second phrasing) | 6 | 8 |
| Ledger Composition (L03) | 6 | – |
| Text Wall (L10) | 6 | – |

Surprise: three of the web patterns (OS metaphor, 3D scene, broken grid) and one print device (rebus) score better than anything the earlier 10-layout study found. The corpus is strong on expressive studio sites and weak on plain product-marketing layouts.

## Failure modes, ranked

Counts are rows (of 33) where the mode materially caused misses. One row can have several modes.

| # | Failure mode | Rows | Concrete example |
|---|---|---|---|
| 1 | **Routing** (a word pulled a page type, industry or style) | 16 | "huge white letters over a photo" → style=High Contrast, which returned type-only studios (drivecapital, iceberg) with no photo. "project list" → page_type=portfolio, which returned image-grid portfolios. |
| 1a | ↳ *Lexical brand-name match* (a new sub-mode) | 5 | "border/frame" → framer, frame, weareframework. "arch" → archipelago, arcprojects, archiebolden. "bento" → BentoML plus food brands. "circle" → Circle. "letter" → letter, lettersfromsweden. |
| 2 | **Mid-load capture** | 15 | Framed Small Media: 9/30 blank or loader screens (joshuaoladiti "100%", neutral-studio, oker, silencio). 3D scene: "Enter / sound on" gates and black WebGL canvases. |
| 3 | **Tag-vocabulary gap** (no corpus tag for the defining feature) | 8 | No tag for rotated, path-set, perimeter, script-placed or masked imagery. Vertical Spine tag-mining returned only generic Swiss tags. |
| 4 | **Rarity** (simply scarce in the corpus) | 7 | Letter Scatter: 4 genuine hits, then filler. Bookend Type: 2. |
| 5 | **Print-only** (common on posters, rare on the web) | 5 | Type Perimeter Frame, Shape-Mask Window, Script Ribbon, Overprint Type Stack, Type on a Path. These are all from the Are.na print board. |
| 6 | **Interaction-only** (needs hover, scroll or a click to see) | 5 | Index list with hover preview: the preview image is never in the still. Type on a Path: most web examples are small spinning badges. Sticky split: stickiness can't be verified. 3D scenes sit behind click-to-enter gates. |
| 7 | **Below the fold** | 4 | 3-column card grid control, Bento grid, Bookend Type (footer wordmark), Index list (the list often starts below a hero). |

## What this implies for the Taste Engine team

1. **Capture after the hero has settled, or flag captures that look mid-load** (blank fields, centred loader rings or percentage counters, "Enter" gates). This one fix would lift 15 of 33 rows. It also matters because mid-load captures currently inflate Whisper Margins and Lone Object, making them look better covered than they are.
2. **Stop words that match brand names from acting as retrieval signals** in descriptive queries ("frame", "arch", "bento", "circle", "letter"). Five patterns failed on this alone.
3. **Add composition tags** for the features that have no vocabulary: rotated or vertical type, type on a path or arc, edge or perimeter type, masked or clipped image shape, repeated motif background, overprinted type layers.
4. **Store a second capture (scroll ~1 viewport) or a full-page thumbnail.** Card grids, bento sections, bookend footers and index lists all live there.
5. **Treat the print-only patterns (Perimeter Frame, Shape-Mask, Script Ribbon) as real corpus gaps.** They would need seeding from outside the current crawl rather than better retrieval.
