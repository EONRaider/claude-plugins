# EONRaider's Claude Code Marketplace

A single [Claude Code plugin marketplace](https://docs.claude.com/en/docs/claude-code/plugin-marketplaces) listing every tool EONRaider publishes, wherever each one actually lives:

- [**foreman**](https://github.com/EONRaider/foreman) — personal orchestrator that tracks a repo's Initiative through an agent-assisted engineering methodology, phase by phase.
- [**skillartisan**](https://github.com/eonraider/SkillArtisan) — build, validate, secure, and maintain Claude Skills.

This repo holds nothing but the marketplace manifest (`.claude-plugin/marketplace.json`) — each plugin's actual code stays in its own repo, referenced here by source.

## Install

```bash
claude plugin marketplace add EONRaider/claude-plugins
claude plugin install foreman@eonraider
claude plugin install skillartisan@eonraider
```

## License

[MIT](LICENSE)
