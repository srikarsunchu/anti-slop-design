# Companion skills

anti-slop-design decides what a thing should look like. Since September 2026 it
sits next to a set of skills that decide how a thing should move and how a
component should be built. They are not vendored here; install them beside
this one and let the handoffs below route the work.

## Emil Kowalski's skills (MIT)

Source: https://github.com/emilkowalski/skills. Install by copying each skill
folder into `~/.claude/skills/`. The set, and what each is for:

| Skill | Use it when |
|---|---|
| `emil-design-eng` | Polish pass on any component: the invisible details, what to cut |
| `animate` | Building a web animation from scratch: purpose, properties, curve, interruption, exit |
| `animate-expo` | Same decisions in React Native / Expo: Reanimated, Gesture Handler, haptics |
| `review-animations` | Critiquing motion in a diff against a craft bar. Flags by default |
| `improve-animations` | Auditing a whole codebase's motion and writing plans for another agent |
| `find-animation-opportunities` | Read-only search for places that should animate and places that must not |
| `animation-vocabulary` | Naming an effect someone described vaguely |
| `mobile-native` | Making a web app feel installed on a phone: 100vh, tap highlight, zoom-on-focus, safe areas |
| `ask-sonner` | Anything about Sonner toasts |
| `pick-ui-library` | Choosing a library for a frontend problem (explicit invocation only) |
| `prototype` | Building several genuinely different versions behind a picker (explicit invocation only) |

## apple-design

Apple's WWDC design guidance translated for the web: springs, gesture-driven
sheets, momentum, interruptible transitions, translucent materials, optical
sizing. Ships in the same pack. Use it when the reference is an Apple surface
or the interaction is drag, swipe, or a sheet.

## motion-primitives

The ibelick/motion-primitives catalog (accordion, dock, spotlight,
morphing-dialog, text effects, tilt, carousel, and the rest) bundled as a
local skill with the component source and the shadcn registry. Use it when a
brief names one of those components; it is a library in the sense of
`libraries/usage.md`, so it counts as a trusted solution to a solved problem.

## How the handoff works

The brief in `methods/brief.md` is still written first, here. Then:

| The brief says | Hand to |
|---|---|
| a component needs motion beyond the ladder in `principles/motion.md` | `animate` |
| the surface is Expo / React Native and something moves or is dragged | `animate-expo` |
| the reference is Apple, or the interaction is a sheet, swipe, or drag | `apple-design` |
| the surface is mobile web or a PWA | `mobile-native`, after `surfaces/mobile.md` |
| a diff with animation is being reviewed | `review-animations` |
| "make this feel more alive" | `find-animation-opportunities`, then this skill's gates decide what survives |
| a named Motion Primitives component | `motion-primitives` |
| a toast | `ask-sonner` |

The gates in `SKILL.md` still apply to whatever comes back. Two curves, a
duration ladder, reduced motion guarded, nothing bouncing for attention.
When a companion proposes a spring or a bounce, it has to explain the change
it makes legible; otherwise it is decoration, and `principles/motion.md`
cuts it.
