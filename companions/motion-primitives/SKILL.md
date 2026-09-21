---
name: motion-primitives
description: Add Motion Primitives components (React/Tailwind/Motion animated UI primitives from ibelick/motion-primitives — accordion, dialog, dock, spotlight, text effects, tilt, carousel, etc.) into a project. Use when the user asks to add, install, or use a "motion primitive", references motion-primitives.com, or wants a specific animated component from this catalog (e.g. "add the spotlight component", "add morphing-dialog").
---

# Motion Primitives

Source project: https://github.com/ibelick/motion-primitives (docs: https://motion-primitives.com)

A collection of React + Tailwind CSS + [Motion](https://motion.dev/) (framer-motion successor)
animated UI primitives. Components are plain `.tsx` source files meant to be copied into a
project (shadcn/ui-style registry), not installed as an npm package.

This skill bundles a local copy of every component's source so components can be added even
without network access. `registry.json` in this skill directory is the full upstream registry
metadata (name, description, deps, file list) for all 33 components.

## When to use this skill

- User asks to "add" / "install" a named component from this list (see catalog below).
- User references motion-primitives.com or ibelick/motion-primitives.
- User wants an animated UI primitive and doesn't already have a preferred library.

## Prerequisites for the target project

These components assume:
- React + Tailwind CSS already set up.
- The `motion` package installed (`npm install motion`). Some components also need
  `react-use-measure` (infinite-slider, toolbar-expandable, sliding-number).
- A `cn` utility at `@/lib/utils` (clsx + tailwind-merge). If missing, create one:

  ```ts
  // lib/utils.ts
  import { clsx, type ClassValue } from 'clsx';
  import { twMerge } from 'tailwind-merge';

  export function cn(...inputs: ClassValue[]) {
    return twMerge(clsx(inputs));
  }
  ```

- Import alias `@/` resolving to the project root (standard in Next.js/Vite templates with
  `tsconfig.json` paths configured).

## How to add a component

**Option A — shadcn CLI (preferred when the project already uses shadcn/ui and has network access):**

```bash
npx shadcn@latest add https://motion-primitives.com/c/<component-name>.json
```

This pulls the latest upstream version and auto-installs npm dependencies.

**Option B — copy the bundled source (offline / no shadcn setup):**

1. Look up `<component-name>` in the catalog table below to confirm dependencies.
2. Copy the file(s) from this skill's `components/core/<component-name>.tsx` into the target
   project's `components/core/` (or wherever the project keeps UI primitives — ask if unclear).
3. Some components additionally need a hook from this skill's `hooks/` directory
   (`useClickOutside.tsx`, `usePreventScroll.tsx`) — check the component's imports.
4. A few components (`toolbar-*`, `dialog`, `morphing-*`) also use base UI primitives copied
   into `components/ui/` here (`button.tsx`, `input.tsx`, `label.tsx`, `tooltip.tsx`) —
   copy any that the target file imports.
5. Ensure `motion` (and `react-use-measure` if required) is installed in the target project:
   `npm install motion` / `npm install react-use-measure`.
6. Fix import paths (`@/components/core/...`, `@/lib/utils`, `@/hooks/...`) to match the
   target project's structure.
7. Read the copied file and adapt Tailwind class names to the project's design tokens if it
   uses a custom theme.

Always read the component source in this skill before copying it in, so you can adapt props/
styling to what the user actually asked for rather than pasting it in blind.

## Component catalog

| Component | Description | Extra deps beyond `motion` |
|---|---|---|
| accordion | Collapsible content with smooth animations | — |
| animated-background | Animated background effect for UI elements | — |
| animated-group | Coordinated stagger animations for a group of children | — |
| animated-number | Animates number changes with smooth transitions | — |
| border-trail | Animated border trail around elements on interaction | — |
| carousel | Cycles through elements with smooth transitions | — |
| cursor | Custom animated cursor | — |
| dialog | Modal dialog with entrance/exit animations | — |
| disclosure | Shows/hides content with animated transitions | — |
| dock | macOS-style dock with scaling/movement effects | — |
| glow-effect | Glow effect that follows cursor movement | — |
| image-comparison | Interactive before/after image slider | — |
| in-view | Triggers animations when elements enter the viewport | — |
| infinite-slider | Infinitely looping slider | `react-use-measure` |
| magnetic | Magnetic attraction effect on hover | — |
| morphing-dialog | Dialog that morphs from its trigger element | — |
| morphing-popover | Popover that morphs from its trigger | — |
| progressive-blur | Progressive blur effect on elements | — |
| scroll-progress | Animated scroll-progress indicator | — |
| sliding-number | Slides between numbers on change | `react-use-measure` |
| spinning-text | Rotating/spinning text animation | — |
| spotlight | Spotlight effect following cursor movement | — |
| text-effect | Generic animated text effects | — |
| text-loop | Cycles through phrases with animation | — |
| text-morph | Morphs between text strings | — |
| text-roll | Rolling text animation | — |
| text-scramble | Scrambling text transition effect | — |
| text-shimmer | Shimmering text effect | — |
| text-shimmer-wave | Wave-like shimmer text effect | — |
| tilt | 3D tilt effect based on cursor position | — |
| toolbar-dynamic | Toolbar with dynamic interaction-based appearance | — |
| toolbar-expandable | Expandable toolbar revealing extra options | `react-use-measure` |
| transition-panel | Smooth transitions between panel states | — |

Full machine-readable metadata (exact file paths, categories) is in `registry.json`.

## Notes

- License: MIT (upstream `LICENCE.md`).
- Docs and live demos for each component live at `https://motion-primitives.com/docs/<name>`.
- If the user wants a component not in this catalog (upstream has added more since this skill
  was created), fetch it directly: `https://motion-primitives.com/c/<name>.json` (shadcn
  registry item JSON with inline file contents) or check the live GitHub repo.
