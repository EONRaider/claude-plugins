# EONRaider's Claude Code Marketplace

A single [Claude Code plugin marketplace](https://docs.claude.com/en/docs/claude-code/plugin-marketplaces) listing every tool EONRaider publishes, wherever each one actually lives:

- [**foreman**](https://github.com/EONRaider/foreman) — personal orchestrator that tracks a repo's Initiative through an agent-assisted engineering methodology, phase by phase.
- [**skillartisan**](https://github.com/EONRaider/SkillArtisan) — build, validate, secure, and maintain Claude Skills.
- [**solid-coding**](https://github.com/EONRaider/solid-coding) — write and refactor code against SOLID, GoF design patterns, and complementary principles, with every finding adversarially verified.
- [**simplicity**](https://github.com/EONRaider/simplicity) — `/simplicity:just-ask` asks every open question with a recommendation; `/simplicity:just-say-it` re-states the last response as a short plain list; `/simplicity:what-now` lists what's done, where the task stands and what's next; `/simplicity:just-finish-it` pushes, opens PRs, waits for CI and merges what passes, through `gh` or the GitHub MCP server; `/simplicity:cleanup` runs an end-of-session checklist; `/simplicity:rename-session` renames the session after what it was about; `/simplicity:promptfy` rewrites a prompt into a stronger one without running it. Every skill except `just-finish-it` also runs when named mid-sentence.
- [**agent-router**](https://github.com/EONRaider/agent-router) — sizes subagents to the task: four pre-sized agent tiers, an enforcement hook, a per-project spawn log, and `/agent-router:report`, which proposes tier changes for a person to accept or reject.

This repo holds nothing but the marketplace manifest (`.claude-plugin/marketplace.json`) — each plugin's actual code stays in its own repo, referenced here by source.

## Install

```bash
claude plugin marketplace add EONRaider/claude-plugins
claude plugin install foreman@eonraider
claude plugin install skillartisan@eonraider
claude plugin install solid-coding@eonraider
claude plugin install simplicity@eonraider
claude plugin install agent-router@eonraider
```

## Update

Each plugin is pinned to a release tag and commit, so new versions arrive through this manifest. Refresh the marketplace, then update the plugins you use (restart Claude Code afterwards):

```bash
claude plugin marketplace update eonraider
claude plugin update simplicity@eonraider
```

## License

[MIT](LICENSE)
