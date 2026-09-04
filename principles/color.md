# Color

## Color carries meaning or it does not exist

Three colors is a full palette: ink greys, one accent for the primary action
and selection, one status color for success. Every color on the page should
answer "what does this tell the user?"

Uses that earn color: the primary CTA, the selected item, a success or error
state, scarcity or urgency, a diff.

Uses that do not: loaders, spinners, progress rings, neutral icons, dividers,
decorative fills, section backgrounds, hover on non-primary items. Those stay
grey. A loading state communicates "wait", which is neutral.

## Where the accent comes from

From the reference or the brief. Sample it from the imagery if there is
imagery. If there is neither, stay monochrome. An accent chosen by habit
(orange, indigo, teal) is the tell.

## Greys

No pure black text. No pure white ground on a light page.

- Light: ground #f9f9f8, surface #f2f2f0, nested surface #ebebe8, ink #292929,
  secondary #5D5D5D, tertiary #9E9E9E, hairline rgba(0,0,0,.08).
- Dark: ground #101010, surface #181818, nested #202020, text #f2f2f0,
  secondary rgba(255,255,255,.6), tertiary rgba(255,255,255,.4).

Adapt these to the reference. They are a starting point.

## Gradients

- As imagery inside a container (a card's art, a hero photo, a logo band):
  allowed.
- As UI chrome (buttons, nav bars, page washes): never.
- One glow on a dark premium surface: allowed, and the base must itself be a
  subtle gradient so no corner is flat.
- Never one radial glow in a corner with three flat corners. Either the whole
  surface moves or none of it does.
- Never purple-to-blue. Never spectral in chrome.

## Dark surfaces

Dark reads premium when it has one light source and a texture. Dark with flat
#000 and grey boxes reads like a default dark mode. Give it a ground.

## Rule

Count the colors before shipping. More than one accent, or the accent used as
decoration, means cut.
