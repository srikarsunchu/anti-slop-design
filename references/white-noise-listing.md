# White-noise listing — a ten-shot App Store screenshot set from a category leader

Source: a competitor's live US App Store listing (white noise, sleep), viewed 4 Sep 2026. Extracted by screenshot read, described in words; no images stored. Names withheld: the lesson is the structure, not the brand.

## The one idea
One ground, one headline slot, one feature per shot. Every shot is the same picture with one thing swapped, so the gallery reads as a single object while the thumb swipes.

## Type (per role)
| Role | Face | Weight | Size | Tracking | Line-height | Color |
|---|---|---|---|---|---|---|
| display (headline) | Geist-like grotesk | 600 | ~32px | near 0 | ~1.1, always two lines | white |
| heading (quote) | same | 600 | ~28px | 0 | 1.2 | white |
| body (CTA) | same | 500 | ~17px | 0 | 1 | pale teal |
| ui (inside phone) | app's own dark list | 400/500 | 15/17 | 0 | 1.3 | white on navy |
| meta | none observed | | | | | |

## Color
- ground: deep navy, about #0F1B2D, identical on all ten shots
- surfaces: the phone's dark list UI, a shade lighter than the ground
- ink / secondary / tertiary: white; no measured secondary tier
- accent: gold (line art, star-bursts, lanterns, lotus) and a pale teal (the CTA)
- status colors: none
- count of distinct colors: four (navy, white, gold, teal) — one more than a full palette

## Ground
Flat navy. It works only because it never changes across the ten frames; on any single shot it is a plain void.

## Icons
None as icons. Line art in gold: a lotus, a reed, a cloud, paper lanterns, two sleeping rabbits — stock-looking illustrations, not a set with one grammar.

## Layout
- content max-width: the 390-wide frame, roughly 28px side margins
- edges: headline centred at a fixed top offset on every shot; device top at the same y on straight shots
- spacing scale observed: headline, then one block (device or illustration), then nothing; three zones at most
- radii: the phone's own; cards inside at roughly 16
- three layouts, rotated for rhythm: (a) tilted iPhone at about −25°, cropped at the bottom edge, line art in the empty corners; (b) straight-on iPhone with cards popping out; (c) no device — an illustration page (testimonial, closer)

## Motion
Static gallery. None.

## Depth
- sections / panels: ten shots — hero grid, "#1" claim with tilted phone, press logos, mix, timers, testimonial, ASMR, "fall asleep in 10 minutes", fan sounds, closer
- how many show the product working: six show a real screen; four are claims or illustration
- how many animate: none

## Hierarchy read
The headline is primary on every shot and the device is secondary; position (top) and weight (largest type) agree. The gold line art is tertiary and stays in the corners. On the testimonial and closer, the illustration takes over and the type shrinks — the two shots with no product in them are the two that lean on decoration.

## What the structure teaches
- One ground across the whole set. Never restyle per shot.
- A two-line headline at a fixed position. The eye lands in the same place ten times.
- One feature per shot, one sentence each.
- One repeated line-art motif in the accent colour ties the set; it lives in the empty corners, never over text.
- Alternate angled and straight device shots for rhythm; crop the tilted phone at the frame edge.
- A testimonial shot and a closer (icon, title, call to action) are structural slots, not optional extras.

## What to refuse
- The navy-and-gold palette: gold is a habit accent here, meaning nothing.
- Stock illustration (lotus, rabbits, lanterns). Draw the motif from the product's own geometry, from exact primitives.
- "#1", press logos, "12 Million Happy Sleepers": claims that cannot be checked from the listing. Never fabricate a number or a quote; if the testimonial slot has no real quote, ship a bracketed placeholder or drop the shot.
- Weight 600 on the headline: 500 with negative tracking does the same job without shouting.
- A fourth colour for the CTA. The call to action is white; colour is spent on one motif and one state.
- Copy about features the product does not have (mixes, ASMR).

## The lesson, as a rule
A screenshot gallery is read as one object while swiping, so hold ground, headline position and motif constant and change exactly one thing per shot.

## Confidence
Layout, order, headline copy and shot types: read directly from the live listing. Font, weight and hex values: estimated from a screenshot, not measured in a DOM. Colour count: measured by eye.

Applied in `~/workspace/lull/design/Store-1.dc.html` to `Store-9.dc.html` (4 Sep 2026): Lull's #111 ground, Geist 500 headline at 72px top, the dial's rim ticks as the motif in 1.5px amber on three shots, a bracketed testimonial placeholder, a white CTA.

## In-app UI (Slumber Studios "White Noise", screenshots 4 Sep 2026)
- Pure black ground. A search field first, full width, 44 tall, #1C1C1E.
- Section headers in 34px bold: Fans, Mechanical Sounds, Colored Noises, Rain,
  Thunder, Water, Birds, Animals, Wind. Rows ~72 tall with a 56px photo
  thumbnail, 20px name, a crown glyph on locked rows.
- A "One time offer! 30 DAY TRIAL" banner at the top of the home list.
- Persistent mini-player: thumbnail, name, play, AirPlay.
- Five tabs: Sounds, Mixes, Controls, Settings, Gift. Purple accent.
- Controls: a 2×3 grid of cards with gradient icons: Fader 1m, Oscillator,
  Timer 8h, Auto Play, Upgrade, Background Audio (off by default).
- The lesson: the same page structure as Dark Noise (list + player + controls)
  carried by breadth and search intent, with none of the craft. Photos as row
  identity, crowns as monetisation, five tabs, and a background-audio toggle
  that ships off are the tells. What to take: breadth behind one control,
  timers to 8h, a one-minute fader.
