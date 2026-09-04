# Mobile

## Rules that do not bend

- Tap targets 44 x 44 minimum, even when the icon is 20px. Invisible padding.
- Safe areas: `env(safe-area-inset-*)` on every fixed bar. Nothing under the
  notch or the home indicator.
- Body text 16px minimum in inputs, or iOS zooms on focus.
- One subject per screen. Density from real content, not more chrome.
- Thumb reach: primary actions in the bottom half. Destructive actions never
  where a thumb rests.
- Sticky bottom bar for the primary CTA on long screens.

## Type

15 / 17 for body and labels, 28 to 34 for titles. Tracking −0.2px to −0.4px
on titles. System face (SF, Roboto) is a legitimate choice on mobile and
reads native; if the brand face is used, tune it.

## Navigation

Tab bar with three to five items, real icons at 24px with 10 to 11px labels.
Back is a chevron plus the previous title, never a bare arrow.

## Lists and cards

Rows 44 to 56 tall. Group by tint on a slightly darker ground, 12px radius,
inset 16px from the edges. Hairlines between rows inside a group only.

## Motion

Sheets slide up over 350ms strong ease-out with a scrim. Push navigation
250ms. Respect reduced motion; on mobile it is common.

## Verify

Screenshot at 375 x 812 and at 430 x 932. Check that nothing is under the
home indicator, that every tappable thing measures 44, and that no text is
under 11px.
