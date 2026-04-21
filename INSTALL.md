# INSTALL — AI Agent Instructions

> Read this file FIRST. Follow phases in order.
> Do NOT skip phases. Each phase builds on the previous one.

---

## Overview

You are installing an Obsidian-compatible documentation system into this repository. You will:

1. **Analyze** the repo (do NOT assume anything)
2. **Design** a doc tree tailored to this specific codebase
3. **Create** interconnected docs with wiki links
4. **Set up** CLAUDE.md as the operational hub
5. **Set up** stable rules and decisions log (`.claude/rules/`, `decisions.md`)
6. **Clean up** installer artifacts and obsolete files (optional, user-approved)
7. **Optimize links** in `CLAUDE.md` and `docs/` for graph cleanliness and token efficiency

## Constraints

- **Do NOT create empty placeholder files** — every doc must have real content
- **Do NOT duplicate information** — link to existing docs instead of copying
- **Do NOT hardcode assumptions** — analyze the repo to discover its structure
- **Do NOT skip human approval** — present your design before implementing
- **Do NOT overwrite existing docs** unless the human explicitly approves
- **Do NOT mix stable rules into CLAUDE.md** — keep stable rules in `/.claude/rules/`

## Installation Mode (required)

Choose one mode before Phase 2 and include it in the design proposal.

### Mode: `strict` (full-standard structure)
- Create the standard category structure from [[README]]: `project`, `architecture`, `features`, `integrations`, `build`, `testing`, `reference`
- Create at least one real-content doc in each category, or explicitly link existing docs that satisfy the category
- Use this mode when the human expects the full standardized structure

### Mode: `adaptive`
- Keep the current behavior from [[PRINCIPLES]]: create only categories justified by the repo analysis
- Skip non-applicable categories
- Use this mode when minimal, structure-following documentation is preferred

If the human does not specify a mode, default to `strict`.

## Phase Sequence

| Phase | File | Description |
|-------|------|-------------|
| 1: ANALYZE | [[PHASES/01-analyze]] | Explore repo structure, identify key folders, subsystems, entry points |
| 2: DESIGN | [[PHASES/02-design]] | Propose doc tree, CLAUDE.md outline, migration plan |
| 3: IMPLEMENT | [[PHASES/03-implement]] | Create docs, write content, add links, set up hub |
| 4: CLEANUP | [[PHASES/04-cleanup]] | Remove installer artifacts and obsolete files (after human approval) |
| 5: OPTIMIZE LINKS | [[PHASES/05-optimize-links]] | Final link-quality pass: remove duplicate/valueless links, keep graph clean |

## How to Execute

1. Read [[PRINCIPLES]] to understand the design philosophy
2. Read [[PHASES/01-analyze]] and execute it fully
3. Present your analysis to the human, wait for acknowledgment
4. Read [[PHASES/02-design]] and execute it fully
5. Present your proposed doc tree to the human, wait for approval
6. Read [[PHASES/03-implement]] and execute it fully
7. Update `decisions.md` with notable design choices
8. Present the result for final review
9. Read [[PHASES/04-cleanup]] and execute it after human approves the review
10. Read [[PHASES/05-optimize-links]] and run final link optimization pass

## Templates

Use files in [[TEMPLATES/]] as structure guides. Each template defines:
- What sections a doc type should have
- What questions it should answer
- How it should link to other docs

| Template | Purpose |
|----------|---------|
| [[TEMPLATES/architecture-doc]] | Structural patterns and subsystem design |
| [[TEMPLATES/build-doc]] | Build process, packaging, release |
| [[TEMPLATES/feature-doc]] | User-facing feature workflows |
| [[TEMPLATES/hub-claude-md]] | CLAUDE.md hub structure |
| [[TEMPLATES/index-doc]] | Documentation navigation hub |
| [[TEMPLATES/integration-doc]] | External tools and libraries |
| [[TEMPLATES/migration-map]] | Section-by-section migration mapping (AGENTS.md and other docs) |
| [[TEMPLATES/project-doc]] | Project-level knowledge |
| [[TEMPLATES/reference-doc]] | Config, constants, conventions |
| [[TEMPLATES/testing-doc]] | Testing strategy and conventions |

Templates are NOT pre-filled content. You must fill them with real information from the repo.

## Completion Checklist

High-level verification — see [[PHASES/03-implement]] for the full detailed checklist.

- [ ] All approved docs created with real content
- [ ] CLAUDE.md and docs/_index.md created as hubs
- [ ] Stable rules created/updated in `/.claude/rules/`
- [ ] `decisions.md` created/updated with key design decisions
- [ ] Mode requirements satisfied (`strict` full standard categories OR `adaptive` justified subset)
- [ ] Wiki links connect related docs
- [ ] AGENTS.md migration coverage is 100% (if AGENTS.md exists)
- [ ] No critical information from AGENTS.md is lost
- [ ] No empty placeholder files or hardcoded assumptions
- [ ] Cleanup completed (installer and obsolete files removed or preserved per user choice)
- [ ] Link optimization completed for `CLAUDE.md` + `docs/` (duplicate/valueless links removed)

## Definition of Done

Installation is complete only when all of the following are true:

1. `CLAUDE.md` exists and is usable as the project hub
2. `docs/_index.md` exists and links to the full documentation set
3. Stable rules exist in `/.claude/rules/` and are referenced by `CLAUDE.md`
4. `decisions.md` exists for persistent design rationale
5. Core docs exist per selected mode:
    - `strict`: all standard categories from [[README]] are represented
    - `adaptive`: only analysis-justified categories are present (with rationale in Phase 2 output)
6. If `AGENTS.md` exists, all meaningful sections are mapped and migrated with evidence
7. Final link optimization pass completed on `CLAUDE.md` + `docs/`
8. Post-install validation checklist is complete with no unresolved critical failures

## Post-Install Validation (mandatory)

Run this checklist before closing the installation:

- [ ] `CLAUDE.md` exists and links to `[[docs/_index]]`
- [ ] `CLAUDE.md` includes an authoritative directory tree
- [ ] `docs/_index.md` links to every created doc
- [ ] Every created doc has real content (no placeholders)
- [ ] Every created doc has at least 2 useful related links
- [ ] No broken wiki links to missing files
- [ ] Selected mode validation passed (`strict` or `adaptive`)
- [ ] Stable rules are placed in `/.claude/rules/` (not mixed into CLAUDE.md)
- [ ] `decisions.md` records key design choices
- [ ] Verification command for affected stack passed (`tsc --noEmit` for TypeScript repos)
- [ ] Work was committed in issue-scoped chunks
- [ ] `CLAUDE.md` was updated at end of session
- [ ] AGENTS.md migration coverage report included (if AGENTS.md exists)
- [ ] Cleanup decisions were human-approved item by item
- [ ] Duplicate/valueless wiki links were removed from `CLAUDE.md` and `docs/`
- [ ] Link graph remains navigable and hub docs are still connected

---

## Troubleshooting & Edge Cases

### Repo has no clear structure
If the repo is a single-file project or lacks identifiable directories:
- Create a minimal doc tree: `CLAUDE.md` + `docs/_index.md` + `docs/project/overview.md`
- Skip categories that don't apply (no architecture doc if there's no architecture)

### Repo already has CLAUDE.md
- Read the existing CLAUDE.md first
- Preserve its content — merge with the new structure rather than overwriting
- Add the Documentation Map and Doc Workflow sections if missing
- Present the merge plan to the human for approval

### Phase 1 analysis is incomplete
- Report what you could and could not determine
- Mark uncertain findings explicitly
- Proceed with what you know — the human can fill gaps during the approval step

### Repo uses a non-standard language/framework
- Identify entry points based on the framework's conventions
- Note the unfamiliar stack in your analysis
- Use the generic [[PRINCIPLES]] guidelines — they apply to any stack

### Existing docs conflict with proposed structure
- Never delete existing docs without human approval
- Link existing docs from the new navigation hub
- Propose a migration plan in Phase 2

### AGENTS.md exists but migration is incomplete
- Do NOT proceed to Phase 3 until every meaningful AGENTS.md section is mapped to a destination
- Use [[TEMPLATES/migration-map]] to track section-level coverage
- Mark unknown or risky mappings explicitly and escalate to the human

---

## Related

- [[README]] — Project overview and usage guide
- [[PRINCIPLES]] — Design philosophy that governs all decisions
- [[CONTRIBUTING]] — How to contribute changes
- [[CHANGELOG]] — Version history

---

Start by reading [[PRINCIPLES]], then [[PHASES/01-analyze]].
