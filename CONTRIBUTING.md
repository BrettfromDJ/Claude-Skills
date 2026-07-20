# Contributing

Thanks for wanting to add to this collection. Skills are small by design, so contributing one is quick.

## Adding a skill

1. **Create a folder** under `skills/` named for your skill in `kebab-case` (e.g. `skills/my-skill/`).
2. **Write `SKILL.md`.** It needs YAML frontmatter with a `name` and a `description`, followed by the instructions themselves:

   ```markdown
   ---
   name: my-skill
   description: What it does, and when Claude should use it. Be specific — this is what triggers the skill.
   ---

   # My Skill

   Clear, direct instructions for Claude...
   ```

3. **Write a `README.md`** for the skill folder: what it does, a before/after example if it helps, and installation instructions.
4. **Add a row** to the Skills table in the root [README](README.md).

## Quality bar

Keep skills honest and focused:

- **One job.** A skill is a single, well-scoped behavior — not a bundle.
- **A sharp description.** The `description` is the trigger. Say plainly what the skill does and when to use it.
- **Tested.** Install your skill locally and confirm it activates when it should — and stays quiet when it shouldn't.
- **Clean writing.** Short sentences. Plain language. No filler.

## Submitting

Open a pull request with a brief note on what the skill does and who it's for. That's it.
