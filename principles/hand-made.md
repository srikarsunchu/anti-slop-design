# What "hand-made" actually means

A page reads as hand-made when it carries evidence of decisions. A page reads
as generated when every choice is the median choice. The tells below are the
median choices. Each has a fix.

## The tells, and the fix for each

| Tell | Why it reads as generated | Fix |
|---|---|---|
| Centered column, three equal cards with a small icon each | It is the single most common layout in the training set | Asymmetry with a reason: one anchor, uneven columns, a table instead of cards |
| Pure #000 text on pure #fff | No designer picks those; they pick greys on off-white | Ink #292929 on #f9f9f8 or the reference's pair |
| Default sans, default weight, default tracking | Unset values are the median | Named face, 400/500 only, negative tracking on display |
| Weak brand color on every card, icon, and divider | Color without a reason | Monochrome; accent only where it means something |
| Hero = headline + one button + empty space | Nothing earns the whitespace | The product doing its job on real data, or a rich ground |
| "Feature 1", lorem, "John Doe", $99 | Placeholders show no one lived in the page | Specific names, real-looking numbers, a scenario |
| Gradient in one corner, three flat corners | One radial fading to a flat base | Full-surface gradient, mesh, or none |
| Purple-to-blue gradient anything | The 2023 AI default | Never |
| Freehand icon paths that look slightly wrong | Coordinates from memory | Real paths from the package |
| Every element bounces or fades in | Motion as decoration | Two curves, a ladder, motion only where it explains something |
| Even spacing everywhere, 24px between all things | No rhythm | A spacing scale with big gaps between sections and tight gaps within |
| Same font size for label, body, and button | No hierarchy | Three sizes within 2px plus one big jump |
| Borders on every box | Divider noise | Tint shifts and radius |
| Bold on every heading and label | Bold-spam | Medium for headings, regular for everything else |
| A logo that is a hand-drawn bezier | Guessed geometry always looks off | Real asset, or exact primitives (circles, rects, arcs) |

## What hand-made pages have that generated ones lack

- **A point of view in the copy.** "Not a stale database." Names competitors.
  Short sentences. Specific nouns.
- **One repeated motif.** A texture, a shape, a color moment that shows up in
  the hero, a card, the footer. Repetition of one idea is identity.
- **Optical corrections.** An icon nudged 1px to look centered. A heading
  hanging punctuation. Numbers set tabular so columns do not jitter.
- **A ground.** Something behind the UI that a person chose: a photo, a
  dither, a paper texture, a dense data surface.
- **Edges that agree.** Every left edge on the page sits on one of two or
  three x positions. Measurable. See `methods/verify.md`.
- **Restraint where it counts, richness where it counts.** The UI is quiet.
  The world behind it, or the data inside it, is full.

## Rule

Before shipping, find three decisions on the page that a template would not
have made. If you cannot, it is a template.
