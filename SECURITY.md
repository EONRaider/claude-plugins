# Security policy

## Supported versions

Only the current manifest on `master` is supported.

## Reporting a vulnerability

Please do not open a public issue. Report privately through GitHub:
[Report a vulnerability](https://github.com/EONRaider/claude-plugins/security/advisories/new).

Include what you found and how to reproduce it. You can expect a first reply within seven
days. Once a fix is released the advisory is published and you are credited, unless you ask
not to be.

## What counts

This repository holds only the marketplace manifest. It decides which code Claude Code installs
when someone adds a plugin from it. Problems of particular interest:

- an entry whose `sha` is not the commit its `ref` tag points at, or whose `url` is not the
  plugin's real repository;
- an entry that isn't pinned to a tag and a full commit id;
- a way to make `claude plugin install` fetch code other than what an entry pins.

A vulnerability in a plugin's own code belongs on that plugin's repository, which has its own
security policy. If you aren't sure where a problem lives, report it here.
