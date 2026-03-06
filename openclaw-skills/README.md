# OpenClaw Unified Skills

Adapted from [claude-code-unified-agents](https://github.com/NecroVR/claude-code-unified-agents) for the [OpenClaw](https://openclaw.ai/) AI agent platform.

## Overview

92 production-ready skills across 12 categories, converted from Claude Code sub-agent format to OpenClaw SKILL.md format.

## Installation

### Install All Skills

```bash
# Clone this repo
git clone https://github.com/NecroVR/claude-code-unified-agents.git
cd claude-code-unified-agents

# Copy all OpenClaw skills to your OpenClaw installation
cp -r openclaw-skills/*/ ~/.openclaw/skills/

# On Windows (Git Bash)
cp -r openclaw-skills/*/ /c/Users/$USER/.openclaw/skills/
```

### Install Specific Skills

```bash
# Copy individual skills
cp -r openclaw-skills/ue5-gameplay-programmer ~/.openclaw/skills/
cp -r openclaw-skills/python-pro ~/.openclaw/skills/
```

## Skill Categories

| Category | Count | Skills |
|----------|-------|--------|
| Development | 20 | backend-architect, frontend-specialist, python-pro, fullstack-engineer, database-specialist, mobile-developer, blockchain-developer, rust-pro, golang-pro, typescript-pro, javascript-pro, java-enterprise, nextjs-pro, react-pro, vue-specialist, angular-expert, edge-serverless-developer, legacy-modernizer, cli-developer, i18n-specialist |
| Infrastructure | 12 | devops-engineer, cloud-architect, devsecops-engineer, iac-specialist, sre-engineer, platform-engineer, build-engineer, incident-responder, performance-engineer, monitoring-specialist, deployment-manager, kubernetes-expert |
| Quality | 7 | code-reviewer, security-auditor, test-engineer, e2e-test-specialist, performance-tester, accessibility-auditor, threat-modeler |
| Data & AI | 7 | ai-engineer, agentic-systems-engineer, data-engineer, data-scientist, mlops-engineer, prompt-engineer, analytics-engineer |
| Business | 8 | project-manager, product-strategist, business-analyst, technical-writer, requirements-analyst, api-designer, research-analyst, competitive-analyst |
| Creative | 7 | ux-designer, ui-designer, content-strategist, brand-designer, design-system-engineer, copywriter, motion-designer |
| Marketing | 7 | seo-specialist, email-marketer, social-media-strategist, growth-engineer, content-marketer, conversion-optimizer, ad-specialist |
| Communication | 4 | presentation-builder, team-communicator, support-writer, changelog-writer |
| HR & Agent Mgmt | 3 | agent-performance-coach, agent-gap-analyst, agent-talent-scout |
| Meta-Management | 5 | context-manager, workflow-optimizer, agent-generator, error-detective, documentation-writer |
| Specialized | 5 | game-developer, embedded-engineer, fintech-specialist, healthcare-dev, ecommerce-expert |
| Unreal Engine 5 | 6 | ue5-blueprint-architect, ue5-gameplay-programmer, ue5-multiplayer-engineer, ue5-rendering-engineer, ue5-technical-artist, ue5-tools-engineer |
| Core | 1 | orchestrator |

## Skill Format

Each skill follows the OpenClaw SKILL.md format:

```markdown
---
name: skill-name
description: When this skill should be used
metadata:
  category: category-name
  source: claude-code-unified-agents
  claude-code-tools: Original Claude Code tools list
---

[System prompt and expertise documentation]
```

## Key Differences from Claude Code Agents

| Feature | Claude Code | OpenClaw |
|---------|------------|----------|
| Location | `.claude/agents/<category>/<name>.md` | `skills/<name>/SKILL.md` |
| Tool control | Per-agent `tools:` frontmatter | Global `tools.profile` in config |
| Sub-agents | `Task` tool | Subagent delegation |
| File editing | `MultiEdit` tool | `Edit` tool equivalent |
| Invocation | `@agent-name` in chat | Automatic skill matching |

## Usage with OpenClaw

Once installed, OpenClaw automatically injects relevant skills into the system prompt based on the task context. You can also reference skills explicitly in your messages.

Skills work with any OpenClaw agent (main, coding, monitor, or custom agents) and are available across all channels (Discord, webchat, etc.).

## License

MIT License - Same as the original repository.
