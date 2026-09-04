# Motion

A small, consistent vocabulary is what reads as polished. Two curves, one
duration ladder, applied everywhere.

## The curves

- **Standard** `cubic-bezier(0.4, 0, 0.2, 1)`: hover color, background,
  border. 100 to 150ms. The default.
- **Strong ease-out** `cubic-bezier(0.16, 1, 0.3, 1)` or
  `cubic-bezier(0.22, 1, 0.36, 1)`: the nice moves. Card lift, reveal, line
  draw, expand. 300 to 700ms. Starts fast, glides to a stop.
- **Decelerate** `cubic-bezier(0, 0, 0.2, 1)`: things entering or growing.
  Accordion open. 300ms.

Never default `ease` or `linear` on UI. Never `ease-in` on anything
interactive.

## Duration ladder

| Move | ms | Curve |
|---|---|---|
| hover color / bg / border | 100–150 | standard |
| transform on press, chevron flip | 200 | standard |
| accordion open | 300 | decelerate |
| card hover lift | 400 | strong ease-out |
| large expand | 420 | strong ease-out |
| SVG line draw | 680 | strong ease-out |
| entrance of a hero anchor | 800 | strong ease-out |

The bigger and rarer the move, the longer and softer. Frequent micro-moves
stay short.

## Recipes

- **Press.** `:active { transform: scale(.97) }` with a 150ms transition on
  every pressable thing.
- **Accordion.** Animate `grid-template-rows: 0fr → 1fr` plus opacity. Chevron
  rotates 180deg at 200ms standard.
- **Line draw.** `stroke-dasharray` equal to path length, animate
  `stroke-dashoffset` to 0 at 680ms.
- **Card lift.** Transition box-shadow, border-color, and background together
  at 400ms. No scale.
- **Scroll reveal.** IntersectionObserver adds a class once; never animate on
  every scroll event.
- **Counters.** NumberFlow, never hand-rolled digit animation.

## Layout and motion never share `transform`

Center with `left:0; right:0; margin:0 auto` or flex/grid, so the transform
channel is free for animation. Centering with `translateX(-50%)` and then
animating transform breaks the centering when the animation ends.

## Reduced motion

```css
@media (prefers-reduced-motion: reduce) {
  .animated { animation: none; transform: none; opacity: 1; }
  * { transition-duration: .01ms !important; }
}
```

Keep opacity and color; drop transforms. Check `matchMedia` in JS before
starting any scripted animation.

## Rule

Motion explains a change or gives tactile feedback. Motion that only asks for
attention is decoration. Cut it.
