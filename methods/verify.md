# Verify

Rules that are not checked do not hold. Nothing ships without these.

## 1. Render and look

Serve the page and open it in the browser pane. Screenshot at 1280 wide,
then at 375 wide. For a full-page capture:

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --disable-gpu --hide-scrollbars --window-size=1280,4200 --virtual-time-budget=4000 --screenshot=out.png http://localhost:8765/
```

Look at every icon at its real size. Look at every button. Look at text over
any textured ground.

## 2. Contrast over texture

For text sitting over a photo, dither, or gradient, sample the ground behind
the text in the console:

```js
// average luminance of the canvas region behind an element
(el => { const c=document.querySelector('canvas'), r=el.getBoundingClientRect(),
  ctx=c.getContext('2d'), d=devicePixelRatio,
  px=ctx.getImageData(r.left*d, r.top*d, r.width*d, r.height*d).data;
  let sum=0; for(let i=0;i<px.length;i+=4) sum+=0.2126*px[i]+0.7152*px[i+1]+0.0722*px[i+2];
  return sum/(px.length/4) })(document.querySelector('.hero .ghost'))
```

White text over a ground averaging above 100 fails. Move the crest, add a
scrim, or move the text.

## 3. Alignment check

```js
// distinct left edges of visible text-bearing elements
[...new Set([...document.querySelectorAll('h1,h2,h3,p,td,th,li,a,button,span')]
  .filter(e=>e.offsetParent && e.innerText.trim())
  .map(e=>Math.round(e.getBoundingClientRect().left)))].sort((a,b)=>a-b)
```

Compare to the grid contract. Extra edges mean something drifted.

## 4. Color count

```js
[...new Set([...document.querySelectorAll('*')].flatMap(e=>{
  const s=getComputedStyle(e); return [s.color,s.backgroundColor]}))]
  .filter(c=>c!=='rgba(0, 0, 0, 0)')
```

More than ink greys plus one accent plus one status color means cut.

## 5. Side by side with the reference

Put the reference screenshot and the build next to each other. Annotate the
deltas with arrows, not adjectives. "The reference's heading is 1.4x the
subhead; mine is 2.1x" is fixable. "Mine feels heavier" is not.

## 6. Reduced motion

Toggle `prefers-reduced-motion` in the browser and reload. Nothing should
move; nothing should be hidden.

## 7. The checklist

Run `checklists/anti-slop.md`. Fix everything it catches. Then run it again.
