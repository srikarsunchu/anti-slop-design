# Mobile

Phone apps, both platforms. Everything in `SKILL.md` still applies; this file
is what changes when the screen is 390 wide, held in one hand, often at night,
by someone whose attention is interrupted every ninety seconds.

## The context that drives every decision

- **One hand.** The other hand is holding a baby, a coffee, a rail. The
  thumb reaches the bottom 60% of the screen comfortably and the top corners
  not at all. Primary actions live in the bottom half. Destructive actions
  never sit where a resting thumb lands.
- **Interrupted attention.** A screen is read in a glance, not studied. One
  subject per screen. If the user has to read a sentence to know what to
  tap, the screen has failed.
- **Night.** Many apps are opened in the dark. A screen at minimum brightness
  is a different design: mid-greys vanish, thin hairlines vanish, saturated
  color glares. Design the dim state on purpose (below).
- **The phone is often lying down.** Face up on a table, in a dock, charging
  in landscape. Ask where the phone physically is when this screen is shown.

## The mobile tells

Every one of these is the median choice and reads as generated. See
`principles/mobile-tells.md` for the lesson behind each.

| Tell | Fix |
|---|---|
| A painted status bar (9:41, wifi, battery) inside the mock | Leave the safe area empty; the real one renders there |
| Three-tab bar: Home / Library / Profile | Tabs only if there are three genuinely different places to be; many apps are one screen and two sheets |
| Onboarding carousel: illustration, headline, three dots, "Get started" | Let them use the product first. Ask for permissions and money on night two, in context |
| A gradient blob hero behind a big rounded card | A ground with a reason: a texture, a photo, the product's own data |
| A grid of 40 tiles with an icon in each | Fewer things, named specifically, in a list a thumb can scan |
| Purple or indigo accent, or a bright accent on every icon | Accent derived from the idea, used for state and action only |
| Bottom sheet holding one giant primary button and nothing else | A sheet holds a decision: the options, the current one marked, a footnote |
| "Welcome to X", "Get started", "Let's go", "You're all set" | A verb and an object, in the product's voice |
| Emoji as icons | One real icon set, one grammar, drawn at the rendered size |
| Every card with a drop shadow on a white void | Tint shift and radius on an off-white or dark ground; hairlines inside groups only |
| 700 weight on every label | 400 and 500; hierarchy from size gaps and color |

## Type

System faces are legitimate here and read native: SF on iOS, Roboto or the
device face on Android. Tune them anyway.

- Ramp: three UI sizes within 2px (13 / 15 / 17) and one display jump (34 to
  56). Hierarchy is the gap.
- Tracking: −0.2px on 15 and 17, −0.4px on titles, −1px or more on a 44+
  display numeral.
- Numerals: tabular on any clock, countdown, count, or duration. A
  countdown that jitters is a tell.
- Machinery text (eyebrows, section labels, timecodes): mono, 13px, +1px
  tracking, caps, tertiary color.
- Dynamic Type: the layout must survive one step larger than default. Test
  it once. Do not lock text to a size to protect the layout.
- Inputs: 16px minimum or iOS zooms on focus.

## Color and the dim state

- Dark grounds are warm or cool, never #000 alone. A dark app needs a
  ground: a full-surface gradient (no corner flat), a grain at 4 to 6% to
  stop OLED banding, or a glow that comes from something on the screen.
- Greys for dark UI (from iOS, see `references/ios-dark-grouped.md`): label
  #F2F2F0, secondary rgba(235,235,245,.6), tertiary .3, cell #1C1C1E, nested
  #2C2C2E, separator rgba(84,84,88,.6). Warm or cool them toward the ground.
- **Dim budget.** Say in the brief what the screen looks like at minimum
  brightness. Rule of thumb: anything below 30% luminance disappears at
  minimum brightness on an OLED; hairlines under rgba(255,255,255,.2)
  disappear; a saturated accent at full value glares. So: the one thing that
  must be tappable in the dark sits at 60%+ luminance; the accent, if any,
  has a dim variant; hairlines are replaced by tint shifts.
- No pure black behind a warm accent: the accent halos and reads as a
  sticker. Lift the ground 3 to 5%. A grey of 5/255 also avoids OLED black
  smear on slow fades.

## Grid contract for a phone

```
edges     20px from the screen edge | 16px inset inside a cell | icon well 36px
targets   44 x 44 minimum, always, even when the glyph is 20px
rows      52 to 56 tall with a detail line, 44 without
spacing   4 / 8 / 12 / 16 / 24 / 32 / 48
type      13 / 15 / 17 + one display (34 to 56)
radii     12 on groups and sheets (16 to 20 at the sheet's top), pill on the one primary action
```

Left edges resolve to three x positions: the screen edge (20), the cell
text edge (36), and the text edge past an icon well (84). Count them in
verify.

## Navigation

- Prefer one screen plus sheets over tabs. A sheet is a decision surface:
  title, options with the current one marked, a one-line footnote, dismiss
  by scrim.
- If tabs are earned: three to five, real icons at 24px, labels 10 to 11px,
  the current tab shown by weight and color together.
- Back is a chevron plus the previous title, never a bare arrow.
- Sheets slide up over 350ms strong ease-out with a 60% scrim; dismiss at
  250ms standard. Push navigation 250ms.

## Motion

Two curves, the ladder from `principles/motion.md`, plus:

- Press: scale .97 over 150ms on every pressable thing, including the big
  one.
- One living element, if the idea earns it: a breath at 4s, a glow that
  follows the sound, an icon that moves with the audio. One. Not every
  card.
- Haptics are motion you feel. Light impact on the primary action and on
  selection; nothing on scroll or on every row.
- Reduced motion is common on phones. Keep opacity and color changes,
  drop transforms, and test it.

## System surfaces are part of the design

An app on a phone is also its lock-screen player, its widget, its Live
Activity, its StandBy face, its icon, and its splash. Design them in the
same pass, with the same idea and the same one accent. A brilliant screen
and a default icon is half a product.

Checklist: lock screen now-playing (title, artist line, artwork) · small
and medium widget · Live Activity / Dynamic Island for anything with a
countdown (it also shows full-screen in StandBy) · StandBy (landscape, dim,
at arm's length, only while charging on a stand) · icon at 60 and 1024 built
from exact primitives · splash that is the ground, not a logo on white.

## Building it (React Native / Expo)

- Ground and glow: `react-native-svg` radial gradients sized to the window;
  grain as an SVG `Pattern` (Image `resizeMode="repeat"` does not tile on iOS).
- Sheets: `Modal` plus `Animated` translateY, or `@gorhom/bottom-sheet`
  when drag-to-dismiss matters.
- Haptics: `expo-haptics`, light impact. Guard `Platform.OS === 'web'`.
- Sliders: `@react-native-community/slider`. Do not hand-roll a track.
- Icons: `lucide-react-native` (real paths, one grammar).
- Reduced motion: `AccessibilityInfo.isReduceMotionEnabled()`.
- Fonts: system by default. A brand face must be loaded with `expo-font`
  and given a fallback.

## Companions

For a web app that has to feel installed (100vh, tap highlight, zoom on
focus, pull-to-refresh, notch), run `mobile-native` after this file. For
anything that moves or is dragged in Expo, `animate-expo`. For sheets and
gestures that should feel like the platform's own, `apple-design`. Map in
`companions.md`.

## Verify

1. Screenshot at 390 x 844 and 430 x 932. On a simulator:
   `xcrun simctl io <udid> screenshot out.png`. On web: the browser pane at
   375 and 430.
2. **Dim test.** Lower the screenshot to 25% brightness (a multiply layer, or
   Pillow `ImageEnhance.Brightness(im).enhance(0.25)`) and look: is the
   primary target still findable? Did the hairlines survive? Does the accent
   glare?
3. Count left edges against the contract (three positions).
4. Measure every tappable thing: 44 or more.
5. Toggle Reduce Motion and Dynamic Type one step up; nothing hidden,
   nothing overlapping.
6. Look at the icon at 60px and the widget at real size next to a system
   app's. If it looks louder than Clock, it is too loud.
7. Run `checklists/anti-slop.md`, then this file's tells table.

## Rule

A phone screen is used by a thumb, in a glance, often in the dark. If a
screen needs two hands, a sentence, or a bright room, redesign it.
