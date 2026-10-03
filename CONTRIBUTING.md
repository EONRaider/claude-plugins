# Contributing to EONRaider's Claude Code marketplace

This repository holds one file that matters: `.claude-plugin/marketplace.json`. Each plugin's
code lives in its own repository, and bugs in a plugin belong there.

## Before you start

- This marketplace lists EONRaider's own plugins. It doesn't take third-party plugins.
- Corrections to an entry, the README or the checks are welcome. For anything larger, open an
  issue first.
- Security problems go through [private reporting](SECURITY.md), not public issues.
- By contributing you agree that your work is released under the [MIT license](LICENSE) and
  that you will follow the [Code of Conduct](CODE_OF_CONDUCT.md).

## Changing an entry

Every entry is pinned to a release tag and to the commit that tag points at.

1. Set `source.ref` to the plugin's new tag and `source.sha` to the tagged commit:

   ```bash
   git ls-remote https://github.com/EONRaider/<plugin>.git 'refs/tags/<tag>^{}'
   ```

2. If the entry has a `version`, set it to the plugin's version at that tag.
3. Refresh `description` and `keywords` so they cover everything the plugin ships.
4. Update the plugin's line in `README.md`.
5. Validate:

   ```bash
   claude plugin validate .claude-plugin/marketplace.json
   ```

## Pull requests

- Branch from `master`; `master` is protected and takes changes only through pull requests.
- Keep a PR to one plugin, or to one change.
- CI must pass. It checks that every entry is pinned to a tag and a full commit id, and that
  the README lists it.
