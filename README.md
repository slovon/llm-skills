# llm-skills

A collection of [Agent Skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) for Claude and other LLM agents that support the `SKILL.md` format.

Each skill lives in its own folder under [`skills/`](skills/). The folder holds a `SKILL.md` file with YAML frontmatter (`name`, `description`) and the instructions the model follows when the skill is active.

## Skills

| Skill | Description |
|---|---|
| [six-hats-facilitator](skills/six-hats-facilitator/) | Runs a Six Thinking Hats session with the model as the Blue Hat only. It picks a hat sequence that fits the problem, then guides you hat by hat while you supply all the content, and ends with a decision roadmap. |

## Installation

### Claude Code: plugin marketplace

This repository is also a Claude Code plugin marketplace. Add it and install a skill:

```
/plugin marketplace add slovon/llm-skills
/plugin install six-hats-facilitator@llm-skills
```

### Claude Code: manual

Copy a skill folder into your personal skills directory (available in every project):

```bash
git clone https://github.com/slovon/llm-skills.git
cp -r llm-skills/skills/six-hats-facilitator ~/.claude/skills/
```

Or copy it into `.claude/skills/` inside a project to make it available only there.

### Claude.ai and the Claude desktop app

1. Download the skill folder and zip it, so the zip contains the `six-hats-facilitator/` folder with `SKILL.md` inside.
2. In Claude, open **Settings → Capabilities → Skills** and upload the zip.

### Other agents

Any agent that supports the Agent Skills format can load the skill folder as is. For tools without skill support, you can paste the body of `SKILL.md` into a system prompt or custom instructions.

## Repository layout

```
.
├── .claude-plugin/
│   └── marketplace.json     # Claude Code plugin marketplace manifest
├── skills/
│   └── <skill-name>/
│       ├── SKILL.md         # Required: frontmatter + instructions
│       └── README.md        # Human-facing docs for the skill
├── LICENSE
└── README.md
```

## Adding a new skill

1. Create `skills/<skill-name>/SKILL.md`. Use lowercase, hyphen-separated names, and make `name` in the frontmatter match the folder name.
2. Write a `description` that says what the skill does and when to use it, since the model uses it to decide when to load the skill.
3. Add a short `README.md` next to it for human readers.
4. Add a row to the **Skills** table above and an entry to `.claude-plugin/marketplace.json`.

## License

Released into the public domain under [The Unlicense](LICENSE).
