# Product and app UI

Dense tools: dashboards, editors, admin panels, settings.

## Density is the ground

There is no photo. The richness is the data. Every panel is populated with a
believable state. Empty states are designed with a short sentence and one
action, never a blank area.

## The quiet spec

- Type: 12 / 13 / 14 for UI, one 20 to 24 title. Tracking −0.15px. Tabular
  numerals everywhere numeric.
- Greys: three levels of text, three levels of surface. Group with a 3% tint
  shift and 8 to 12px radius, not borders. Hairlines only where rows need
  separating.
- Icons: 14px in nav and rows, 16 to 20 in toolbars. One set.
- Radii: 6 to 8 on controls, 12 to 16 on panels, pill on primary actions only.
- Spacing: 4 / 8 / 12 / 16 / 24. Rows 32 to 40 tall.

## Selection and state

Selected items get two or three reinforcing signals: a tint, a hairline, an
indicator. Never a color change alone. Only the selected item expands to show
detail; the rest collapse to one line.

Color: one accent for the primary action and selection. Green for success,
red for destructive and error. Grey for everything else including loading.

## Machinery text

Mono caps for labels that describe the system: shortcuts, IDs, timecodes,
units, statuses. It separates message from mechanism.

## Solved problems

Command palette: cmdk. Toasts: Sonner. Long lists: Virtuoso. Reorder: dnd-kit.
Counters: NumberFlow. See `libraries/usage.md`.

## Motion

Hover 100 to 150ms standard. Panel open 300ms decelerate. Nothing on page
load except a fade. Press scale on every button.

## Layout

One grid parent with named columns for any sidebar-plus-content layout. Label
columns share one edge; value columns share one edge. The verify script
counts them.
