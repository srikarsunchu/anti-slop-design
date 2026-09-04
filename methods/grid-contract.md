# The grid contract

"Align things" changes nothing. Declaring the grid before markup changes the
order of work, and that is what produces alignment.

## Declare three lines first

```
edges     content-left = 24px | content-right = width − 24px | (optional) label col = 120px
spacing   4 / 8 / 12 / 16 / 24 / 32 / 48 / 96   — nothing else
type      12 / 13 / 14  +  32 (display)          — nothing else
```

Adapt the numbers to the reference. Then do not deviate. No `margin-left:
17px`. No `font-size: 15px`.

## Build alignment structurally

One `display: grid` parent with named columns gives every row the same edges
for free. Tables for tabular content. Never per-element margins hoping they
add up.

## Section rhythm

Big gaps between sections (96), medium within a section (32 to 48), tight
inside a component (8 to 16). Rhythm is the contrast between those, not equal
spacing everywhere.

## Verify

`methods/verify.md` has a script that counts distinct left edges. If the
count exceeds what the contract defines, alignment is broken. That is a
machine check, not a feeling.
