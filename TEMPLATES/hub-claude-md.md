# Template: CLAUDE.md Hub

> Use for: CLAUDE.md — the file that AI agents read first
> Location: repo root

---

## Structure

```markdown
# [Project Name] — Project Hub

> Central operational hub for AI agents working on this codebase.
> For full documentation index, see [[docs/_index]].

---

## Identity

| Field | Value |
|-------|-------|
| Name | [project name] |
| Type | [project type] |
| Stack | [key technologies] |
| Version | [current version] |
| Repo | [repo URL] |

---

## Read First

- [[docs/_index]] — Full documentation map
- [[docs/project/overview]] — Project identity and stack
- [[README]] — User-facing introduction

---

## Quick Commands

```bash
[command to run]
[command to test]
[command to build]
```

---

## Working Rules

1. **[Rule 1]** — [why]
2. **[Rule 2]** — [why]
3. **[Rule 3]** — [why]
... (keep to 5-8 rules, repo-specific)

---

## Doc Workflow

When creating or significantly modifying a feature:

1. **Spec + Plan** — create in `docs/superpowers/` (if using that workflow)
2. **Feature doc** — create in `docs/features/` or appropriate category
3. **Design Origin** — link to spec/plan if applicable
4. **Link here** — add entry to Documentation Map below
5. **Link related docs** — add wiki links in Related section

### Where to put docs

| Category | Path | When |
|----------|------|------|
| Feature workflow | `docs/features/` | New user-facing behavior |
| Architecture | `docs/architecture/` | Structural changes |
| Reference | `docs/reference/` | New constants, config options |
| Project | `docs/project/` | Known issues, project changes |

---

## Documentation Map

### Project
- [[docs/project/overview]] — [one-line description]
- [[docs/project/repository-map]] — [one-line description]
... (only include categories that have docs)

### Architecture
- [[docs/architecture/...]] — [one-line description]

### Features
- [[docs/features/...]] — [one-line description]

### Reference
- [[docs/reference/...]] — [one-line description]

---

## Key Warnings

- **[Warning 1]** — see [[docs/path-to-detail]]
- **[Warning 2]** — see [[docs/path-to-detail]]

---

## Related Files

- [[README]] — User-facing intro
- [[AGENTS]] — (if preserved during transition)
```

## Guidelines

- Keep CLAUDE.md under 100 lines
- Every link must point to a real file
- Working Rules must be specific to THIS repo (no generic rules)
- Key Warnings should point to docs that explain the risk
- Doc Workflow section must exist so AI knows to auto-create docs

---

## Related

- [[INSTALL]] — Main instruction flow that sets up CLAUDE.md
- [[TEMPLATES/index-doc]] — The second navigation hub after CLAUDE.md
- [[PHASES/02-design]] — Phase that designs the CLAUDE.md structure
- [[PHASES/03-implement]] — Phase that creates CLAUDE.md
