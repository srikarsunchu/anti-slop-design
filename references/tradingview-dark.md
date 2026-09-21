# TradingView dark — the default palette for trading tool UI

Source: TradingView chart and screener, dark theme (tradingview.com). Extracted
2026-09-09 from memory of the published theme variables, cross-checked against
the Signal scanner dashboard build in `whop-blueprints/saas-website`. Values
are the well-known theme tokens, not a live DOM pull; treat as high confidence
on color, guessed on type sizes.

## The one idea
"The chart is the page." Everything else is chrome at 11 to 13px around one
large price series, and the only saturated color is the direction of price.

## Type (per role)
| Role | Face | Weight | Size | Tracking | Line-height | Color |
|---|---|---|---|---|---|---|
| price | mono/tabular | 400 | 20 | 0 | 1.2 | #d1d4dc |
| ticker | mono | 500 | 13 | 0 | 1.2 | #d1d4dc |
| ui | sans | 400 | 12 | −0.15px | 1.4 | #d1d4dc |
| meta / axis | sans or mono | 400 | 10–11 | 0.04em caps for labels | 1.3 | #787b86 |

## Color
- ground: #131722
- surfaces: panels #1e222d, lines and hairlines #2a2e39
- ink / secondary / tertiary: #d1d4dc / #787b86 / #50535e
- accent: none as brand. Green #26a69a and red #ef5350 carry direction, P&L, and long/short state only. Tints at 15% alpha for chips.
- status colors: the same green/red; amber only for paused.
- count of distinct colors: three greys, two surfaces, green, red.

## Ground
Dense data. No texture. A single price chart with a gradient fill under the
line at 25% to 0% opacity, hairline grid horizontal only.

## Icons
Lucide 14px in nav and rows, stroke 1.75. Radar, BellRing, FlaskConical, Bot,
NotebookPen for a scanner product.

## Layout
- sidebar 160px, main padding 12 to 16
- spacing 4 / 8 / 12 / 16
- radii 12 on panels, 5 on chips and the logo tile
- KPI strip as a 1px-gap grid on the line color, never wrapping into an empty slot

## Motion
- 200ms fade on panels, staggered 50ms. Nothing else on load.
- One pulsing dot for "live". Chart lines do not animate on load.

## Depth
- panels: sidebar, top bar, KPI strip, chart, alert feed, account, positions, strategies
- all populated; alert feed and positions carry the scenario (NVDA 20D high break, 09:37, RVOL 3.2x)

## Hierarchy read
Price and chart first, alert chip second, feed third. Position (top-left of
main) and weight (20px price) agree.

## Applied as a whole-site theme (Signal, 2026-09-09)
The landing page later went fully dark using shadcn zinc dark tokens with the
background deepened one step (oklch 0.13) so cards at 0.21 read as panels. Every
colour is a semantic token (background, card, muted, border, primary). Primary
CTAs flip to white pills. Glass cards become 4 to 6% white over the ground. The
Whop Checkout element takes `appearance.theme.appearance = "dark"`. Lesson: a
product demo and its marketing page must share one skin; two skins read as two
products.

## The lesson, as a rule
"Color means direction because traders read green and red before they read
words, so never use green or red for anything that is not P&L, direction, or
long/short state."

## Confidence
Colors measured from the published theme. Sizes and spacing are the build's
choices and match the surfaces/product-ui spec.
