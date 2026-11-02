# MIRAI-Setu 2026 · Kyushu A website

## What This Does
A static website with a Japanese look and a light Indian accent, for the 11 members of Kyushu A:
- **Team:** one button per member, each with their photo. Each button opens that person's own page.
- **Journey map:** an animated, illustrated map of the route, with a hanko stamp for each city.
- **Presentation:** a slide viewer plus buttons to download the PPTX and PDF.
- **Language:** an EN / 日本語 button at the top switches the whole site and remembers the choice.

## Setup
None. Open `index.html` in Chrome or Edge. No server and no internet needed, apart from the web fonts.

## Usage: where files go
Names must match exactly. `.jpg`, `.jpeg`, `.png` and `.webp` all work.

| What | Put it here |
|---|---|
| Member photo (on the card and their page) | `images/<member>/profile.jpg` |
| Member's 6 gallery photos | `images/<member>/1.jpg` … `6.jpg` |
| Slides for the viewer | `presentation/slides/Slide1.PNG`, `Slide2.PNG` … |
| Deck to download | `presentation/MIRAI-Setu_KyushuA.pptx` (and `.pdf`) |

Member folders: `aabhas-malpani`, `sparsh-shukla`, `aryan-nilesh-pansare`, `meghraj-sarjerao-shinde`, `adarsh-gyan-priyadarshi`, `siddhant-chauhan`, `aarya-shisode`, `nandani-nareshkumar-maheshwari`, `divya-gupta`, `anmol-singhal`, `aarsh-jain`.

**Slides:** in PowerPoint, choose File → Export → Change File Type → PNG → All Slides, then move the images into `presentation/slides/`.

**Text:** edit `PEOPLE` (members), `STOPS` (map) and `PRESENTATION` (file names) at the top of the `<script>` in `index.html`.

**Japanese text:** members' text is in `PEOPLE_JA`, photo captions in `CAPTION_JA`, map stops in the `dj` and `wj` fields of `STOPS`, and everything else sits next to its English as `tr("English","日本語")`. Anything without Japanese shows in English.

## File Map
| Path | Purpose |
|---|---|
| `index.html` | The whole site: styles, data and pages |
| `images/<member>/` | Each member's photos |
| `presentation/` | The deck (`.pptx`/`.pdf`) and `slides/` images |

## Domain Assumptions
- The itinerary comes from the AFS welcome letter (Kyushu group). Planes appear only on the two legs the itinerary says were flights.
- The map is drawn from hand-placed coastline points, not survey data.
- The katakana names are first guesses. Ask each member to check theirs.
- The Japanese text is a draft translation that no native speaker has reviewed. It includes members' personal stories, so have a Japanese speaker and each member check it.
- The footer disclaimer follows the group's rule: the site is not an official AFS or Ministry website. Get each person's permission before publishing their name, face or photos.
- Member folders left over from v1–v2 (the other Kyushu scholars) are no longer used and can be deleted.
- Card photos (`profile.jpg`) are square crops from one of each member's own gallery photos. To use a different one, replace `profile.jpg`.
- Gallery captions were written from what each photo shows. Change them in the member's `captions` list.
- Members' text comes from `website_data.docx`, lightly edited (Aarsh's voice-note transcript tidied into prose; spelling and grammar fixed for Meghraj). Divya and Nandani have no text yet.

## Changelog
| Date | Change |
|---|---|
| 2026-11-01 | v1: template with a home grid (20 scholars), the journey route and a page per person |
| 2026-11-01 | v2: Japanese-first design (sakura crests, woodblock-print-style emblem, falling petals, hanko headings); animated route map with hanko stamps |
| 2026-11-01 | v4: real photos for all 11 members (66 gallery photos + card portraits, HEIC converted, resized to ≤1600 px); text for 9 members; captions per photo; empty template fields hidden once a member's page is written |
| 2026-11-01 | v3: narrowed to the 11 Kyushu A members; photos detected automatically (profile + gallery, any common extension); an album per place linked from the map stamps, the stop list and a new Photos section; a presentation viewer with PPTX/PDF download; disclaimer footer |
| 2026-11-01 | v5: gallery photos shown whole in a masonry layout so faces are never cropped; captions moved below the photos; album covers and thumbnails no longer crop |
| 2026-11-01 | v6: team order changed to Aarsh, Anmol, Siddhant, Adarsh, Aarya, then the rest |
| 2026-11-01 | v7: browser tab icon added (the 九 hanko from the header logo) |
| 2026-11-01 | v8: team cards keep names on one line (first + last name; full name stays on each person's page) |
| 2026-11-01 | v9: place-wise photo albums removed (Photos section, map-stamp links, album viewer, `images/places/`) |
| 2026-11-02 | v10: EN / 日本語 toggle at the top; whole site translated into Japanese |
| 2026-11-02 | v11: one-line tagline prompt removed; tags match on every member page (Programme and Team; college, internship and city show only once all 11 have them) |
