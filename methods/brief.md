# The brief

Fill this in, in the conversation, before writing any markup. Saying it out
loud is the point: a wrong brief is cheap to correct; a wrong build is not.

```
IDEA        This design's idea is ___.
ANCHOR      The thing on the page that IS the idea is ___.
SURFACE     landing | product-ui | mobile | film-tooling
REFERENCE   <named real site or screen>
  face      ___ (weights ___, display tracking ___, UI tracking ___)
  greys     ink ___ / secondary ___ / tertiary ___ on ground ___
  accent    ___ (from ___) | none
  ground    photo | dither | mesh | texture | dense data
  motion    curves ___ / hover ___ms / reveal ___ms
  icons     <set> (viewBox __ / stroke __ / caps __)
GRID        edges ___ | spacing ___ | type scale ___
DEPTH       __ sections, __ show real data, __ animate
DIM         (mobile) at minimum brightness the screen shows ___; the tappable thing is ___
SCENARIO    <two sentences of the demo data's story>
ACCEPTANCE  "Done when ___."
```

## Filling it well

- If the reference is unknown, pick one now from `references/` or ask. Do not
  build without one.
- If the accent's source is "habit", write "none".
- The scenario must be specific enough to fill a table from.
- The acceptance sentence is measurable: "every left edge sits on x=24 or
  x=1056", "hero text passes 4.5:1 over the dither", "resembles creed's hero
  in a side-by-side".

## Then

Go to `methods/grid-contract.md`, then build, then `methods/verify.md`.
