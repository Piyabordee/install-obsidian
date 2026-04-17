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
5. **Clean up** installer artifacts and obsolete files (optional, user-approved)

## Constraints

- **Do NOT create empty placeholder files** — every doc must have real content
- **Do NOT duplicate information** — link to existing docs instead of copying
- **Do NOT hardcode assumptions** — analyze the repo to discover its structure
- **Do NOT skip human approval** — present your design before implementing
- **Do NOT overwrite existing docs** unless the human explicitly approves

## Phase Sequence

```
Phase 1: ANALYZE     → PHASES/01-analyze.md
    Explore repo structure, identify key folders, subsystems, entry points

Phase 2: DESIGN      → PHASES/02-design.md
    Propose doc tree, CLAUDE.md outline, migration plan

Phase 3: IMPLEMENT   → PHASES/03-implement.md
    Create docs, write content, add links, set up hub

Phase 4: CLEANUP     → PHASES/04-cleanup.md
    Remove installer artifacts and obsolete files (after human approval)
```

## How to Execute

1. Read `PRINCIPLES.md` to understand the design philosophy
2. Read `PHASES/01-analyze.md` and execute it fully
3. Present your analysis to the human, wait for acknowledgment
4. Read `PHASES/02-design.md` and execute it fully
5. Present your proposed doc tree to the human, wait for approval
6. Read `PHASES/03-implement.md` and execute it fully
7. Present the result for final review
8. Read `PHASES/04-cleanup.md` and execute it after human approves the review

## Templates

Use files in `TEMPLATES/` as structure guides. Each template defines:
- What sections a doc type should have
- What questions it should answer
- How it should link to other docs

Templates are NOT pre-filled content. You must fill them with real information from the repo.

## Completion Checklist

High-level verification — see `PHASES/03-implement.md` for the full detailed checklist.

- [ ] All approved docs created with real content
- [ ] CLAUDE.md and docs/_index.md created as hubs
- [ ] Wiki links connect related docs
- [ ] No empty placeholder files or hardcoded assumptions
- [ ] Cleanup completed (installer and obsolete files removed or preserved per user choice)

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
- Use the generic PRINCIPLES.md guidelines — they apply to any stack

### Existing docs conflict with proposed structure
- Never delete existing docs without human approval
- Link existing docs from the new navigation hub
- Propose a migration plan in Phase 2

---

Start by reading `PRINCIPLES.md`, then `PHASES/01-analyze.md`.
