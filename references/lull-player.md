# Lull player — the shipped structure: list + player

Source: `~/workspace/lull` (`src/theme.ts`, `src/components/PlayButton.tsx`,
`src/components/SelectSheet.tsx`, `src/screens/Now.tsx`) and
`~/workspace/lull/design/Main.dc.html`. Built 2026-09-04, the same day the
dial (`lull-dial.md`) was dropped. Values are the code's own.

## The one idea
"One tap to start; the list is one pull away." Layout copied from Dark Noise's
player, value for value, in Lull's system: a 196pt tile with the sound's icon,
the name at 34, one 76pt light play disc with the glyph in amber, "Choose a
sound ⌄", two small glyphs (log, timer), the volume slider.

## How the structure was chosen
Dark Noise (3.6K ratings, praised for its interface) and Slumber Studios
"White Noise" share the same pages: a grouped sound list with favourites, a
player with one big control, timer controls, widgets, lock screen. Dark Noise
wins on craft. Lull adopts the structure and keeps its own craft: one accent,
mother-first copy, dim design, a night log.

## Type (per role)
| Role | Face | Weight | Size | Tracking | Line-height | Color |
|---|---|---|---|---|---|---|
| display (countdown) | SF (Geist on the canvas) | 400, tabular | 44 | −1.2 | 48 | label |
| name | same | 500 | 22 | −0.4 | 28 | label |
| label (row, search) | same | 400 | 17 | −0.3 | 22 | label |
| body | same | 400 | 15 | −0.2 | 20 | secondary |
| caption (row note) | same | 400 | 13 | −0.2 | 18 | secondary |
| machinery (eyebrow, hint, VOL, section labels) | Menlo / Geist Mono, caps | 400 | 13 | +1 | 18 | tertiary |

## Color
- ground #111111 with a radial lift to #1A1A1A behind the play disc; grain 5%
- surfaces: cell #181818 (tile, rows), nested #222222 (sheet groups); play disc #F2F2F0
- rim #2A2A2A; ink #F2F2F0 / rgba(242,242,240,.6) / .4
- accent #E39A45: the play/pause glyph on the light disc, and nothing else.
  Favourites use a filled white heart, not the accent.

## Layout
- edges 20 from the screen, 16 inside a cell, 36 icon well, text at 84
- player: tile 196 (radius 48) + name 34 + play 76 + "Choose a sound" + tools row + volume; nothing else
- Structure: the list is the base screen; the player is a full-screen card
  over it, dragged down with a PanResponder (follows the finger, snaps at
  120pt or a fast flick) and brought back by the Now Playing bar.
- Choose a sound is a FULL PAGE (Dark Noise's Select Noise): gear left, title,
  plus right; FAVOURITES (drag handle, filled heart) then seven families; rows
  60 with a 44 icon well; locked rows show a padlock; a Now Playing bar at the
  bottom (tile, caption, name 24, 56pt light play disc) returns to the player
- catalogue: 32 synthesized loops; the nine originals at 44.1 kHz / 24 s, the
  rest 12 s at 32 kHz; 32 MB total

## Motion
- press .97 at 150ms on the disc and rows; dot fades over 300ms
- sheet 350 strong ease-out in, 250 standard out
- drag to reorder favourites: long-press or grip, `react-native-draggable-flatlist`

## Hierarchy read
The disc is the subject by size, depth, and the only colour. The name sits
above it so the eye reads "what, then do". The list is a sheet, so the first
screen never becomes a catalogue.

## The lesson, as a rule
"When a praised product in the category already has the structure your users
expect, take the structure and compete on craft; a novel control has to beat a
tap, and almost nothing does."

## Confidence
Measured from source. Verified on Expo web: sheet, search, pick, heart. Drag
reorder and the native build are verified separately in the session log.

## Monetisation (copied from Dark Noise)
Two free sounds, padlocks on the rest, paywall on first play (swipe down to
continue), on any locked row, and from the plus. $19.99 a year, one week free.
The lesson generalises: in a category with a praised leader, the business
model is also a solved problem. Copy it, then earn the difference in craft.
