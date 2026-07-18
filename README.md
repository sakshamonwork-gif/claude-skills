# 🧠 Claude Skills — Superpower Library

Custom Claude Code skills that transform Claude from a conversational assistant
into a disciplined, structured analyst and researcher.

## Skills Available

| Skill | Version | Category | Description |
|-------|---------|----------|-------------|
| `research-workflow` | 1.1 | Productivity & Research | Structured 4-phase research: Plan → Execute → Analyse → Synthesise |

## How to Use a Skill

In Claude Code (or any MCP-compatible client), load a skill by pointing to
the skill file:

```bash
# Example in Claude Code
@.codex/skills/research-workflow/skill.md
```

Or reference the raw GitHub URL in your system prompt / project instructions:

```
https://raw.githubusercontent.com/sakshamonwork-gif/claude-skills/main/.codex/skills/research-workflow/skill.md
```

## Repository Structure

```
claude-skills/
├── README.md
└── .codex/
    └── skills/
        └── research-workflow/
            ├── skill.md                          ← Main skill definition
            ├── assets/
            │   ├── research-plan-template.md
            │   ├── research-report-template.md
            │   └── source-evaluation-checklist.md
            └── references/
                ├── methodology.md
                └── output-formats.md
```

## Adding More Skills

Follow the same folder pattern: `.codex/skills/[skill-name]/skill.md`.
Each `skill.md` should have YAML front-matter with `name`, `description`,
`version`, `license`, and `compatibility`.

## License

MIT — free to use, fork, and extend.
