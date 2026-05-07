# decisions.md

> Persistent design decisions for this repository.

## 2026-04-21 — Separate stable rules from CLAUDE.md

- **Decision**: keep immutable rules in `./.claude/rules/` and use `CLAUDE.md` as operational hub.
- **Why**: reduce accidental overwrite risk in session-level edits and prompt-driven changes.
- **Impact**: agents must read stable rules first, then apply session instructions.

## 2026-04-21 — Keep an authoritative directory tree in CLAUDE.md

- **Decision**: include a repo tree snapshot in `CLAUDE.md`.
- **Why**: reduce path/structure misunderstanding across AI agents.
- **Impact**: update tree when structure changes.

## 2026-04-21 — Enforce explicit verification + session closeout

- **Decision**: add Definition of Done including `tsc --noEmit` for TypeScript repos and issue-scoped commits.
- **Why**: improve consistency and reduce regressions.
- **Impact**: agents must run verification and close every session with CLAUDE/decisions updates.

## 2026-04-23 — Adopt hybrid documentation strategy (core + inspired layer)

- **Decision**: preserve install-obsidian’s phase-based installer core, while adding llm-wiki-inspired practices as a complementary layer.
- **Why**: keep strong operational safeguards (approval gates, migration safety, stable rules) while improving retrieval quality via modular docs, better graph links, living updates, and rationale-first writing.
- **Impact**: README/INSTALL/PRINCIPLES/PHASES/TEMPLATES now enforce systematic-but-flexible behavior, drift prevention, and context-rich documentation expectations.

## 2026-05-07 — Define explicit re-install behavior for already-installed repos

- **Decision**: require agents to acknowledge prior installation status and prefer targeted refresh runs instead of fully repeating Phases 1-3 when docs are already in place.
- **Why**: reduce unnecessary churn and avoid duplicated work in repositories that have already completed installation and migration once.
- **Impact**: INSTALL and README now instruct agents to announce prior install context, run focused updates (often Phase 5), and avoid recreating `AGENTS.md` when migration coverage is already complete.

## 2026-05-07 — Define `/install-obsidian:update` as delta-only refresh mode

- **Decision**: treat `/install-obsidian:update <range>` as a targeted documentation refresh that only updates delta derived from the specified commit window.
- **Why**: make refresh behavior explicit, reduce accidental full reinstall work, and keep doc updates scoped to the code changes the human actually asked about.
- **Impact**: README, INSTALL, and Phase 5 now define supported range inputs, scope-control rules, required output, and delta-first link optimization expectations.

## 2026-05-07 — Add Claude Code Marketplace orchestration layer

- **Decision**: add Marketplace metadata and explicit command → agent → skill structure for install-obsidian.
- **Why**: make the repository directly usable from Claude Code Marketplace while preserving existing phase-based behavior as the source of truth.
- **Impact**: `.claude-plugin/`, `commands/`, `agents/`, and `skills/` now exist; README/INSTALL/PRINCIPLES/CLAUDE are updated to align with Marketplace usage without replacing installer core rules.
