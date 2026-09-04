# Extracting ground truth

Never guess a value that can be measured. This applies to fonts, colors, icon
sets, spacing, motion, and to aesthetic qualities like ratios and what
touches what.

## From a live site

Open it in the browser pane and run in the console:

```js
// type per role: pick the elements, read computed styles
[...document.querySelectorAll('h1,h2,p,button,a,code')].slice(0,30).map(e=>{
  const s=getComputedStyle(e);
  return [e.tagName, s.fontFamily.split(',')[0], s.fontWeight, s.fontSize,
          s.letterSpacing, s.lineHeight, s.color].join(' | ')
})
```

```js
// colors used, counted
Object.entries([...document.querySelectorAll('*')].reduce((m,e)=>{
  const s=getComputedStyle(e);
  for (const c of [s.color, s.backgroundColor, s.borderColor]) m[c]=(m[c]||0)+1;
  return m},{})).sort((a,b)=>b[1]-a[1]).slice(0,20)
```

```js
// icon set fingerprint
[...document.querySelectorAll('svg')].map(s=>[s.getAttribute('viewBox'),
  s.getAttribute('stroke-width'), s.getAttribute('stroke-linecap')].join('/'))
  .reduce((m,k)=>(m[k]=(m[k]||0)+1,m),{})
```

```js
// motion vocabulary
[...new Set([...document.querySelectorAll('*')].flatMap(e=>{
  const s=getComputedStyle(e);
  return [s.transitionTimingFunction, s.transitionDuration]}))].slice(0,30)
```

Also record: page height and section count, max-width of the content column,
the background treatment of the hero and footer, the exact hero headline
size and tracking.

## From a screenshot or video

- Write down five measurable properties before touching code: ratios,
  what is visible at rest versus hover, edges counted, colors counted, the
  marker-to-content ratio in dense overlays.
- Identify the face from distinctive glyphs.
- Sample colors with an eyedropper, not by eye.
- For video, seek frames at the key states and read them individually.

## Recording it

Put the result in `references/<name>.md` using `references/TEMPLATE.md`.
Text and numbers only. Do not commit third-party images.

## Rule

If you are about to type a font name, hex, path, or duration you did not
read from a source, stop and go read it.
