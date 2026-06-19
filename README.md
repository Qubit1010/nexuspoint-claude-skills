# NexusPoint Claude Skills

Free, research-backed [Claude Code](https://docs.claude.com/en/docs/claude-code) skills from [NexusPoint](https://nexus-point.co/). Two installable skills, each grounded in a NotebookLM synthesis of cited 2026 sources, no API keys or accounts required.

## claude-advisor

The go-to guide to **everything Claude**, as an installable skill. Ask it anything about Claude and get a specific, sourced answer instead of a vague one:

- **"Which Claude should I use for this?"** chat vs Claude Code vs Cowork, with a decision table.
- **"Opus vs Sonnet vs Haiku for X?"** model selection grounded in 2026 specs and pricing.
- **"Can I build this workflow in Claude Code?"** feasibility first, then the build shape.
- **"Best plugins / MCP servers / tools?"** the ecosystem map.
- **"Which plan should I buy?"** Free / Pro / Max / Team / Enterprise, and how Claude compares to ChatGPT and Gemini.

Grounded in a **NotebookLM synthesis of 237 cited 2026 sources**, with honesty flags on anything version- or price-sensitive.

## marketing-advisor

A **research-backed marketing advisor** for agencies and founders. Strategy and benchmarks, not framework dumps:

- **"How do I get more clients?"** channel selection paced to 2026 reply/connection-rate benchmarks.
- **"Who should I target?"** ICP definition, scoring, and intent signals.
- **"What should I post?"** LinkedIn / Instagram-Reels strategy and content calendars.
- **"How should I price/package this?"** offer positioning on the Value Equation with 2026 agency pricing data.
- **"Is X still working?"** a sourced kill list of stale tactics, plus a live benchmark scoreboard.

Grounded in a **NotebookLM synthesis of 234 cited 2026 sources**. Strategy only - it frames the plan; the actual outreach copy is a separate pass.

## leads-to-crm

An **outreach lead router** for agencies and teams. Scrape leads manually on Instagram or LinkedIn → drop them in a source Google Sheet → run this skill → new leads land in your CRM with a personalized Touch 1 message, and nothing gets duplicated or silently dropped.

- **Identity-based dedup** on `@handle` / LinkedIn slug — not raw URLs. Idempotent: run it twice, the second run appends zero rows.
- **Two bugs fixed by design:** post-URL scrapes used to collapse to a useless key (duplicates) or get hard-dropped as "invalid" (lost leads). This skill never auto-filters; it trusts the rows you curated.
- **Touch 1 generation:** OpenAI `gpt-5.4-mini` primary, Claude Haiku fallback. Rotates opener archetypes per lead. Set `SENDER_IDENTITY` env var to describe yourself (default: "a founder at a digital agency").
- **Channel-config-driven:** Instagram + LinkedIn today; adding Facebook is a one-subclass extension with no changes to the push engine.
- **Needs:** `gws` CLI (Google Workspace CLI) authenticated to your Google account + Sheet IDs in env vars. No hardcoded credentials.

Trigger phrases: "push leads to CRM", "sync my instagram leads", "run the linkedin push", "any new leads to push", "dedup the CRM", "fill the blank DMs".

## Install

In Claude Code, add the marketplace once, then install any or all skills:

```
/plugin marketplace add Qubit1010/nexuspoint-claude-skills
/plugin install claude-advisor
/plugin install marketing-advisor
/plugin install leads-to-crm
```

The skills activate automatically when you ask a matching question.

## Use it on Claude.ai (no Claude Code needed)

Each skill folder also works as an uploadable Skill on Claude.ai (Settings -> Capabilities -> Skills). Zip the inner skill folder (e.g. `plugins/claude-advisor/skills/claude-advisor/`) and upload it.

## What's inside

```
plugins/
├── claude-advisor/skills/claude-advisor/       # SKILL.md + 11 references + 237-source index
├── marketing-advisor/skills/marketing-advisor/ # SKILL.md + 11 references + 234-source index
└── leads-to-crm/skills/leads-to-crm/          # SKILL.md + push engine + channel config + archetypes
```

`claude-advisor` and `marketing-advisor` require no API keys or Google account. `leads-to-crm` requires `gws` CLI + Google Sheet IDs (see its SKILL.md Setup section).

---

Built by [NexusPoint](https://nexus-point.co/) - AI systems, automation, and web. If this is useful and you want this kind of thing built for your business, that's what we do.

## License

[MIT](./LICENSE) - use it, fork it, ship it.
