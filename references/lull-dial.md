# Lull dial — SUPERSEDED 4 Sep 2026

Kept for the record. The dial was dropped the same day after comparing Dark
Noise and Slumber Studios in-app UI; see `lull-player.md` for the shipped
structure and `principles/mobile-tells.md` ("A physical control on glass").

# Lull dial — a mobile build under this method, direction picked from three sketches

Source: `~/workspace/lull` (`src/theme.ts`, `src/components/Dial.tsx`,
`src/screens/Now.tsx`) and the design canvas working files in
`~/workspace/lull/design/`. Built 2026-09-04. Values are the code's own.

## The one idea
"The app is a knob." One physical control: turn to choose a sound with a
detent per stop, press the centre to start or stop, the rim fills as the
timer runs down. Everything else is a sheet.

## How the direction was chosen
Three low-fi directions on one canvas, each as two 390 x 844 frames (Now and
the picker) so they compared like for like: A Nightstand (the phone as an
instrument on the table), B Journal (the mother's night, not the baby's),
C Dial (one physical control). Sri picked C. The unchosen sketches stay on an
Archive page with their names unchanged.

## Type (per role)
| Role | Face | Weight | Size | Tracking | Line-height | Color |
|---|---|---|---|---|---|---|
| display (countdown) | Geist in the canvas, SF in the app | 400, tabular | 44 | −1.2 | 48 | label |
| name | same | 500 | 22 | −0.4 | 28 | label |
| label (row) | same | 400 | 17 | −0.3 | 22 | label |
| body | same | 400 | 15 | −0.2 | 20 | secondary |
| caption (rim labels, detail) | same | 400 / 500 selected | 13 | −0.2 | 18 | secondary / label |
| machinery (eyebrow, hint, VOL) | Geist Mono / Menlo, caps | 400 | 13 | +1 | 18 | tertiary |

## Color
- ground: #111111 with a radial lift to #1A1A1A behind the dial; grain at 5%
- surfaces: cell #181818, nested #222222, knob #171717, knob centre #141414
- rim #2A2A2A, ticks #8C8C8C, selected tick and pointer #F2F2F0
- ink / secondary / tertiary: #F2F2F0 / rgba(242,242,240,.6) / .4
- accent: #E39A45, a 10pt dot at the knob centre, only while playing. Nothing
  else in the app is coloured, including selection and the slider.
- count of distinct colors: four greys of surface, three of text, one accent

## Ground
Radial lift centred on the dial so no corner is flat; grain as an SVG
pattern. The knob casts a real shadow (0 14 24 at 60%). No colour in the
ground: the dot is the only light.

## Icons
Almost none. A chevron on the Timer row (Lucide). The dial is drawn from
primitives: two circles, nine tick lines, one bar. The app icon is the same
knob with the pointer at eleven o'clock so it reads as a knob, not a clock.

## Layout
- edges: 20 from the screen; 16 inside a cell; VOL label 44 wide
- dial: 340 box, knob 240, rim r=158, ticks at r 144 to 154, labels at r 174
- detents: nine stops from −160° to +160°, 40° apart, a 40° dead zone at six
  o'clock like a real potentiometer
- centre target: 88 (44 radius); the pan responder yields to it
- spacing: 4 / 8 / 12 / 16 / 24 / 32 / 48; rows 52; radii 12 groups, 20 sheet

## Motion
- knob follows the finger with no easing; snaps to the detent at 200ms
  standard on release; haptic selection click at each detent crossing
- press .97 at 150ms on the centre; the dot fades in over 300ms
- sheet 350 strong ease-out in, 250 standard out
- reduced motion: snap is instant, opacity changes stay

## Depth
- screens on the canvas: Now (works: drag, tap, timer sheet, volume), turning
  state, timer, tonight, three first-run moments, paywall, rating, lock
  screen, Live Activity, two widgets, StandBy, icon, five store shots
- real data: the Priya scenario throughout (2:41, third wake, 44:12 left,
  Rain 2 h 00, Shush 40 min)

## Hierarchy read
The knob is the subject by size, by being the only thing with depth, and by
owning the only colour. The countdown is the second thing and only exists
while true. Position and weight agree.

## The lesson, as a rule
"A physical control replaces a list, so when the whole product is one
decision, make that decision a knob, a slider, or a switch that the thumb can
work without reading, and let every other option live in a sheet."

Second: "Direction fidelity is not deliverable fidelity, so pick between
low-fi sketches that each show the same two screens, then build only the
winner hi-fi."

## What the first render got wrong
- The static sketch put ticks at 45° while the labels sat at 40°; the hi-fi
  pass computed both from one table. Compute geometry once, never by eye.
- Widget title wrapped at 158 wide; `white-space: nowrap` on the name.
- Dial tick marks at #5A5A5A vanished at 25% brightness; lifted to #8C8C8C.

## Confidence
Measured from source and the canvas files. The pan gesture is verified in the
browser canvas (pointer events) and by review in React Native; it has not yet
been driven on a real device.
