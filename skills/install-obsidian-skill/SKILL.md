---
name: install-obsidian-skill
description: Knowledge base for the install-obsidian phased documentation workflow, including strict/adaptive mode selection, migration safety, and delta-refresh update behavior.
---

# install-obsidian Skill

## Purpose

Provide operational rules and checklists to run install-obsidian consistently through command → agent → skill orchestration.

## Core Rules

- Preserve phase order: Analyze → Design → Implement → Cleanup → Optimize Links
- Do not skip human approvals between analysis/design/implementation gates
- Keep stable rules inside `./.claude/rules/` and operational flow in `CLAUDE.md`
- Avoid empty placeholders and duplicated documentation
- Keep wiki-link format `[[...]]` without `.md` suffix

## Mode Selection

- Default mode: `strict`
- Optional mode: `adaptive`
- Mode must be stated before Phase 2 proposal

## Delta Refresh Mode

For `/install-obsidian:update <range>`:
- Update only docs affected by the specified commit range
- Do not automatically re-run Phases 1-3 in full
- Report changed docs, untouched docs, and pending approvals

## Required Outputs

- `CLAUDE.md` and `docs/_index.md` must remain hub documents
- `decisions.md` must capture notable durable decisions
- Final pass must validate links and avoid low-signal graph clutter
