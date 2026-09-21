# Digesting a reference

When the user shares a site, screenshot, or video, turn it into a stored
lesson so it survives the session. Narrate every step in the conversation so
a wrong extraction is caught before it becomes taste.

## Steps, said out loud

1. **What is this?** One line: screen type, purpose, the one idea it is
   built around.
2. **What is the delta?** If it is a comparison or an A/B, name the one
   variable that differs. Do not describe both halves.
3. **Ground truth.** Run `methods/extract-ground-truth.md`. Fonts per role,
   colors counted, background treatment, icon grammar, grid, motion, depth.
4. **Hierarchy read.** What is the one primary subject? Do position and
   visual weight agree on it? Disagreement is a flaw worth noting.
5. **The lesson as a rule.** "X because Y, so always Z." Stated so it applies
   beyond this one screen. If it cannot be written as a rule, it is not
   learned yet.
6. **Confidence.** What was measured versus guessed. Invite correction.

## Store it

- Ground truth goes in `references/<name>.md` from the template.
- The rule goes into the relevant `principles/` file, or a new one if it is
  a new lesson. Link it from the reference.
- Never commit third-party images or video. Text and numbers only.

## The failure to avoid

Picking a direction from sketches alone. Three low-fi frames compared side by
side will always favour the most striking one, and striking is not the same as
usable. Before committing a direction, look at a shipping, praised product
in the same category and ask what its pages are; if the striking direction
cannot explain why those pages exist, it has not earned the build. Lull
built a rotary dial hi-fi before doing this and threw it away in a day.


Silently absorbing "this looks nice" and later reproducing a vague version.
Every lesson is a checkable rule with a reason.
