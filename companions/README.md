# Vendored companion skills

Copies of the skills that anti-slop-design hands motion and component work
to. Each folder is a complete Claude Code skill; `../companions.md` says
which brief goes where.

| Folder | Upstream | License |
|---|---|---|
| `animate`, `animate-expo`, `animation-vocabulary`, `apple-design`, `ask-sonner`, `emil-design-eng`, `find-animation-opportunities`, `improve-animations`, `mobile-native`, `pick-ui-library`, `prototype`, `review-animations` | [emilkowalski/skills](https://github.com/emilkowalski/skills) | MIT, Emil Kowalski (LICENSE in each folder) |
| `motion-primitives` | [ibelick/motion-primitives](https://github.com/ibelick/motion-primitives), bundled as a skill with component source and registry | MIT, Julien Thibeaut (LICENSE in folder) |

Snapshot taken 2026-09-15 (Emil's pack) and 2026-09-09 (Motion Primitives).
Upstream moves; refresh from the source repos rather than editing here.

## Install

```bash
cp -R companions/* ~/.claude/skills/
```

Each folder lands as its own skill, next to anti-slop-design.
