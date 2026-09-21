# Diffusion Studio — the bar for an agent-native editor landing page

Source: https://diffusion.studio/ live DOM and screenshots at 1200 and 1440 wide, 2026-09-14.

## The one idea
"Turn your agent into a video editor." The thing that embodies it is a macOS dock of real agent app icons (Claude Code, Codex, Cursor, Claude, Gemini) floating over a planet at sunrise. The idea is an object on the first screen.

## Type (measured)
| Role | Face | Weight | Size | Tracking | Line-height | Color |
|---|---|---|---|---|---|---|
| h1 | Geist Variable | 470 | 52 | -1.3px | 57.2 | oklch(.946 0 0) |
| h2 | Geist Variable | 470 | 36 | -0.9px | — | same |
| body | Geist Variable | 400 | 18 | 0 | 29.25 | oklch(.66 0 0) |
| button | Geist | 400 | 12 | 0 | 32px tall | oklch(.946) on oklch(.254) |
| mono | Geist Mono | 400 | 14 / 11.9 | 0 | — | 30–45% white for shell noise, 100% for the command |

One weight for every heading. Body is large and grey. Buttons are tiny.

## Color
- ground: oklch(0 0 0), pure black
- ink: oklch(.946 0 0); secondary oklch(.66 0 0)
- accent: none. Every color on the page comes from imagery: sunrise, rocket exhaust, a lamp, a sunset wallpaper.
- count: two greys, no accent, no status colors.

## Ground
Every section has a cinematic ground. Hero: 3840px HEVC loop of a planet limb at sunrise. Section 2: the editor playing a real spaceflight documentary at 1152px wide. Section 3: a looping camera move across the project's TSX source, tilted, with depth of field. Feature cards: blurred colored wallpapers behind product panels. Closing: a dark satin swirl behind an install command.

## Layout
- content max-width 1152 at 1200 viewport (96%); 128px section padding; no borders anywhere
- product images at full column width; feature panels 373 wide in threes
- stats band: four flat tiles, one value each, no icons

## Motion
Three muted looping videos, all autoplay, none decorative. Nothing else animates.

## Copy
Two sentences per section. "Or don't do any of it yourself. Just ask your agent." Alt text is a full sentence describing the scene.

## Depth
10 sections: hero, editor, open source (code shot), canvas, generate, design, speed, Mac, FAQ, try. Product shown working in 7. Three move.

## The lesson, as a rule
"Film the product and film the code. A code block in a card is documentation; a camera move across the source with depth of field is footage, and footage is what makes a claim feel true."

Second: "One heading weight, one grey for body, no accent. Let the imagery carry all the color."

## What to refuse
Their dock idea and their space imagery are theirs. Take the method (film everything, one weight, no accent), not the shots.
