# Phase 5: OPTIMIZE LINKS

> Final link pass after implementation and cleanup.
> Remove duplicate/valueless links and improve Obsidian graph clarity.

---

## Objective

Optimize wiki-link structure in `CLAUDE.md` and all files under `docs/` so links stay useful, non-redundant, and token-efficient.

## Precondition

- Phase 3: IMPLEMENT is complete
- Phase 4: CLEANUP is complete (or explicitly skipped by the human)
- Human approved entering final optimization pass

## What counts as a valueless link

Treat a link as valueless when it does not improve navigation or understanding, for example:

- Duplicate link to the same target within one section where one link is enough
- Placeholder-style links (example-only targets) left in final docs
- Bidirectional links that only reference each other without adding context
- Broad hub spam (too many low-signal links in one paragraph)

Do NOT remove links that are needed for navigation, provenance, or safety context.

## Steps

### 5.1 Build Link Inventory

Scan:

- `CLAUDE.md`
- `docs/**/*.md`

Collect:

- source file + section
- target file
- duplicate counts

### 5.2 Identify Optimization Candidates

Classify each candidate:

- `duplicate` — same target repeated unnecessarily
- `valueless` — no meaningful navigation or context gain
- `keep` — valuable link, keep as-is

### 5.3 Apply Minimal Edits

Edit only what improves signal:

1. Remove duplicates in the same local context
2. Remove valueless links
3. Keep at least core navigational links for each doc (hub/index/related)
4. Preserve links required for migration evidence, warnings, and design origin

### 5.4 Graph Cleanliness Check

Verify:

- No broken wiki links
- Hubs remain connected (`CLAUDE.md`, `docs/_index.md`)
- Spoke docs are not isolated unless intentionally standalone
- Link density is readable (avoid overloaded sections)

### 5.5 Report Outcome

Present:

```markdown
## Link Optimization Complete

### Files Updated
- [list files]

### Links Removed
- duplicate: [count]
- valueless: [count]

### Links Kept by Design
- [critical links retained and why]

### Verification
- [ ] no broken wiki links
- [ ] hub docs still connected
- [ ] graph readability improved
```

---

## Related

- [[INSTALL]] — main flow
- [[PHASES/03-implement]] — docs creation phase
- [[PHASES/04-cleanup]] — cleanup phase before final optimization
- [[PRINCIPLES]] — usefulness-first linking principles
