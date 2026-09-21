# Examples

Full builds made under this method. Use them to calibrate what "done" looks
like, and as a source of working snippets (the dither canvas, the grid-rows
accordion, the line-draw check).

- `slate-landing.html` — a nine-section landing page for a fictional shot-list
  tool. Monochrome dither ground, Geist, Lucide, one green for state. Ground
  truth in `references/slate-landing.md`.
- Lull (`~/workspace/lull`, not vendored here) — an Expo app for new mothers:
  a player with one big play disc (the amber dot is the only colour) and a
  sound list one pull away, with favourites, search, a night log, timers that
  fade, a Live Activity and widgets. The structure follows Dark Noise's pages;
  a rotary-dial direction was built hi-fi and dropped the same day. Ground truth
  in `references/lull-player.md`; the lesson in `principles/mobile-tells.md`.

Serve any of them with:

```bash
python3 -m http.server 8765 --directory examples
```

Add a new example whenever a build under this method is worth keeping, and
write its reference file at the same time.
