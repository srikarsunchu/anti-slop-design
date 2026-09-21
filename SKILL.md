---
name: anti-slop-design
description: Sri's personal design method (anti-slop-design) for building UI with AI that feels hand-made. Use for any visual work — landing pages, product/app UI, mobile screens, film and video tooling, dashboards, docs sites. Loads a brief template, hard gates, and a verify step. Has no house style; it makes the output resemble a real, named reference and reads as crafted by a person.
---

# anti-slop-design

A method, not a theme. The goal of every build is that a designer looks at it
and cannot tell a model made it. That happens when three things are true:

1. The page has **one idea**, and you can point at the thing that embodies it.
2. Every value was **taken from a real reference**, not invented.
3. Someone **looked at the pixels** before calling it done.

Read `principles/hand-made.md` first. It lists the tells that give a generated
page away. Everything else in this repo exists to remove those tells.

## Before any markup — write the brief (mandatory)

Fill in `methods/brief.md` in the conversation, out loud, before writing code:

- **Idea.** "This design's idea is ___." One sentence. If you cannot name it,
  you are not ready to build.
- **Reference.** A real, named site or screen. Its font, weights, tracking,
  greys, accent, background treatment, grid, motion. Use
  `methods/extract-ground-truth.md`. Stored references live in `references/`.
- **Surface.** Which of `surfaces/` applies: landing, product UI, mobile, film
  tooling. Read that file.
- **Grid contract.** Edges, spacing scale, type scale. Three lines. See
  `methods/grid-contract.md`.
- **Depth budget.** How many sections or panels, how many show real data, how
  many move.
- **Dim budget** (mobile only). What the screen looks like at minimum
  brightness, and which one thing must still be tappable. See
  `surfaces/mobile.md` and `principles/mobile-tells.md`.

## Hard gates

Violating one of these makes the output generated-looking. Check every time.

1. **No accent by habit.** Derive the accent from the reference or brief, or
   stay monochrome. Color carries meaning only: state, action, selection,
   scarcity. Never purple or indigo as a default. Never orange as a default.
2. **Real icons, real marks.** Pull Lucide, Heroicons, Phosphor, or the brand's
   own SVG from the published package or DOM. Never type path coordinates from
   memory. Never freehand a logo. `principles/icons-and-marks.md`.
3. **A real ground.** Either a rich backdrop (photo, dither, mesh, texture) or
   dense real-data product content. A flat white void with three cards is the
   number one tell. `principles/backgrounds-and-depth.md`.
4. **Real data in demos.** Every product mock shows specific, believable
   content: names, timecodes, prices, file names. Never lorem, never
   "Feature 1".
5. **Real motion values.** Two easing curves, a duration ladder, reduced-motion
   guarded. Nothing bounces for attention. `principles/motion.md`.
6. **Trusted libraries for solved problems.** Toasts, command menus, OTP, drag
   and drop, virtual lists, animated numbers. `libraries/usage.md`.
7. **Text stays legible over texture.** Any text over a photo, dither, or
   gradient gets a contrast check. Move the crest, add a scrim, or move the
   text. `methods/verify.md`.
8. **Look before you ship.** Render, screenshot, compare to the reference side
   by side. Run the anti-slop checklist. No "done" without eyes on pixels.

## The quiet defaults (adapt to the reference, never ship as-is)

- Type: three UI sizes within 2px (12/13/14) plus one big jump (28–56). Hierarchy
  is the gap. Tracking −0.15px on UI, −0.02em on display. One face per role.
  Weights 400 and 500 only.
- Greys, no pure black: #292929 primary, #5D5D5D secondary, #9E9E9E tertiary.
- Radii ladder: 8 for nav items, 16 for cards, pill for primary CTAs.
- Group with a 3% tint shift and radius, not borders.
- Tabular numerals on anything numeric. Mono caps for machinery text.

## Reach for a library

| Building | Use |
|---|---|
| number that changes | NumberFlow |
| ⌘K / searchable list | cmdk |
| toast | Sonner |
| OTP field | input-otp |
| live tuning panel | Leva |
| 100+ row list | react-virtuoso |
| drag to reorder | @dnd-kit |
| streaming chart | Liveline |
| a named Motion Primitives component (dock, spotlight, morphing dialog…) | `motion-primitives` skill |

Verify versions with `npm view <pkg> version` before trusting the snippets.

## Companion skills

Motion and component craft are handed to skills that sit beside this one;
the brief and the gates stay here. `companions.md` has the full map. Short
form: web motion beyond the ladder goes to `animate`, Expo motion to
`animate-expo`, Apple-style sheets and gestures to `apple-design`, mobile web
feel to `mobile-native`, reviewing motion in a diff to `review-animations`,
a polish pass to `emil-design-eng`. Whatever comes back still passes gate 5.

## Process

0. Brief (above). Say it in the conversation.
1. Grid contract, then wireframe: where the anchor goes, where the ground goes.
2. Build monochrome. Add color last, only where it means something.
3. Pull real icons and library snippets.
4. Add the ground and the depth.
5. Verify: screenshot, contrast check, alignment check, checklist. Fix. Repeat.
6. If the user gave a reference, digest it into `references/` using
   `methods/digest-a-reference.md` so the lesson survives the session.

## Folders

- `principles/` — the taste. Read all on load. Each file is one lesson with a rule.
- `methods/` — how to work: brief, extraction, grid, verify, digest.
- `surfaces/` — what changes per surface: landing, product UI, mobile, film tooling.
- `references/` — ground truth from real designs, stored as text and numbers.
- `libraries/` — verified snippets for the trusted libraries.
- `examples/` — full builds made under this method, for calibration.
- `checklists/` — the pre-ship gate.
- `companions.md` — the motion and component skills installed beside this one, and when to hand off.

For Elide work specifically, the brand system at `~/workspace/design-system`
is the reference. Extract from it; do not restyle it.
