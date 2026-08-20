# skills

[![skills.sh](https://skills.sh/b/dmunro-karius/skills)](https://skills.sh/dmunro-karius/skills)

Personal [agent skills](https://agentskills.io) — installable into Claude Code and 70+ other agents
via the [`skills`](https://github.com/vercel-labs/skills) CLI.

## Install

```bash
# everything, into this project's .claude/skills/
npx skills@latest add dmunro-karius/skills

# one skill, globally (~/.claude/skills/)
npx skills@latest add dmunro-karius/skills --skill unslop -g -a claude-code -y

# see what's in here without installing
npx skills@latest add dmunro-karius/skills --list
```

## Skills

| Skill | Description |
| ----- | ----------- |
| [`unslop`](skills/unslop/SKILL.md) | Cut AI tells from any writing. Must always apply. |
| [`typescript-best-practices`](skills/typescript-best-practices/SKILL.md) | TypeScript best practices. Use when reading or editing any `.ts` or `.tsx` file. |

## Layout

Each skill is a directory under `skills/` containing a `SKILL.md` with YAML
frontmatter (`name`, `description`). Supporting files (references, scripts,
templates) live alongside it in the same directory.

```
skills/
  <skill-name>/
    SKILL.md
    references/
      <topic>.md
```

Set `metadata.internal: true` in the frontmatter to hide a work-in-progress
skill from discovery; it then only installs with `INSTALL_INTERNAL_SKILLS=1`.

## Updating

```bash
npx skills@latest update unslop
```
