# Ghost of Tsushima — menus and HUD, the restraint benchmark for a duel game

Source: interfaceingame.com/games/ghost-of-tsushima (1920×1080 captures:
main-menu, pause, hud, hud-2, hud-3, logo, hint), read 2026-09-09 by drawing
each capture into a canvas and sampling regions. Written descriptions from
Andy's Cabin (UI immersion piece), Mike Ackerman's Director's Cut icon work,
and the standoff wiki. No Sony asset was copied; values only. Used for Temple
Night (`~/workspace/temple-night`).

## The one idea
"Lost in nature, not in menus" (Nate Fox). Nothing is on screen unless
something is happening: the HUD leaves outside combat, the standoff turns the
frame into a film frame, and the menus are black bars and one red square. The
thing that embodies it is the standoff: letterbox bars, one prompt, one word.

## Type (per role)
| Role | Face | Weight | Size (1080p) | Tracking | Line-height | Color |
|---|---|---|---|---|---|---|
| logo | brush calligraphy caps | — | ~120 | wide | — | #f4f5f1 |
| location title | light humanist sans caps, ornament dashes each side | 300–400 | ~30 (22 cap) | ≈.2em | — | #fdfdfd |
| menu item | same sans caps | 300–400 | ~30 (22 cap) | ≈.08em | rows 70 (6.5% of height) | selected #fdfdfd on a white brush bar (black text on the bar); unselected #cdd4cf; disabled #849290 |
| pause/option button | same sans caps on a black brush bar | 400 | ~22 | ≈.08em | 44 bar | #ffffff on #363636 bar |
| enemy / boss name | same sans caps | 400 | ~24 | ≈.1em | — | #fdfefe |
| hint bar | same sans caps, button glyph inline | 400 | ~20 | ≈.06em | 40 bar | #eeeeee on rgba(14,17,13,.8) |
| objectives | same sans, sentence case | 400 | ~18 | 0 | — | #fdfdfd, dimmed line #b4e0da when done |

The face is not published; it reads as a light humanist/geometric sans
(pointed A M N, spurless G, straight-legged R). Jost 400 with tracked caps is
the closest OFL stand-in; the brush calligraphy is a logo, not a text face.

## Color
- ground: the game world; menus over a crushed, desaturated still of it
- pause ground: light grey #d4d5d4 (the one light surface in the game) with
  black #080808 chrome, black-and-white crushed photos as tile art
- ink / secondary / tertiary: #fdfdfd / #cdd4cf (≈78%) / #849290 (≈50%)
- red, one family: seal #b81e10 (brightest) with average #ad2c1b; selected
  pause tile #9e2c29; territory tag #d13d39; health rules #f74445 (a 7px
  rule at 1080p, slight glow). It marks the seal, the selected tile, danger
  and health. Nothing else.
- gold: resolve dots only (#f0c850 region)
- count: white at three levels, black, one red, one gold

## Ground
The scene. Menus use a crushed black-and-white still of the world so the UI
stays two-tone. No gradients as chrome; a bottom bar of near-black at 80%
for hints.

## Icons
Kamon-derived: simplified, perspective-free, symmetrical, bold lines, mono.
Gear icons from crushed 3D screenshots. Button glyphs inline in the hint text.

## Layout
- HUD: player health a thin red rule at x=10.4% of width, y=97%, ~14% of
  width long, resolve dots above its head; boss health a thin red rule 26%
  wide centred at y=4%, name beneath; stance in a bottom-right tile only
  while relevant; objectives top-left; location title centred at y=22%
  with dashes each side and a red tag beneath.
- Menus: one left column at x=14%, rows 6.5% of height, caps.
- Pause: tiles 6.5% wide with 1.2% gutters; a vertical stack of black bars
  centred at 16% width; footer buttons bottom-right.
- Standoff: letterbox bars top and bottom, prompt centred low, HUD gone.

## Motion
- HUD fades out a few seconds after combat ends and returns on any change
  (not measured; from the written descriptions).
- Standoff: bars slide in, a hold prompt, the enemy twitches, release; a
  perfect release cuts to the kill. Timings not measured.
- Menus: a brush stroke sweeps behind the selected item.

## Depth
- surfaces: title, HUD, standoff, hints, location card, pause, options,
  confirmation, journal, map
- all populated with real state; the HUD is empty by design when idle

## Hierarchy read
The world is primary and everything agrees: the largest element on any
gameplay frame is the scene, the HUD is two thin rules and dots, and even the
main menu gives 80% of the frame to the sword in the grass. The one
disagreement is the pause screen's light grey ground, which reads as a
different product until the black brush bars pull it back.

## The lesson, as a rule
"A HUD that disappears makes every appearance a signal, so draw HUD elements
as thin rules and small glyphs that fade to a rest opacity when nothing
changes, and let the standoff (letterbox + one word) carry the drama instead
of the chrome."

Second: "One red, spent on the seal and on danger, is enough for an entire
game; white at three levels does the rest."

## Confidence
Colors: measured from the 1080p captures. Sizes and positions: measured in
image pixels, rounded. Tracking and face: read from magnified crops, guessed
as a family. Motion timings: not measured; the durations used in Temple
Night (320 letterbox, 220/180 banner, 600 HUD fade, 900 result) are the
method's ladder, not the game's.
