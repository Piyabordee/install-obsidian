# Phase 2: DESIGN

> Propose a documentation tree tailored to this specific repo.
> Do NOT create any files yet. Only propose and wait for approval.

---

## Objective

Design the documentation architecture based on Phase 1 analysis.

## Steps

### 2.1 Propose Doc Tree

Based on the analysis, determine:

- Which category folders are justified (not every repo needs all categories)
- Which specific docs should exist (each must earn its existence per [[PRINCIPLES]])
- What CLAUDE.md should contain

Present the proposed tree:

```markdown
## Proposed Doc Tree

repo-root/
├── CLAUDE.md                  # [what it contains]
├── docs/
│   ├── _index.md              # [what it contains]
│   ├── project/
│   │   └── <name>.md          # [why this doc exists]
│   ├── architecture/
│   │   └── <name>.md          # [why this doc exists]
│   └── ...
```

For each proposed doc, explain:
- **Why** it should exist (what gap it fills)
- **Source** of its content (which repo analysis finding it addresses)
- **Links** it should have (to which other docs)

### 2.2 Propose CLAUDE.md Structure

Show the proposed sections of CLAUDE.md:
- Identity
- Read First links
- Quick Commands
- Working Rules
- Documentation Map
- Key Warnings
- Doc Workflow

### 2.3 Migration Plan

If existing docs (AGENTS.md, README, etc.) have valuable information:
- Show which sections go where
- Show what stays unchanged
- Show what gets linked vs. rewritten
- Propose whether to keep, redirect, or remove existing docs

If `AGENTS.md` exists, this mapping is mandatory and must be section-by-section.
Use [[TEMPLATES/migration-map]] and include every meaningful section.

Required AGENTS mapping table:

```markdown
### AGENTS.md Section Mapping (mandatory if AGENTS.md exists)
| AGENTS.md section | Destination file | Destination section | Migration method (link/rewrite/keep) | Status |
|-------------------|------------------|---------------------|----------------------------------------|--------|
| [section name] | [[docs/...]] | [heading] | rewrite | mapped |
```

Rules:
- Every meaningful AGENTS.md section must appear in this table
- `Status` must be `mapped` for all rows before Phase 3
- If a section cannot be mapped, stop and request human guidance
- Do NOT proceed to [[PHASES/03-implement]] with partial mapping

Include a **Files Marked for Removal** section:

```markdown
### Files Marked for Removal (pending Phase 4 verification)
| File | Content migrated to | Status |
|------|-------------------|--------|
| AGENTS.md | [[docs/project/overview]], [[docs/architecture/structure]] | proposed |
| old-doc.md | [[docs/features/workflow]] | proposed |
```

This list is used by Phase 4 to auto-detect and verify files eligible for cleanup.
Each file starts as `proposed` and gets verified during Phase 4.

### 2.4 Priority Order

List docs in creation order (most useful first):

1. `[most critical doc]` — why first
2. `[second doc]` — why second
3. ...

### 2.5 Hybrid Fit Check (required)

Add a brief check before Phase 3:

- **Core preserved:** phase gates, stable rules separation, migration safeguards remain intact
- **Inspired layer applied:** docs are modular, linked, living, and context/rationale-driven
- **Drift guard:** no category/doc exists only because a template suggested it
- **Signal check:** proposed doc count is justified by repo complexity

---

## Output

Present your design as:

```markdown
## Design Proposal: [Repo Name]

### Proposed Doc Tree
[file tree with explanations]

### CLAUDE.md Outline
[section structure]

### Migration Plan (if applicable)
[where existing info goes]

### AGENTS.md Migration Coverage
[100% required if AGENTS.md exists; otherwise "not applicable"]

### Priority Order
[creation sequence]

### Estimated Docs Count
[N docs to create]

### Hybrid Fit Check
[pass/fail + short rationale]
```

Wait for the human to approve or request changes before proceeding to [[PHASES/03-implement]].

---

## Related

- [[INSTALL]] — Main instruction flow
- [[PRINCIPLES]] — Design philosophy for doc tree decisions
- [[PHASES/01-analyze]] — Previous phase: repo analysis
- [[PHASES/03-implement]] — Next phase: create the docs
- [[TEMPLATES/hub-claude-md]] — Template for CLAUDE.md hub
- [[TEMPLATES/index-doc]] — Template for docs/_index.md navigation
- [[TEMPLATES/migration-map]] — Template for section-by-section migration planning
