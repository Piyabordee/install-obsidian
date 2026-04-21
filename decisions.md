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
