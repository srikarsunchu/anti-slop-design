# Dark Noise — the craft benchmark for a single-sound ambient app

Source: App Store listing id1465439395, MacStories review (2019), Peer Reviewed
(2019), Dark Noise 2 review. Extracted 2026-09-04 from listing screenshots
and written reviews. No live DOM; values are read from screenshots and marked
as such.

## The one idea
"Pick a sound and get back to what you were doing." The thing that embodies it
is the list: one tap on a row starts the sound, and the playback screen is a
sheet you pull up only if you want more.

## Type (per role)
| Role | Face | Weight | Size | Tracking | Line-height | Color |
|---|---|---|---|---|---|---|
| title | SF | 700 (large title) | 34 | system | system | white |
| row | SF | 400, 600 when playing | 17 | system | 44pt row | white |
| section | SF | 400 | 13 | system | — | secondary grey |
| now playing | SF | 600 | 17 | system | — | white on accent bar |

Guessed from screenshots; the app uses system text styles.

## Color
- ground: near-black with a violet cast (#0E0A1A region) in the default theme
- surfaces: rows are unbounded on the ground; the now-playing bar is the accent
- ink / secondary / tertiary: white / ~60% white / ~35% white
- accent: violet (#7C4DFF region) used for the now-playing bar, play button,
  favorite fill, and the header of the mix editor
- status colors: red minus badges in the mix editor
- count of distinct colors: greys plus one accent plus red. Eight alternate
  themes swap the accent.

## Ground
Flat dark with a violet tint. No texture. The richness comes from the
custom icon per sound and the animation of that icon while playing.

## Icons
Custom set, one per sound, monoline white, roughly 24 grid, animated on the
playback screen (waves move, fan spins). Consistent stroke across all 40+.

## Layout
- content max-width: full width list
- edges: 16 (iOS default inset)
- spacing scale observed: 8 / 16
- radii: 12 on the mix editor cards, pill on the play button
- rows: 44, icon well left, heart right

## Motion
- curves: iOS spring on the sheet
- durations: system sheet timing
- notable interactions: playback sheet pulled from the bottom; icon animates
  rhythmically while playing; heart fills with a small animation on favorite;
  haptics on play, favorite, reorder, and settings toggles.

## Depth
- sections / panels: list, playback sheet, mix editor, timer, settings, widgets,
  lock screen, Shortcuts
- how many show the product working: every listing screenshot shows a real
  sound name and state
- how many animate: the icon, the sheet, the heart

## In-app pages (from the 2026 listing screenshots)
- **Select Noise**: grouped list (Favorites, Noises, Water, Fire, Vehicles,
  Urban). Favorites pinned at the top with filled hearts and drag handles;
  every other row has an outline heart. One monoline icon per sound in a
  small dark well. Now-playing bar at the bottom with the sound's icon,
  "Now Playing", name, and a play button in the accent.
- **Player**: the sound's icon large in a rounded tile, its name, one play
  button, a "Select Noise ⌄" chevron that pulls the list up, AirPlay and volume.
- **Mixes**: name, artwork, per-sound level sliders, remove buttons.
- **Widgets, lock screen, Shortcuts** (Play <noise> with timer type, time,
  fade duration), **themes** and **alternate icons**.
- What the structure teaches: list + player is the praised standard in this
  category; favorites are the personal layer on top of a full catalogue; the
  player is one big control, not a metaphor. What to refuse: themes and icon
  packs (a design with one accent has nothing to theme), mixes for a product
  built on one decision.

## Hierarchy read
The list is primary and the screenshots agree: the first two shots are the
list. Position and weight agree. The purple is the one disagreement: it is
the loudest thing on screen and means nothing beyond "this is the theme".

## The lesson, as a rule
"One custom animated icon per sound turns a list into a product, so give each
item a drawn mark that moves when it is live, and let system integration
(lock screen, widgets, Shortcuts) do the rest of the work."

Second lesson: "A theme accent used everywhere is decoration, so if the
palette is user-chosen, still spend it only on state."

## Confidence
Layout, motion, and integration: measured from reviews and screenshots.
Exact hex and sizes: guessed; do not copy them, copy the structure.
