# Founder Mode

**Teach Claude Code to talk to you like a technical partner — not another developer.**

Founder Mode is for the person building the product, not maintaining the codebase. It changes *how Claude communicates*, not what it's capable of. Claude still writes the same code, runs the same tools, and solves the same problems. It just stops narrating the parts you don't care about and starts leading with the part you do: what changed, and why it matters.

> Skill id: `founder-mode` · Part of [Claude Skills](../../README.md)

---

## Why it exists

Claude Code is extraordinary at the work. Out of the box, it also talks like it's pairing with a senior engineer — stack traces, file diffs, lint output, a running commentary of every package it installs.

If you're a founder or designer, that's noise. You don't need the play-by-play. You need to know whether it's done, what moved, and whether you have to do anything.

Founder Mode closes that gap.

---

## Before & after

**Without Founder Mode**

> I've refactored `AuthProvider.tsx` to use the `useReducer` hook instead of multiple `useState` calls, updated the `SessionContext` type signature, resolved 3 ESLint warnings about exhaustive-deps, and bumped `@tanstack/react-query` to 5.2.1. The build passes. Note the token refresh now fires on a 401 interceptor rather than a polling interval...

**With Founder Mode**

> **Done**
> Logins are more reliable now — sessions refresh automatically instead of dropping people out. Nothing changes visually.
>
> **Important**
> Worth a quick test: log in, leave the tab open for a few minutes, and confirm you stay signed in.

Same work. A fraction of the cognitive load.

---

## What it does

- **Explains coding work in plain English** — no jargon unless it genuinely helps.
- **Leads with what changed and why it matters** — from your perspective, not the code's.
- **Skips the routine narration** — no more play-by-play of file reads, refactors, or installs.
- **Makes reasonable technical calls on its own** — so you're not rubber-stamping every decision.
- **Interrupts you only when it counts** — when a choice affects the product, design, cost, security, or long-term direction.
- **Handles failures cleanly** — what happened, whether it's fixed, and what you need to do next.

---

## Installation

Founder Mode is a [Claude Code skill](https://docs.claude.com/en/docs/claude-code). Install it once and it applies automatically to your coding work — no command to remember, no flag to pass.

### Option 1 — Personal (recommended)

Available in every project on your machine.

```bash
git clone https://github.com/BrettfromDJ/claude-skills.git
cp -r claude-skills/skills/founder-mode ~/.claude/skills/
```

### Option 2 — Per project

Scoped to a single repository and shareable with your team via version control.

```bash
git clone https://github.com/BrettfromDJ/claude-skills.git
mkdir -p .claude/skills
cp -r claude-skills/skills/founder-mode .claude/skills/
```

That's it. The next time Claude Code does anything code-related, Founder Mode is on.

---

## Verifying it's active

Ask Claude Code to make a small change, then watch how it reports back. You'll know Founder Mode is working when the response opens with **Done** and a plain-English summary instead of a technical changelog.

You can also confirm the file is in place:

```bash
cat ~/.claude/skills/founder-mode/SKILL.md   # personal install
cat .claude/skills/founder-mode/SKILL.md     # per-project install
```

---

## Customizing it

Founder Mode is a single Markdown file — open `SKILL.md` and make it yours. A few common tweaks:

- **Tighten or loosen the tone.** Edit the *Default behavior* section to match how you like to be talked to.
- **Change what gets escalated.** Adjust the line about when to interrupt you — add "brand voice" or "accessibility," for example.
- **Reshape the sign-off.** The **Done / Important** format is a preference, not a rule. Rewrite it.

After editing, restart your Claude Code session so the change is picked up.

---

## Uninstalling

Delete the folder:

```bash
rm -rf ~/.claude/skills/founder-mode   # personal
rm -rf .claude/skills/founder-mode     # per-project
```

---

## FAQ

**Does this make Claude write worse code?**
No. It changes communication only. The engineering is identical.

**Will it stop asking me questions entirely?**
No — it asks *fewer*, and only the ones that matter: decisions affecting product, design, cost, security, or long-term direction. The routine calls it makes on its own.

**I'm actually a developer. Is this for me?**
Probably not day-to-day — you likely want the detail. But it's useful when you're reviewing at a high level or handing work to non-technical teammates.

**Does it work with any programming language or framework?**
Yes. It's about communication, so it's language- and stack-agnostic.

---

<p align="center">
  <a href="../../README.md">← Back to Claude Skills</a>
</p>
