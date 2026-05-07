---
allowed-tools: Read, Glob, Grep
name: install-obsidian-install
description: Run the install-obsidian phased documentation installer in the current repository
---

# install-obsidian install

Invoke `@install-obsidian-agent` to install or refresh the Obsidian documentation system.

Use this command when you want to:
- run a full install flow (Analyze → Design → Implement → Cleanup → Optimize Links)
- choose `strict` or `adaptive` mode before Phase 2
- run delta-only refresh with `/install-obsidian:update <range>`
