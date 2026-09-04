# Icons and marks

## Never type path coordinates from memory

Guessed bezier numbers look wrong every time, and icons are the most visible
place a page breaks. Get the real path.

Order of preference:

1. The real SVG from the published package. For Lucide:
   `https://cdn.jsdelivr.net/npm/lucide-static@<version>/icons/<name>.svg`.
   Check the version with `npm view lucide-static version`. Heroicons,
   Phosphor, Tabler, and Radix are all on the same CDN.
2. The site's DOM if replicating a site. Read the `<svg>` grammar first:
   viewBox 24, stroke 2, round caps is Lucide. viewBox 24, stroke 1.5 is
   Heroicons outline. That fingerprints the set, then pull those paths.
3. A raster tracing harness: ghost the PNG at 35% opacity inside an SVG at
   the icon's viewBox, draw over it, delete the image.

There is no fourth option where guessing is right.

## Match the set's grammar

One set per page. Same stroke width, same caps, same corner style. Mixing a
Lucide chevron with a Heroicons check looks off even when each is correct.

## Size by role

About 14px in navigation and inline text, about 20px in cards, 24px for
feature icons. An icon that gets mangled when shrunk was drawn at the wrong
weight for that size. Give every icon a 44px tap target on touch surfaces.

## Logos and bespoke marks

This is where pages actually break. Utility icons are usually fine; the logo
is a hand-drawn bezier and looks wonky.

1. Use the real brand asset. Pull it from the repo, the app bundle, the DOM,
   or the press kit.
2. If none exists, build from exact geometric primitives: circles, rects,
   lines, arcs with computed points. Exact geometry cannot look wonky.
3. Monochrome, or a color derived from the brand.

A hand-typed `<path d="M... C...">` for a logo is a bug.

## Verify by looking

Render every icon and look at it at its real size. A mangled icon shows in
pixels, never in code.
