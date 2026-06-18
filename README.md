# NexusPoint Claude Skills

Free, research-backed [Claude Code](https://docs.claude.com/en/docs/claude-code) skills from [NexusPoint](https://nexus-point.co/).

## claude-advisor

The go-to guide to **everything Claude**, as an installable skill. Ask it anything about Claude and get a specific, sourced answer instead of a vague one:

- **"Which Claude should I use for this?"** chat vs Claude Code vs Cowork, with a decision table.
- **"Opus vs Sonnet vs Haiku for X?"** model selection grounded in 2026 specs and pricing.
- **"Can I build this workflow in Claude Code?"** feasibility first, then the build shape.
- **"Best plugins / MCP servers / tools?"** the ecosystem map.
- **"Which plan should I buy?"** Free / Pro / Max / Team / Enterprise, and how Claude compares to ChatGPT and Gemini.

Every load-bearing claim is grounded in a **NotebookLM synthesis of 237 cited 2026 sources** (`research-synthesis.md` + a per-source index in `_research/sources.json`), with honesty flags on anything version- or price-sensitive.

### Install

In Claude Code:

```
/plugin marketplace add Qubit1010/nexuspoint-claude-skills
/plugin install claude-advisor
```

Then just ask Claude anything about Claude. The skill activates automatically.

### Use it on Claude.ai (no Claude Code needed)

The skill folder also works as an uploadable Skill on Claude.ai (Settings -> Capabilities -> Skills). Zip `plugins/claude-advisor/skills/claude-advisor/` and upload it.

### What's inside

```
plugins/claude-advisor/skills/claude-advisor/
├── SKILL.md                  # the skill logic + mode detection
├── references/               # 11 research-backed reference files
├── _research/sources.json    # the 237-source citation index
└── scripts/save_guide.py     # export a guide to a local Markdown file (no accounts needed)
```

No API keys, no Google account, no external auth required.

---

Built by [NexusPoint](https://nexus-point.co/) - AI systems, automation, and web. If this is useful and you want this kind of thing built for your business, that's what we do.

## License

[MIT](./LICENSE) - use it, fork it, ship it.
