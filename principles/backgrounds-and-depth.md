# Backgrounds and depth

## Clean is not sparse

Restraint belongs in the UI. Richness belongs in the ground or the content.
The great references are quiet per element and full per page. A page that is
quiet per element and empty per page is a void.

## Two ways to escape the void; pick at least one

**A. A rich ground.** A full-bleed photo, a dither field, a mesh, a paper
texture. Clean monochrome UI floats over it. The contrast between the
disciplined UI and the living backdrop is the whole feeling.

**B. Dense real-data content.** Clean off-white, no photo, but every section
shows the product working on specific believable data: a table with real
rows, a schedule with times, stat tiles with plausible numbers.

A page that has neither is a template.

## Ground techniques

- **Photo.** Saturated, emotional, full-bleed. Sample the accent from it.
  Never a stock illustration.
- **Dither / stipple.** A canvas field where dot density carries the fade, in
  one hue family. Draw once, redraw on resize, never per frame. See
  `examples/slate-landing.html` for a working monochrome version.
- **Aurora / mesh.** Three to five analogous pastel radial blobs covering the
  whole surface, a blurred copy behind, a grain overlay at 5% to kill banding.
  Base color inside the family so no corner is flat.
- **Texture.** Faint diagonal hatching, paper grain, a subtle grid. Depth
  without shadows.

Always: text over any ground gets a contrast check. Move the crest, add a
scrim, or move the text. A dither is brightest at its crest; do not put a
ghost button there.

## Depth budget

- Marketing site: 8 to 12 sections. The product shown working in most. At
  least three that move. Hero with a real anchor, stats band, how-it-works
  with mini demos, a full-width product demo, setup steps, integrations, FAQ,
  closing CTA.
- Product UI: every panel has a populated state. Empty states are designed,
  not blank.
- Mobile: each screen has one subject; density comes from real content, not
  more chrome.

## Rule

Before shipping, name the ground. If the answer is "white", the page needs
either a ground or a lot more real data.
