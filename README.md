# sri-design

My personal design method for building UI with AI that feels hand-made.
Packaged as a [Claude Code](https://claude.com/claude-code) skill.

It has no house style. It is a way of working: name one idea, take every value
from a real reference, build quiet UI over a rich ground or dense real data,
and look at the pixels before calling it done.

## Layout

```
SKILL.md          entry point: the brief, hard gates, quiet defaults, process
principles/       the taste, one lesson per file, each ending in a rule
methods/          brief, ground-truth extraction, grid contract, verify, digest
surfaces/         landing pages, product UI, mobile, film tooling
references/       ground truth from real designs, as text and numbers
libraries/        verified snippets for the trusted libraries
examples/         full builds under this method, for calibration
checklists/       the pre-ship gate
```

## Install

```bash
git clone https://github.com/srikarsunchu/sri-design ~/.claude/skills/sri-design
```

It loads on any UI work, or invoke it with `/sri-design`.

## Growing it

When a build teaches something, write the rule into `principles/`. When a
reference is studied, record it in `references/` from the template. When a
build is worth keeping, put it in `examples/`. The repo is the memory; the
conversation is not.

## License

MIT.
