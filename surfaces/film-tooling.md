# Film and video tooling

Editors, shot lists, timelines, review tools, color panels. The references
are Resolve, Premiere, Frame.io, Avid, and the good indie tools.

## Dark chrome is the convention, and it has rules

- Ground #101010 to #1a1a1a. Panels one or two steps lighter. Never #000.
- Text #e8e8e6, secondary at 60% white, tertiary at 40%.
- One accent, used for the playhead, the selection, and the primary action.
  Resolve uses a warm orange for the playhead; Premiere uses blue. Pick from
  the brand, not from those.
- Green and red for clip status and warnings only.

## Timecode and numbers

Mono, tabular, always. `01:02:14:08` reads as machinery. Frames, fps, lens
lengths, f-stops, shot numbers: all mono. The sans is for names and
descriptions only.

## The timeline

- Tracks 32 to 48px tall. Clips with 4px radius and a 1px darker edge.
- The playhead is the one high-contrast vertical on the surface.
- Ruler ticks in mono at 10 to 11px.
- Snap indicators and range selections use the accent at low alpha.

## Panels

Dense, tabular, keyboard-driven. Rows 28 to 32px. Every row has a status,
a duration, and a name. Populate with a real scene: shot numbers like 14A,
lenses like 85mm, moves like "slow push".

## Video content

Real frames when possible. If not, a dithered or gradient placeholder in the
scene's palette, never a grey box with a play icon. Thumbnails at 16:9 with
a 2px radius.

## Motion

Scrubbing is instant. Panel transitions 200ms. Nothing bounces. Playhead
movement is linear because it is constant motion.

## Verify

Check the accent count. Check every timecode is tabular mono. Check the
playhead is the highest-contrast element on the timeline. Screenshot at
1440 wide because these tools are used on large screens.
