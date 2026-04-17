# Phase 3: IMPLEMENT

> Create the documentation files approved in Phase 2.
> Follow the priority order from the approved design.

---

## Objective

Build the documentation system. Every file must have real content derived from repo analysis.

## Steps

### 3.1 Create Directory Structure

Create only the directories that were approved in Phase 2. Do NOT create categories that were not approved.

```bash
# Example — adjust to match the approved doc tree:
mkdir -p docs/project docs/architecture docs/features docs/reference
```

### 3.2 Create docs/_index.md

Use the `TEMPLATES/index-doc.md` pattern:
- Navigation hub with links to all docs
- Organized by category
- Include existing related files (README, etc.)

### 3.3 Create Docs in Priority Order

For each approved doc:

1. **Choose the right template** from `TEMPLATES/`
2. **Fill with real information** from your Phase 1 analysis
3. **Add wiki links** to related docs
4. **Add Design Origin** if the feature has a spec/plan
5. **Add Related section** at the bottom

Rules while writing:
- Every paragraph must contain information NOT obvious from the code
- Every doc must link to at least 2 other docs
- No doc should be a copy of something that already exists elsewhere
- Use the repo's actual terminology, not generic terms

### 3.4 Create CLAUDE.md

Use `TEMPLATES/hub-claude-md.md` as the structure guide:
- Keep it compact (<100 lines if possible)
- All links must point to real docs that exist
- Working Rules must be specific to THIS repo
- Doc Workflow section must be included

### 3.5 Handle Existing Docs

Per the approved migration plan:
- Keep, redirect, or link existing docs as approved
- Do NOT delete anything the human hasn't explicitly approved for deletion
- If in doubt, preserve and link

### 3.6 Final Verification

After creating all docs:

- [ ] Every doc has real content (no empty placeholders)
- [ ] Every wiki link points to an existing file
- [ ] CLAUDE.md links to every doc in the Documentation Map
- [ ] docs/_index.md links to every doc
- [ ] Every doc has a Related section with at least 2 links
- [ ] Doc Workflow section exists in CLAUDE.md
- [ ] No hardcoded assumptions from other repos
- [ ] No information was lost from existing docs (if migration)

---

## Output

Present the result:

```markdown
## Implementation Complete

### Created
- [list all new files]

### Modified
- [list all changed files]

### Preserved
- [list untouched files]

### Verification
- [checklist results]
```

Wait for the human's final review.
