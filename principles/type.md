# Type

## Extract, never guess

Replicating a live site: read `getComputedStyle` for family, size, weight,
letter-spacing, line-height, color per role. From a screenshot: zoom into
distinctive glyphs (a, g, R, the numerals) to identify the face.

## The four settings that make type look chosen

1. **Tracking.** Display sizes get −0.02em to −0.03em. UI text gets −0.15px.
   Untouched tracking is the single most-skipped detail.
2. **Color.** Dark grey, never #000.
3. **Numerals.** `font-variant-numeric: tabular-nums` on anything in a column,
   badge, timecode, or counter.
4. **Line-height per size.** 1.1 for display, 1.3 for headings, 1.5 for body.

## Scale

Three UI sizes within 2px of each other (12, 13, 14) and one big jump for the
title (28 to 56). Hierarchy comes from the gap, not from six sizes. Nothing in
between.

## Roles

One face per role, and roles are the only reason to add a face:

- UI and body: one sans. Geist, Inter (tuned), or the reference's.
- Display: optional serif for editorial tone. The scale gap between a serif
  display and a small sans label is the hierarchy.
- Meta and machinery: one mono, small caps, wide tracking. Timecodes, labels
  like PER SEAT / MONTH, file paths, shortcuts.

Weights: 400 and 500. Add 600 only for a display face that needs it. Never 700
on UI.

## Loading fonts

Google Fonts is fine for prototypes; self-host for anything shipped. Always
give a real fallback stack. Set `font-display: swap`.

## Rule

If the font, weight, and tracking are the defaults, the page will look
generated regardless of everything else.
