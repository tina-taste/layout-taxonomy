# Discovery sample: how the corpus splits across the 35 categories, and what's missing

## Method
- I ran 16 layout-neutral searches with `search_brands` (fast, top_k 30). Ten were "company homepage" with an industry filter (saas, fashion, food, architecture, media, healthcare, fintech, hospitality, nonprofit, gaming). Six had no filter: "minimal / bold colourful / dark / editorial / playful / corporate website".
- That gave 480 cards, or **441 unique first screens** after removing duplicate URLs. I downloaded every screenshot, put them on 19 contact sheets, and looked at each one.
- Each screen got one primary category for its dominant composition. Some also got modifier tags, such as overprint or motif. Screens that fit none of the 35 went into the X-clusters.
- Search IDs for the discovery searches are in the tool-results files. The candidate scoring searches are: lefthero 9138ae6c, textleftmedia 23e83b1b, textleftmedia v2 a58bd76a, logosplash 54a6626b, textsplit 000a5d80, framed 103c2456, motif ec7a72dd, overprint 079265bd, shapemask 2af150bb, letterscatter 16783710.
- Files: `prevalence.tsv`, `new-candidates.tsv`, and `new-<slug>/1-taste-engine/` (6 screenshots plus `sources.tsv` for each candidate).
- Caveat: one person classified everything, once, from about 350px thumbnails. Treat counts within ±2 as ties.

## How the sample splits
**Half-loaded or blocked: 63 of 441 (14.3%).** This covers loaders, blank or faded captures, cookie walls and email-capture popups. Fashion and food e-commerce cause the most, mainly through newsletter popups (taylorstitch, thousandfell, greats, bettr, newgroundcoffee).

Of the 441 screens:

| # | Category | n | share |
|---|---|---|---|
| 02 | Full-bleed media with overlaid text | 83 | 18.8% |
| 01 | Centred hero | 74 | 16.8% |
| NEW | Left-aligned statement hero | 62 | 14.1% |
| 26 | Monumental type | 34 | 7.7% |
| NEW | Text-left / visual-right hero | 30 | 6.8% |
| 07 | Split screen | 12 | 2.7% |
| NEW | Logo splash | 10 | 2.3% |
| 18 | Editorial broken grid | 8 | 1.8% |
| 31 | Collage/layered | 7 | 1.6% |
| 29 / 32 | Corner-text frame / Floating archipelago | 6 each | 1.4% |
| 30 | Isolated object in void | 5 | 1.1% |
| 03 / 17 | Product-screenshot hero / Colour block mosaic | 4 each | 0.9% |
| 19 / 20 | Magazine cover / News front page | 3 each | 0.7% |
| 09 11 22 23 | Sidebar, Card grid, Text-only index, Text wall | 2 each | 0.5% |
| 05 12 13 21 35 | Carousel, Bento, Contact sheet, Long-form column, 3D scene | 1 each | 0.2% |
| 04 06 08 10 14 15 16 24 25 27 28 33 34 | Search-led, Video-first, Map+list, Feature rows, Masonry, Drifting grid, Ruled grid, Pricing, Form-led, Big header+footer, Vertical spine, Dashboard, OS window | 0 | 0% |

Five compositions make up **79%** of the sample (02, 01, Left-aligned hero, 26 Monumental type, Text-left/visual-right). Only 3 of those 5 are in the current 35. The other 30 categories share the remaining 21%, and 13 of them have no examples at all.

## What the corpus over- and under-represents
- **Over-represented: hero-style first screens.** The corpus stores one first screen per site, mostly homepages and about pages, so almost everything is a hero. Full-bleed, centred and left-aligned heroes make up about half the sample.
  - Monumental type is very common in agency, food and gaming sites, much more than on the web generally. That reflects the curated, design-forward bias of the corpus.
  - Dark agency sites with a small left-aligned statement are a recognisable sub-cluster (see screens 367–380).
- **Under-represented: below-the-fold and page-type patterns.** Feature rows, Pricing, Map+list, Dashboard, Form-led, Bento and Card grid barely show in a first screen. They aren't rare on the web. They live further down the page or on page types that the neutral searches don't route to.
  - These categories are only reachable with routing words such as "pricing", "map" or "dashboard". The brief already notes the risk that those words pull in industries along with the layout.
- **Rare and boutique: art-directed type and grid categories.** Vertical spine, Big header + big footer, Drifting photo grid, Visible ruled grid and OS window never appeared in a neutral sample. Earlier targeted searches did find them, so they exist in the corpus but in tiny numbers (well under 1%).
- **Industry skew in the sample:**
  - Fintech, healthcare and SaaS sites split almost entirely between Left-aligned hero, Centred hero and Text-left/visual-right.
  - Fashion and hospitality are mostly Full-bleed media.
  - Architecture is the most varied industry: editorial grid, corner text, colour blocks, and many loaders.
  - Playful and bold sites drive Monumental type, Collage and Motif field.

## New category candidates (clusters of 3 or more that fit none of the 35)
| Candidate | n in sample | top10 / top30 | Verdict |
|---|---|---|---|
| **Left-aligned statement hero** | 62 (+3 two-column text split) | 8 / 12 | **Add (core).** The left-aligned twin of Centred hero and the biggest hole in the taxonomy. |
| **Text-left / visual-right hero** | 30 | 8 / 10 (with the right phrase) | **Add (core)**, or define it formally as the soft, continuous-field variant of 07 Split screen. The phrase "photo on the right" got only 4/10 because it pulls hard splits. |
| **Logo splash** | 10 | 6 / 7 | **Add (niche).** Score preloaders as misses, since many look identical. |
| **Motif field** | 3 primary + 6 tagged | 8 / 13 | **Add.** The best search recall of any candidate. |
| **Letter scatter** | 3 tagged | 7 / 8 | **Add (niche).** Precise in the top 10. |
| Bleed photo overprint | 8 tagged | 4 / 6 | **Modifier** on 02 and 26. The search returns plain monumental type. |
| Framed media on empty stage | 4 | 3 / 6 | **Weak.** Merge into 30 Isolated object in void. |
| Shape-mask window | 4 | 2 / 3 | **Modifier** (image-crop attribute). "arch" pulls real architecture. |
| Two-column text split | 3 | 6 / 8 | **Merge** into Left-aligned statement hero. |

Clusters with fewer than 3 examples, left unplaced:
- Illustrated scene (2: prevint, maximatherapy). Several more illustrated screens were filed as Centred hero.
- Image triptych (1: commonry).
- Sticker scatter (2, tagged): cafe-robot, huehaus. Fold into 31 Collage.

## Known candidates from earlier research
| Candidate | Seen in sample | Verdict |
|---|---|---|
| Bleed photo overprint | 8 tagged | Modifier, not a category (see above). |
| Centred classical axis | 0 distinct | No. It's a typographic or styling variant of 01 Centred hero. Use it as a style tag. |
| Motif field | 9 | **Yes**, add it. |
| Shape-mask window | 4 | Modifier. |
| Type perimeter frame | 2 (common-coin, soundsright) | No. It's a sub-variant of 29 Corner-text frame. Keep it as a tag. |
| Type on a path | 2 (hims, relajaelcoco), plus 1 in the shapemask search (thirteen23) | No. Typographic modifier. |
| Overprint type stack | 0 clear | No. Watchlist only. |
| Letter scatter | 3 | **Yes (niche)**: rare, but search finds it precisely. |
| Script ribbon | 1 (happycog) | No. |
| Index list with hover preview | n/a | No. The behaviour doesn't show in a static first screen. Fold into 22 Text-only index. |
| Sticky split | n/a | No. Scroll behaviour can't be seen in the stored screenshot. Fold into 07 Split screen. |
| Framed media on empty stage | 4 | Weak. Merge into 30. |

## Recommendations
1. Add **Left-aligned statement hero** and **Text-left / visual-right hero** to the hero family. Together they cover about 21% of the corpus that the 35 currently miss.
2. Add **Motif field**, **Logo splash** and **Letter scatter**. That makes 40 categories.
3. Keep these as modifier tags rather than categories: overprint, shape-mask, type-perimeter, type-on-path and sticker-scatter.
4. Expect about 14% half-loaded captures in any neutral query, and up to 25–30% in fashion and food e-commerce, because of popups.
