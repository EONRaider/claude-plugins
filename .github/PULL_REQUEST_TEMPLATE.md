## What changed

## Why

## How it was checked

- [ ] `claude plugin validate .claude-plugin/marketplace.json` passes
- [ ] `ref` is a pushed tag and `sha` is the commit that tag points at
- [ ] `version` (where the entry has one) matches the plugin's `plugin.json` at that tag
- [ ] `description` and `keywords` cover everything the plugin ships
- [ ] The plugin's line in README.md is up to date
