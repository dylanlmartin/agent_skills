# Agent skills from Jane Street

A collection of skills for AI agents and chatbots.
Each skill is a directory containing a `SKILL.md` file
with instructions for the agent.

## Skills

- **socratic-tutor** — turns an LLM into a strict personal tutor that teaches a
  topic of your choice using the Socratic method: a diagnostic, a skill map with
  levels 0-5, one question at a time, spaced review, and a final assessment.

## How to use

Each skill follows the open [Agent Skills](https://agentskills.io) format: a
directory whose `SKILL.md` starts with YAML frontmatter (`name`,
`description`) followed by the instructions.

### Claude Code (plugin marketplace)

This repo is a Claude Code plugin marketplace
(`.claude-plugin/marketplace.json`). Install the skill with:

```
/plugin marketplace add dylanlmartin/agent_skills
/plugin install socratic-tutor@dylanlmartin-skills
```

### Other agents that support `SKILL.md`

Copy the skill directory into your agent's skills folder, for example:

| Agent | Personal skills | Project skills |
| --- | --- | --- |
| Claude Code | `~/.claude/skills/` | `.claude/skills/` |
| Other tools | see their docs | |

```
git clone https://github.com/dylanlmartin/agent_skills.git
cp -r agent_skills/socratic-tutor ~/.claude/skills/
```

For claude.ai or the Claude app, zip the `socratic-tutor` directory and upload
it under Settings > Capabilities > Skills.

Then ask the agent to use it ("teach me X").

### Plain chatbots

Paste the body of the skill's `SKILL.md` into the chat (or into a
custom/system prompt), followed by what you want it to do.
