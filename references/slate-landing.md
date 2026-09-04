# Slate landing — the example build

Source: `examples/slate-landing.html`. Built 2026-09-04 from a blank page under
this method, as a calibration sample. A fictional shot-list product.

## The one idea
"Your film is a list of shots; the product is that list." The anchor is a
populated shot table, mid-shoot, with actual and estimated timings.

## Type
| Role | Face | Weight | Size | Tracking |
|---|---|---|---|---|
| display | Geist | 500 | 48 | −0.02em |
| heading | Geist | 500 | 32 | −0.02em |
| body / ui | Geist | 400 | 14 / 13 / 12 | −0.15px |
| meta | Geist Mono | 400 | 12 | +0.02em, caps |

## Color
- ground #f9f9f8, surface #f2f2f0, nested #ebebe8
- ink #292929 / #5D5D5D / #9E9E9E
- accent: none. Green #1f7a3a for "covered" only.
- dark sections #101010 with a monochrome dither.
- distinct colors: greys plus one green.

## Ground
Monochrome canvas dither in the hero and closing section. Density carries
the fade. Drawn once, redrawn on resize.

## Icons
Lucide 24 / 2 / round, fetched from lucide-static on the CDN. 14px inline,
20px in cards.

## Depth
Nine sections. Table, three mini demos, schedule, steps, FAQ. Three animate:
the hero anchor entrance, the checkmark line-draw, the schedule reorder.

## What the first render got wrong
- Anchor-styled buttons inherited an underline.
- The hero CTAs sat on the dither's brightest band and the ghost button was
  hard to read.

Both were caught by looking, not by reading code. That is why gate 8 exists.

## The lesson, as a rule
A monochrome dither is a legitimate ground and needs no accent. Text over any
generated texture needs a contrast check at the texture's brightest point.
