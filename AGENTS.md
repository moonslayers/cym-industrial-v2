# Repository Guidelines

## How to Use This Guide

- Start here for cross-project norms.
- Each component has an `AGENTS.md` file with specific guidelines (e.g., `api/AGENTS.md`, `ui/AGENTS.md`).
- Component docs override this file when guidance conflicts.

## Available Skills

Use these skills for detailed patterns on-demand:

### Generic Skills (Any Project)

| Skill | Description | URL |
|-------|-------------|-----|
| `typescript` | Const types, flat interfaces, utility types | [SKILL.md](skills/typescript/SKILL.md) |
| `tailwind-4` | cn() utility, no var() in className | [SKILL.md](skills/tailwind-4/SKILL.md) |
| `frontend-designer` | Distinctive frontend interfaces, avoid AI aesthetics | [SKILL.md](skills/frontend-designer/SKILL.md) |

### Project-Specific Skills

| Skill | Description | URL |
|-------|-------------|-----|
| `cym-ui` | CYM Industrial UI patterns (index section) | [SKILL.md](skills/cym-ui/SKILL.md) |
| `skill-creator` | Create new AI agent skills | [SKILL.md](skills/skill-creator/SKILL.md) |

### Auto-invoke Skills

When performing these actions, ALWAYS invoke the corresponding skill FIRST:

| Action | Skill |
|--------|-------|
| -- | `agent-creator` |
| After creating/modifying a skill | `skill-sync` |
| Creating new agents | `agent-creator` |
| Creating new skills | `skill-creator` |
| Designing, redesigning, or improving UI interfaces | `frontend-designer` |
| Regenerate AGENTS.md Auto-invoke tables (sync.sh) | `skill-sync` |
| Troubleshoot why a skill is missing from AGENTS.md auto-invoke | `skill-sync` |
| Working with Tailwind classes | `tailwind-4` |
| Writing TypeScript types/interfaces | `typescript` |

---

## Project Overview

landing page for CYM Industrial vendedores de compresores de aire industriales y tambien de servicio de manteimiento y renta de maquinas
