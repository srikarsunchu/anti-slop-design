# The mobile tells

Phone UI has its own median choices. Each one below is what a template does,
why it reads as generated, and what a person does instead. The surface rules
live in `surfaces/mobile.md`; this file is the reasoning.

## The painted status bar

A mock with "9:41", full bars and a full battery drawn inside the frame. On a
real phone the real status bar renders on top, so the painted one is either
doubled or a lie. It also tells the viewer the designer has never run the
screen. Leave the safe area empty. Let the device draw its own.

## The three-tab template

Home, Library, Profile. It is the App Store's most common bottom bar because
templates ship with it, not because most apps have three places to be. A
white noise app has one place to be and two decisions to make. A tab bar
exists when a user would genuinely be lost without it. Otherwise the app is
one screen and its sheets.

## The onboarding carousel

Illustration, headline, three dots, "Get started". Nobody reads it, and it
stands between a tired person and the thing they opened the app for. Let them
use the product first. Ask for notifications when there is something to
notify about. Ask for money on the second night, after the first one worked.

## The blob hero

A soft gradient blob behind a rounded card, usually purple to pink. It is
decoration standing in for a ground. A ground has a reason: the product's
own data, a texture the idea suggests, a glow that comes from a real element
on the screen.

## The tile grid

Forty sounds in a four-column grid, each with an icon. It looks like
abundance and works like a menu in a language you do not speak. Fewer
things, named the way the user names them ("Hair dryer", not "Machine 3"),
in a single-column list with one line of reason under each. A thumb scans a
list; it hunts in a grid.

## The habitual accent

Purple or indigo on the primary button, on every icon, on the selected tab,
on the divider. Color that means nothing. Derive the accent from the idea, or
stay monochrome. Then spend it only on state and action.

## The empty sheet

A bottom sheet that contains one giant primary button. A sheet is a decision
surface: the options, the current one marked, one footnote that explains a
consequence. If there is only one thing to do, it does not need a sheet.

## The template voice

"Welcome to X", "Get started", "Let's go", "You're all set", "Oops!". A verb
and an object, in the product's voice: "Tap the light to start", "Fades out in
the last minute", "Until 6:30".

## Emoji as icons

They vary by platform, cannot be recolored, and never sit on a baseline. One
icon set, one grammar, drawn at the size they render at.

## Bold everything

Every label at 600 or 700 because the template's heading style was reused.
On a phone, 400 and 500 only. Hierarchy comes from size gaps and color.

## Designing for the bright room

A dark UI that only works at 60% brightness. Most night apps are opened at
minimum brightness, where mid-greys and thin hairlines disappear and a
saturated accent glares. Design the dim state on purpose: the one thing that
must be tappable sits at high luminance, hairlines become tint shifts, the
accent has a dim variant.

## A physical control on glass

A knob to turn, a slider to sweep, a switch to flick, drawn to look like the
hardware it replaces. It photographs well and demos well. In use it is slower
than a tap, it caps the list at however many stops fit around the rim, and a
screen reader cannot turn it. The praised apps in the category (Dark Noise,
2026) give "one tap to start" with a big play control and a list one pull
away. So: one large tap target for the primary action, a list behind it, and
the physical metaphor kept only as the icon mark. Lull learned this the slow
way: a rotary dial was picked from three sketches and built hi-fi before the
comparison with a shipping app showed the list + player structure was what
people actually praise.

## Rule

Before shipping a phone screen, remove the painted status bar, count the
tabs, delete the carousel, name the ground, look at it at minimum
brightness, and ask whether the primary control is a tap or a metaphor. If
any of the tells above survives, it is a template.
