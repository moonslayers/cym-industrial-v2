---
name: agent-creator
description: >
  Creates new OpenCode agents following the agent specification format. 
  Trigger: When user asks to create a new agent, add agent instructions, or document agent patterns.
license: Apache-2.0
metadata:
  author: moonslayers
  version: "1.0"
  scope: [root]
  auto_invoke:
    - "Creating new agents"
---

## When to Use

- User requests to create a new agent for OpenCode
- Need to add agent instructions for specific workflows
- Task involves documenting agent behavior patterns
- Converting manual processes into agent-based workflows

## Critical Patterns

### Agent Location

ALL agents MUST be stored in `.opencode/agents/` directory:
- File path: `/path/to/project/.opencode/agents/{agent-name}.md`
- Agent name MUST be lowercase with hyphens (e.g., `log-simple-reporter`)

### Frontmatter Structure

ALL agents MUST have valid YAML frontmatter:
```yaml
---
name: {agent-name}
description: Use this agent to {what it does}
---
```

### Agent Instructions Format

Follow the structure from existing agents:
- Start with clear objective/instructions
- Use numbered steps or sections for complex workflows
- Provide examples when appropriate
- Include validation rules and success criteria
- Use code blocks for templates

## Code Examples

### Simple Agent Template

```markdown
---
name: my-agent-name
description: Use this agent to [brief description]
---

## INSTRUCCIONES PRINCIPALES

**OBJETIVO:** [Clear, concise objective]

**REGLAS:**
- Rule 1
- Rule 2

## FORMATO REQUERIDO

```markdown
[Template or format specification]
```

## PROCESO

### PASO 1: [Description]
[Detailed instructions]

### PASO 2: [Description]
[Detailed instructions]

## VALIDACIÓN

[Success criteria]
```

## Commands

```bash
# Create new agent file
nano .opencode/agents/your-agent-name.md

# List existing agents
ls -la .opencode/agents/

# Verify agent syntax
cat .opencode/agents/your-agent-name.md
```

## Naming Conventions

| Pattern | Example | Use Case |
|---------|---------|----------|
| `{purpose}-reporter` | `log-simple-reporter` | Reports/generators |
| `{target}-formatter` | `whatsapp-formatter` | Formatters/transformers |
| `{action}-{target}` | `data-processor` | General purpose agents |

## Success Criteria

- Agent file created in `.opencode/agents/`
- Valid YAML frontmatter with name and description
- Clear, actionable instructions
- Includes examples or templates when relevant
- Follows existing agent structure

## Failure Criteria

- Agent file created in wrong directory
- Missing or invalid frontmatter
- Vague or incomplete instructions
- No examples for complex workflows
- Inconsistent with existing agent patterns

## Resources

- **Templates**: See [assets/](assets/) for agent templates
- **Examples**: See [`.opencode/agents/`](.opencode/agents/) for reference implementations
