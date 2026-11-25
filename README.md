# Layout taxonomy

A taxonomy of **medium-agnostic compositional moves**: layouts you can identify from a single still, whether it is a poster, a book spread or a website first screen. It is not industry-specific. The quality bar is the Are.na reference board (below). The research is laid out visually in Figma.

- **Figma:** [Layout-Research](https://www.figma.com/design/LxWxkVXJpuZUP9VmFisKnP/Layout-Research?node-id=0-1), page "Nov 24"
- **Are.na reference board (PDF, 710 MB):** attached to this repo's [Releases](../../releases) as `arena-taxonomy-reference.pdf`. It is too large for git; page numbers `pNNN` used throughout refer to it.

## What's here

| Path | What it is |
|---|---|
| `docs/arena-derived-styles.md` | Definitions of the styles derived from the Are.na board |
| `docs/gap-analysis.md`, `.tsv` | Which styles the Taste Engine corpus covers, is THIN on, or is MISSING |
| `layouts/L01…L10` | Core layout styles. Each has `spec.md`, `vocabulary.tsv`, search `calibration*.tsv`, and reference images by source: `0-arena-reference`, `1-taste-engine`, `2-firecrawl`, `3-wikimedia-commons` |
| `devices/D01…D06` | Graphic devices that modify a layout (e.g. Type-Image Rebus, Shape-Mask Window) |
| `categories/` | 35 web layout categories plus `new-*` candidates, with Taste Engine examples, `coverage.tsv` and `prevalence.tsv` |
| `seed-list/` | Patterns the corpus is missing or thin on, with verified live sites and print sources (`seed-list.md`, `.tsv`) |
| `boards/` | Data and assets behind the annotated layout boards in Figma (`boards.json`) |
| `taste-engine-layout-tags/` | Taste Engine images for its 8 `layout` filter values (30 each, no industry filter), plus `boards-thin-missing/`: 15 boards of 12 for the thin and missing styles, with match grades |
| `figma-board-references/` | 2026-11-24 update: better visual and website references for six boards. See its README |

Every image folder has a `sources.tsv` (site or source URL, search id, match grade) where one applies.

## Notes for engineers

- **The 8 Taste Engine layout tags are coarse.** Treat them as modifiers rather than styles. Specific styles are reached with a filter plus a query (see `docs/gap-analysis.md`).
- **The tag rows skew to subpages.** Many results are customers, about or careers pages; a homepage-only re-pull would give a cleaner baseline.
- **Still missing from the corpus:** Type Perimeter Frame has no verified web example. Lone Object in Void and Framed Media are weak. See `seed-list/`.
- **Signed screenshot tokens are redacted** (`?token=REDACTED`). Re-read a search with the Taste Engine `get_search_result` tool to get fresh URLs.
- Screenshots of third-party sites and Are.na images are for internal research reference only.
