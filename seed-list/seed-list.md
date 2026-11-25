# Seed list: patterns the Taste Engine corpus is missing or thin on

Built 2026-11-24 for the Taste Engine team. Full rows, including rejects and unchecked leads, are in `seed-list.tsv`. Verified screenshots are in the per-pattern folders.

## Method and caveats

- **Web candidates** came from three places:
  - visual browsing of minimal.gallery (pages 1–5, as full-page screenshots)
  - four Firecrawl research agents, which mined speckyboy, onepagelove, awwwards, muuuuu.org, createtoday.io and siiimple
  - my own leads
- **Taste Engine was not used.** Every candidate was captured live with a Firecrawl screenshot (waitFor 4000–5000 ms) and checked by eye. Only first screens that pass the test were saved.
- **Search worked poorly for these patterns.** Keyword search on the galleries returned listing pages or tutorials, not sites. The research agents' descriptions were unreliable: about 3 of 30 checked agent leads passed. Browsing gallery screenshots by eye found 3 of the 6 passes from far fewer captures.
- **Throughput was low.** Firecrawl rate limits (roughly 10 requests per minute, shared with the agents) slowed the work, so 13 leads are listed as *unchecked* in the TSV.
- **Print sources** are links only. They come from a research pass over V&A, MoMA, Cooper Hewitt, Wikimedia Commons, MACBA and Fonts In Use. Each is marked `yes` (a catalogue or curator description states the layout), `partial` or `unconfirmed` (not seen). MoMA, Cooper Hewitt and eMuseum block automated access, so their entries need a quick look in a browser.

---

## 1. Type Perimeter Frame (MISSING)

**Test:** Type runs around all four edges of the format like a border, and the image or an empty field sits in the middle.

**Web (0 verified).**
- Rejected: gotham.studio. It has small rotated labels on the side edges only.
- Closest near-miss: Petrillo.studio (see Bookend Type), whose giant numerals sit in all four corners.
- No search phrasing or agent surfaced a true edge-text frame. On the web this pattern seems to exist mainly as marquee-frame code demos (e.g. a freefrontend "scroll-driven marquee frame"), not as live brand sites.

**Print:**
- A.M. Cassandre, *Nord Express*, 1927 — https://collections.vam.ac.uk/item/O89673 (V&A: "text on the top, bottom and around the frame of the image")
- Anon., Walker Brothers Carpets ad, 1880 — https://fontsinuse.com/uses/24847/walker-brothers-carpets-ad-1880 (Fonts In Use tag "type as frame")
- J.O. Barnard, Mauritius "Post Office" 1d stamp, 1847 — https://commons.wikimedia.org/wiki/File:Mauritiuspostofficeissuestamp1847PD.JPG (unconfirmed)
- Charles Bell, Cape of Good Hope triangular stamp, 1853 — https://commons.wikimedia.org/wiki/File:Cape_Triangular_Postage_Stamp.jpg (unconfirmed)
- Collection: Fonts In Use, "type as frame" — https://fontsinuse.com/tags/7199/type-as-frame

## 2. Shape-Mask Window (MISSING)

**Test:** A photo or colour field is cut into a non-rectangular shape (arch, oval, circle, blob or letterform) that sits as a window in a flat ground.

**Web (1 verified).**
- `01-thecreativebodega.png`: The Creative Bodega — https://www.thecreativebodega.com/ — arch-topped portrait on a flat cream ground, with the headline beside it.

Rejected: sondergroup.ca, baldwintherapygroup.com, balenstherapy.com, xzecreative.com.

Unchecked leads (all small-business Squarespace/Podia sites):
- createwithmariah.com
- kerribakerpilates.com
- cerrutirealestate.com
- collabwithdom.com
- inspirewithintherapy.com

Note: on the web the arch mask lives mostly in therapist, wellness and creator templates, not on design-studio sites. That is probably why the studio-weighted corpus has none.

**Print:**
- Curt Teich & Co., large-letter postcard "Greetings from Springfield, Ohio", c.1930s–40s — https://commons.wikimedia.org/wiki/File:Greetings_from_Springfield_Ohio_-_Curt_Teich_big_letter_postcard.jpg (photos inside letterforms)
- Jan Tschichold, *Die Frau ohne Namen*, 1927 — https://www.moma.org/collection/works/5754 (partial: photo through a red circle)
- Studio Paul Andali / Alain Papazian, La Trinité 24/25 season, 2024 — https://fontsinuse.com/uses/65095/la-trinite-24-25-season (unconfirmed; Fonts In Use tag "arches")
- E. McKnight Kauffer, *Magicians Prefer Shell*, 1934 — https://collections.vam.ac.uk/item/O1037684 (partial: flat circles, colour not photo)
- Collection: Fonts In Use, "arches" — https://fontsinuse.com/tags/27696 (also "image masking type", /tags/17593)

## 3. Bookend Type (L07)

**Test:** Giant type bands pin the top and bottom edges, and the image or information sits in the gap between them.

**Web (1 verified).**
- `01-petrillo-studio.png`: Petrillo.studio — https://petrillo.studio/ — giant clock numerals (time across the top, date across the bottom) with a clock face in the middle band.

Rejected:
- ortolan.com.au: giant wordmark at the bottom only, over a photo (half a bookend)
- madeinhaus.com

Unchecked: wandelmaier.com.

**Print:**
- Cassandre, *Nord Express*, 1927 — https://collections.vam.ac.uk/item/O89673
- Herbert Matter, *Pontresina Engadin*, 1935 — https://www.moma.org/collection/works/5323 (unconfirmed)
- El Lissitzky, *USSR Russische Ausstellung*, 1929 — https://www.moma.org/collection/works/6458 (partial)
- The existing folder `layouts/L07-bookend-type/3-wikimedia-commons/` already holds 10 checked Commons posters.

## 4. Vertical Spine Type (L08)

**Test:** A line of type is rotated 90° and runs the full height of the format as a structural column, with other content hung against it.

**Web (0 verified).** Eleven candidates were captured, and all fail:
- The speckyboy "vertical lettering" roundup sites now show only small rotated nav labels, or have been redesigned.
- The Japanese tategaki sites (upforward.co.jp, misakigumi.com) set vertical text mid-screen, not as a full-height edge spine.

Partial hits:
- istdawards.com (see Letter Scatter) has DESIGNERS set vertically at the right edge.
- kwokyinmak.com has vertical text rails at both edges.

**Print:**
- Armin Hofmann, *Giselle*, Basler Freilichtspiele, 1959 — https://collection.cooperhewitt.org/objects/18673303 (Cooper Hewitt: GISELLE runs vertically down the left edge). Fonts In Use record: https://fontsinuse.com/uses/1328/giselle-poster-basel-stadt-theater
- Herbert Bayer, *Kandinsky zum 60. Geburtstag*, 1926 — https://www.moma.org/collection/works/5104 (unconfirmed)
- Enea Bortone, *Neubad über Wasser halten*, 2021 — https://fontsinuse.com/uses/77630/neubad-ueber-wasser-halten-poster (unconfirmed)
- Collection: Fonts In Use, "rotated type" — https://fontsinuse.com/tags/2755
- The existing folder `layouts/L08-vertical-spine-type/3-wikimedia-commons/` holds Lissitzky and Klutsis examples.

## 5. Whisper Margins (L05)

**Test:** The centre is empty or nearly empty, and all information is tiny type pushed into the corners and edges.

**Web (1 verified).**
- `01-thursdayschild.png`: Thursday's Child — https://www.thursdayschild.global/ — black viewport with tiny nav and credits in the four corners and one tiny word at the centre. This is the dark variant.

Rejected: imsky.co, stickbird.studio, shm.studio.

Unchecked:
- greymac.com
- marinasuvorova.com
- martinstoleru.com

Caution: empty-centre captures are easily confused with mid-load states (see the gap analysis).

**Print:**
- Richard Hamilton, The Beatles ("White Album") sleeve, 1968 — https://www.macba.cat/en/node/27579
- Kenya Hara, MUJI "Horizon", 2003 — https://hara.ndc.co.jp/en/news/make-the-future-better-than-today/ (unconfirmed)
- Dafi Kühne, *Daylight* poster — https://fontsinuse.com/uses/54530/daylight-poster (unconfirmed)
- Collection: Fonts In Use, "small type" — https://fontsinuse.com/tags/4101

## 6. Script Ribbon

**Test:** One oversized calligraphic or script line sweeps across a photo or field.

**Web (0 verified).** Five agent leads from onepagelove were all captured and all fail:
- mikemcalister.com
- tiagofragoso.com
- victorialavine.com
- thisisfc88.com
- danielsun.space

They use hand-lettering at small scale, or no script at all.

**Print:**
- Stefan Sagmeister, AIGA Detroit, 1999 — https://www.moma.org/collection/works/102915 (partial)
- Stefan Sagmeister, Lou Reed, *Set the Twilight Reeling*, 1996 — https://sammlung.mak.at/en/collect/set-the-twilight-reeling_67816 (unconfirmed)
- Mary Banas, Mitski, *Laurel Hell*, 2022 — https://fontsinuse.com/uses/45896/mitski-laurel-hell-album-art (unconfirmed)

## 7. Letter Scatter

**Test:** The letters of one word are spread out individually across the field or a grid.

**Web (3 verified).**
- `01-onoera.png`: Onœra — https://onoera.com/ — wordmark split into on · œ · ra and spread edge to edge. Borderline, because it splits into syllables rather than letters.
- `02-kwokyinmak.png`: Kwok Yin Mak — https://www.kwokyinmak.com/ — the three characters of the name set huge and spread diagonally, joined by hairlines.
- `03-istdawards.png`: ISTD International Typographic Awards 2024 — https://istdawards.com/ — giant I, S, T, D scattered across a black screen, with rotated and diagonal words. The page is kinetic.

Rejected:
- henriheymans.com (word-level scatter behind an Enter gate)
- rxkstudio.com
- localstudio.fr
- nationalstudentshow.com
- typographyprinciples.obys.agency

Unchecked: giorgospapadakis.com, bleibtgleich.com.

**Print:**
- Dafi Kühne, *F-u-t-u-r-e* poster — https://fontsinuse.com/uses/40887/f-u-t-u-r-e-poster (Fonts In Use tag "scattered type")
- Dafi Kühne, *Tipoteca 1–25* — https://fontsinuse.com/uses/31399/tipoteca-1-25-poster
- Theo van Doesburg & Kurt Schwitters, *Kleine Dada Soirée*, 1922 — https://www.moma.org/collection/works/5533 (partial)
- F.T. Marinetti, *Après la Marne, Joffre visita le front en auto*, 1915/1919 — https://www.moma.org/collection/works/7683 (unconfirmed)
- Collection: Fonts In Use, "scattered type" — https://fontsinuse.com/tags/9344

## 8. Type on a Path

**Test:** Display type follows a diagonal, curve or circle.

**Web (0 verified).**

Rejected:
- kota.co.uk
- unseen.co (Enter gate)
- contentarchitecture.dev: the spiral text panel did not render. The minimal.gallery thumbnail shows it, so it is worth a retry with a longer wait.

Partial hits:
- istdawards.com: INTERNATIONAL is set on a diagonal.
- victorialavine.com: a slightly tilted marquee band, small type.

As the gap analysis found, most circular type on the web is a small spinning badge.

**Print:**
- Guillaume Apollinaire, *Il pleut* (calligramme), 1916 — https://commons.wikimedia.org/wiki/File:Guillaume_Apollinaire_-_Calligramme_-_Il_pleut.png
- E. McKnight Kauffer, *Magicians Prefer Shell*, 1934 — https://collections.vam.ac.uk/item/O1037684 (V&A: text running around a circle)
- Vladimir & Georgii Stenberg, *Man with a Movie Camera*, 1929 — https://www.moma.org/collection/works/217943 (partial)
- El Lissitzky, *Beat the Whites with the Red Wedge*, 1919 — https://commons.wikimedia.org/wiki/File:Beat_the_Whites_with_the_Red_Wedge.jpg (unconfirmed)
- Collection: Fonts In Use, "type on a circle" — https://fontsinuse.com/tags/4587 (also "type on a curve", /tags/3595)

---

## Summary

| Pattern | Web verified | Print sources (yes/partial/unconfirmed) |
|---|---|---|
| Type Perimeter Frame | 0 | 5 (3/0/2) |
| Shape-Mask Window | 1 | 5 (2/2/1) |
| Bookend Type | 1 | 4 (2/1/1) |
| Vertical Spine Type | 0 | 5 (3/0/2) |
| Whisper Margins | 1 | 4 (2/0/2) |
| Script Ribbon | 0 | 3 (0/1/2) |
| Letter Scatter | 3 | 5 (3/1/1) |
| Type on a Path | 0 | 5 (3/1/1) |

**Recommended next step:** browse more gallery pages by eye (minimal.gallery pages 6 and on, godly.website, siteinspire typographic) rather than keyword search, and work through the 13 unchecked leads in the TSV when the rate limit allows.
