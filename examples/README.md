# Examples

Full builds made under this method. Use them to calibrate what "done" looks
like, and as a source of working snippets (the dither canvas, the grid-rows
accordion, the line-draw check).

- `slate-landing.html` — a nine-section landing page for a fictional shot-list
  tool. Monochrome dither ground, Geist, Lucide, one green for state. Ground
  truth in `references/slate-landing.md`.

Serve any of them with:

```bash
python3 -m http.server 8765 --directory examples
```

Add a new example whenever a build under this method is worth keeping, and
write its reference file at the same time.
