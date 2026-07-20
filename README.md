<h1 align="center">Claude Skills</h1>

<p align="center">
  <strong>A curated collection of skills that make Claude Code work the way you do.</strong>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-black.svg" alt="License: MIT"></a>
  <img src="https://img.shields.io/badge/skills-1-black.svg" alt="Skills: 1">
  <img src="https://img.shields.io/badge/PRs-welcome-black.svg" alt="PRs welcome">
  <img src="https://img.shields.io/badge/built%20for-Claude%20Code-black.svg" alt="Built for Claude Code">
</p>

---

Skills are small, focused instructions that Claude Code loads automatically when they're relevant. They don't change what Claude can do — they change *how* it does it. A good skill captures a preference, a workflow, or a way of working once, so you never have to explain it again.

This collection starts with one skill built for founders and designers, with more on the way.

---

## Skills

| Skill | What it does |
| --- | --- |
| **[Founder Mode](skills/founder-mode)** | Teaches Claude Code to communicate with non-developers — plain English, no jargon, and decisions made on your behalf until one actually needs you. |

---

## Quick start

Every skill in this collection is a self-contained folder. Installing one is a two-step copy.

```bash
# 1. Clone the collection
git clone https://github.com/BrettfromDJ/claude-skills.git

# 2. Copy a skill into Claude Code (Founder Mode shown here)
mkdir -p ~/.claude/skills/plain-language
cp claude-skills/skills/founder-mode/SKILL.md ~/.claude/skills/plain-language/
```

That's it. The skill activates automatically the next time it's relevant — no command to run, no flag to pass.

Each skill has its own README with full installation and customization notes:

- **[Founder Mode →](skills/founder-mode/README.md)**

---

## How skills work

A skill is a single `SKILL.md` file: a short block of instructions with a name and a description. Claude Code reads the description of every installed skill and pulls the full instructions into context only when they apply — so skills stay out of your way until the moment they're useful.

```
skills/
└── founder-mode/
    ├── SKILL.md      # the skill itself
    └── README.md     # docs, install, and examples
```

Skills live in one of two places:

- **`~/.claude/skills/`** — personal, available in every project.
- **`<project>/.claude/skills/`** — scoped to one repo and shareable with your team.

Learn more in the [Claude Code documentation](https://docs.claude.com/en/docs/claude-code).

---

## Philosophy

Good tools disappear. The best skills aren't clever — they're the ones that quietly remove friction you'd stopped noticing. Every skill here follows the same three rules:

1. **Do one thing well.** A skill is a preference, not a platform.
2. **Stay out of the way.** It should activate when it's needed and be invisible when it isn't.
3. **Respect the reader.** Whether that's a founder or an engineer, meet them where they are.

---

## Contributing

New skills, refinements, and fixes are all welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for the short version of how to add one.

---

## License

Released under the [MIT License](LICENSE). Use it, fork it, ship it.

<p align="center">
  <sub>Built for <a href="https://docs.claude.com/en/docs/claude-code">Claude Code</a>.</sub>
</p>
