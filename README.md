# anti-slop-design

My personal design method for building UI with AI that feels hand-made.
Packaged as a [Claude Code](https://claude.com/claude-code) skill.

It has no house style. It is a way of working: name one idea, take every value
from a real reference, build quiet UI over a rich ground or dense real data,
and look at the pixels before calling it done.

## What's in the repo

```
SKILL.md          entry point: the brief, hard gates, quiet defaults, process
principles/       the taste, one lesson per file, each ending in a rule
methods/          how to work: brief, extraction, grid, verify, digest
surfaces/         what changes per surface
references/       ground truth from real designs, as text and numbers
libraries/        verified snippets for the trusted libraries
examples/         full builds under this method, for calibration
checklists/       the pre-ship gate
companions.md     which motion or component skill takes which brief
companions/       vendored copies of those skills (MIT), one folder each
```

### `SKILL.md`

The entry point. The mandatory brief (idea, reference, surface, grid
contract, depth budget, dim budget), eight hard gates, the quiet defaults,
the library table, the companion handoffs, and the build process.

### `principles/` — the taste

| File | Lesson |
|---|---|
| `hand-made.md` | Read first. The tells that give a generated page away, and the fix for each |
| `mobile-tells.md` | The phone's own tells: painted status bar, three-tab template, onboarding carousel, blob hero, tile grid, physical controls on glass |
| `one-idea.md` | One idea, made physical: you can point at the thing that embodies it |
| `type.md` | Three UI sizes within 2px plus one jump; tracking; weights 400 and 500; match text rendering too |
| `color.md` | No accent by habit; color carries state, action, selection, scarcity |
| `backgrounds-and-depth.md` | A real ground: photo, dither, mesh, texture, or dense real data. Never a white void with three cards |
| `icons-and-marks.md` | Real icons from the published package or DOM; never path coordinates from memory |
| `motion.md` | Two curves, a duration ladder, reduced motion guarded, and when to hand off to `animate` |
| `copy.md` | A verb and an object in the product's voice; no template voice |

### `methods/` — how to work

| File | What it does |
|---|---|
| `brief.md` | The fill-in template said out loud before any markup |
| `extract-ground-truth.md` | Reading font, greys, accent, grid and motion from a live DOM, a screenshot, or a video |
| `grid-contract.md` | Three lines declared first (edges, spacing, type), alignment built structurally, section rhythm |
| `verify.md` | Render and look, contrast over texture, alignment, color count, side by side with the reference, reduced motion, checklist |
| `digest-a-reference.md` | Turning a studied reference into a file in `references/`, and the failure of picking a direction from sketches alone |

### `surfaces/` — what changes per surface

| File | Covers |
|---|---|
| `landing.md` | Landing pages and marketing sites |
| `product-ui.md` | Product and app UI: density from three greys and real data |
| `mobile.md` | Phone apps on both platforms: one hand, interrupted attention, night; the dim state; the phone grid contract; system surfaces (lock screen, widgets, Live Activity, icon); building in Expo; the dim test |
| `film-tooling.md` | Film and video tooling: dark chrome, one accent, timecodes |

### `references/` — ground truth

Sixteen digested references plus `TEMPLATE.md` and an index in
`references/README.md`. No third-party images are committed; each file is
the numbers and the rule.

| File | What it is |
|---|---|
| `elide-brand.md` | Elide's own brand system; for Elide work, extract, don't restyle |
| `slate-landing.md` | The example build, as ground truth |
| `ios-dark-grouped.md` | Apple's dark grouped tables: greys, type ramp, row anatomy |
| `dark-noise.md` | The craft benchmark for a one-sound ambient app |
| `baby-sleep-category.md` | The anti-reference: why baby sleep apps read as templates |
| `lull-player.md` | Lull's shipped list + player structure |
| `lull-dial.md` | Superseded: the rotary-dial direction built and dropped in a day |
| `white-noise-listing.md` | A category leader's ten-shot App Store set, digested as structure |
| `behold.md` | Black ground, one photographic colour field per item |
| `lore-listing.md` | Four pastel store slides, serif claim, white-bezel phone |
| `rage-feed.md` | The quote category's cleanest wall: one screen, no tab bar |
| `clipping-agencies.md` | Eight clipping-agency landing pages measured at 1280 |
| `tradingview-dark.md` | TradingView's dark theme as the default trading-UI palette |
| `motion-so-frame.md` | Motion.so's shell, extracted for Frame |
| `diffusion-studio.md` | The bar for an agent-native editor landing page |
| `ghost-of-tsushima-hud.md` | Menus and HUD sampled from 1080p: three whites, one red |

### `libraries/usage.md`

Verified snippets and install lines for the trusted libraries: NumberFlow,
cmdk, Sonner, input-otp, Leva, react-virtuoso, dnd-kit, Liveline, plus a
React Native / Expo table (haptics, SVG grounds, sliders, sheets, Reanimated,
expo-audio, store review).

### `examples/`

`slate-landing.html`, a nine-section landing page for a fictional shot-list
tool built from a blank page under this method. Lull, an Expo app, is
described in `examples/README.md` but lives in its own repo.

### `checklists/anti-slop.md`

The pre-ship gate, one section per gate: idea, reference, color, ground and
depth, type, icons and marks, motion, copy, libraries, verification.

### `companions.md` and `companions/`

The handoff map and vendored copies of the thirteen skills it points at.
Every folder is a complete Claude Code skill with its MIT license.

| Skill | From | Use it when |
|---|---|---|
| `emil-design-eng` | Emil Kowalski | Polish pass on any component |
| `animate` (+ `RECIPES.md`) | Emil Kowalski | Building a web animation from scratch |
| `animate-expo` (+ `RECIPES.md`) | Emil Kowalski | The same in React Native / Expo |
| `review-animations` (+ `STANDARDS.md`) | Emil Kowalski | Critiquing motion in a diff |
| `improve-animations` (+ `AUDIT.md`, `PLAN-TEMPLATE.md`) | Emil Kowalski | Auditing a codebase's motion and planning fixes |
| `find-animation-opportunities` | Emil Kowalski | Where a UI should and should not animate |
| `animation-vocabulary` | Emil Kowalski | Naming a motion effect described vaguely |
| `mobile-native` | Emil Kowalski | Making a web app feel installed on a phone |
| `apple-design` | Emil Kowalski | Apple's springs, sheets, gestures and materials on the web |
| `ask-sonner` (+ `API.md`) | Emil Kowalski | Anything about Sonner toasts |
| `pick-ui-library` | Emil Kowalski | Choosing a library for a frontend problem (explicit only) |
| `prototype` (+ `PICKER.md`) | Emil Kowalski | Several genuinely different versions behind a picker (explicit only) |
| `motion-primitives` | ibelick | The 33 Motion Primitives components with source, hooks and registry |

## Install

```bash
git clone https://github.com/srikarsunchu/anti-slop-design ~/.claude/skills/anti-slop-design
cp -R ~/.claude/skills/anti-slop-design/companions/* ~/.claude/skills/
```

It loads on any UI work, or invoke it with `/anti-slop-design`.

## Companions

This skill decides what a thing looks like. Motion and component craft are
handed to skills installed beside it: Emil Kowalski's
[skills](https://github.com/emilkowalski/skills) (`animate`, `animate-expo`,
`review-animations`, `mobile-native`, `emil-design-eng`, and the rest),
`apple-design`, and a local `motion-primitives` bundle of
[ibelick/motion-primitives](https://github.com/ibelick/motion-primitives).
They are vendored under `companions/` with their licenses; `companions.md` says which one takes which brief.

## Growing it

When a build teaches something, write the rule into `principles/`. When a
reference is studied, record it in `references/` from the template. When a
build is worth keeping, put it in `examples/`. The repo is the memory; the
conversation is not.

## License

MIT.
