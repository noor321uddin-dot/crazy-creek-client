# Crazy Creek — Sled Zone Map

Two related assets for the Sled-and-Stay campaign: a **navigation map** guests use to
reach the riding zones, and a **stylized brand illustration** of the same story.

## Live previews
- **Sled Zone Navigator (interactive):** https://noor321uddin-dot.github.io/crazy-creek-client/sled-map/
- **Brand illustration:** https://noor321uddin-dot.github.io/crazy-creek-client/sled-map/illustration.html

## Files
| File | What it is | Where it goes |
|---|---|---|
| `index.html` | Clean full-bleed wrapper around the navigator (for the public link) | Preview only |
| `nav-map-embed.html` | **The navigation map** — Leaflet + OpenTopoMap, real staging coordinates, Get-Directions handoff to Google Maps. Pure fragment. | Paste into a **GHL Custom JS/HTML** element |
| `illustration.html` | Stylized topographic brand map (SVG), standalone page | Preview / export |
| `ghl-embed.html` | The brand illustration as a GHL-paste block | Paste into a **GHL Custom JS/HTML** element |
| `preview.png` | Thumbnail render | — |

## Navigation map — how it works
- Home view is **centered on Crazy Creek Resort**; gold dashed lines point to each staging area.
- **⛶** frames all five zones · **⌂** returns to the resort · **⌖** shows the guest's live position.
- Each pin + card shows compass bearing and straight-line distance, and a **Get directions**
  button that opens **Google Maps turn-by-turn** from wherever the guest is.
- Scoped under `.ccnav` (won't restyle the host page); re-run guard for GHL hydration.

## Staging coordinates (researched 2026-08-26 — sources on file)
| Zone | Confidence | Note |
|---|---|---|
| Eagle Pass | HIGH | Trailhead ~2 km from the resort's own lot (Eagle Valley SC map + AllTrails) |
| Boulder Mountain | HIGH | Trailforks trailhead pin, Westside Rd Revelstoke |
| Owlhead | HIGH | Eagle Valley SC map + AllTrails, Sicamous |
| Queest Mountain | HIGH | **Staging moved to Sicamous Mar 2024** — old FSR lot deprecated |
| Frisby Ridge | MEDIUM | Trailforks pin matching the club's "end of Westside Rd" description — verify before towing |

⚠ Confirm the staging points with Jason / the local clubs before promoting; always check
[avalanche.ca](https://avalanche.ca) conditions.

## To use in GoHighLevel
Page → Edit → drag a **Custom JS/HTML** element → paste the whole `nav-map-embed.html`
(or `ghl-embed.html`) → Save → verify in **Preview** (the builder canvas doesn't run scripts),
then on a phone (⌖ needs a location-permission tap; Get directions opens the Maps app).
