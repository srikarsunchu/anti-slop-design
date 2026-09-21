# iOS dark grouped UI — Settings, Clock, the system's own dark tables

Source: Apple Human Interface Guidelines (Color, Typography), UIKit semantic
colors as rendered on iOS 17 to 26 dark mode. Extracted 2026-09-04 from the
documented system values; these are Apple's numbers, not guesses.

## The one idea
"A table is a stack of decisions." Each grouped cell is one setting: label on
the left, value on the right, chevron if it opens. The user scans the left
edge and reads the right edge.

## Type (per role)
| Role | Face | Weight | Size | Tracking | Line-height | Color |
|---|---|---|---|---|---|---|
| large title | SF Pro Display | 700 | 34 | 0.4 | 41 | label |
| title 2 | SF Pro Display | 400/700 | 22 | 0.35 | 28 | label |
| body (row label) | SF Pro Text | 400 | 17 | −0.41 | 22 | label |
| subheadline (row detail) | SF Pro Text | 400 | 15 | −0.24 | 20 | secondary |
| footnote (section footer) | SF Pro Text | 400 | 13 | −0.08 | 18 | secondary |
| caption (section header) | SF Pro Text | 400 | 13, caps | −0.08 | 18 | secondary |

## Color (dark, elevated = grouped)
- ground: systemGroupedBackground #000000
- surfaces: secondarySystemGroupedBackground #1C1C1E (cells),
  tertiarySystemGroupedBackground #2C2C2E (nested)
- ink / secondary / tertiary: label #FFFFFF / secondaryLabel rgba(235,235,245,.6)
  / tertiaryLabel rgba(235,235,245,.3), quaternary .18
- separator: rgba(84,84,88,.6), 1/scale pt, inset to the text edge
- accent: systemBlue #0A84FF for interactive text; toggles systemGreen #30D158
- status colors: red #FF453A, orange #FF9F0A, green #30D158
- count of distinct colors: three surfaces, four label levels, one accent,
  status set

## Ground
Flat black. The system gets away with it because every screen is full of
cells; there is no void. A third-party app with less content needs a ground.

## Icons
SF Symbols, regular weight, 17 to 20pt in rows, in a 29pt colored square in
Settings. The chevron is `chevron.right` at 14pt, tertiary.

## Layout
- content max-width: full width
- edges: 16 (cell inset from screen), 16 (text inset inside cell); 20 on iOS 26
- spacing scale observed: 8 / 16 / 35 (between groups)
- radii: 10 (iOS 15 to 18), 26 concentric on iOS 26 grouped cells
- rows: 44 minimum; 52 to 56 with a detail line

## Motion
- curves: system springs; sheet presentation ~350ms
- durations: push 350, sheet 350 to 400
- notable interactions: cell highlight on touch is a tint change (nested
  surface), not a scale

## Depth
- sections / panels: grouped tables all the way down
- how many show the product working: every cell shows its current value
- how many animate: toggles, sheet, push

## Hierarchy read
Left edge = what, right edge = current value. Section headers are caps
footnote, tertiary. Position and weight agree everywhere; the only emphasis
is the large title.

## The lesson, as a rule
"Grouped cells show the current value on the right edge, so any settings-like
row should read as label · value · affordance and never make the user open it
to learn its state."

Second: "Apple's dark greys are four label levels on three surfaces; borrow
the ratios, then warm or cool them toward your ground so the app is not
mistaken for Settings."

## Confidence
Measured: colors, type sizes, line heights (Apple documented). Radii on
iOS 26 vary by device; check on the simulator.
