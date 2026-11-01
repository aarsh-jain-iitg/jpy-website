# MIRAI-Setu 2026 · Kyushu A website

## What This Does
A static website with a Japanese look and a light Indian accent, for the 11 members of Kyushu A:
- **Team:** one button per member, each with their photo. Each button opens that person's own page.
- **Journey map:** an animated, illustrated map of the route, with a hanko stamp for each city. Tap a stamp to open that city's photo album.
- **Photos:** one album per place (Tokyo, Fukuoka, Nagasaki, Beppu, Kyoto, Hamamatsu, Yamanashi).
- **Presentation:** a slide viewer plus buttons to download the PPTX and PDF.

## Setup
None. Open `index.html` in Chrome or Edge. No server and no internet needed, apart from the web fonts.

## Usage: where files go
Names must match exactly. `.jpg`, `.jpeg`, `.png` and `.webp` all work.

| What | Put it here |
|---|---|
| Member photo (on the card and their page) | `images/<member>/profile.jpg` |
| Member's 6 gallery photos | `images/<member>/1.jpg` … `6.jpg` |
| City album | `images/places/<city>/1.jpg`, `2.jpg`, `3.jpg` … with **no gaps** in the numbering |
| Slides for the viewer | `presentation/slides/Slide1.PNG`, `Slide2.PNG` … |
| Deck to download | `presentation/MIRAI-Setu_KyushuA.pptx` (and `.pdf`) |

Member folders: `aabhas-malpani`, `sparsh-shukla`, `aryan-nilesh-pansare`, `meghraj-sarjerao-shinde`, `adarsh-gyan-priyadarshi`, `siddhant-chauhan`, `aarya-shisode`, `nandani-nareshkumar-maheshwari`, `divya-gupta`, `anmol-singhal`, `aarsh-jain`.

City folders: `tokyo`, `fukuoka`, `nagasaki`, `beppu`, `kyoto`, `hamamatsu`, `yamanashi`.

**Slides:** in PowerPoint, choose File → Export → Change File Type → PNG → All Slides, then move the images into `presentation/slides/`.

**Text:** edit `PEOPLE` (members), `PLACES` (album captions), `STOPS` (map) and `PRESENTATION` (file names) at the top of the `<script>` in `index.html`.

## File Map
| Path | Purpose |
|---|---|
| `index.html` | The whole site: styles, data and pages |
| `images/<member>/` | Each member's photos |
| `images/places/<city>/` | Each city's album |
| `presentation/` | The deck (`.pptx`/`.pdf`) and `slides/` images |

## Domain Assumptions
- The itinerary comes from the AFS welcome letter (Kyushu group). Planes appear only on the two legs the itinerary says were flights.
- The map is drawn from hand-placed coastline points, not survey data.
- The katakana names are first guesses. Ask each member to check theirs.
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
