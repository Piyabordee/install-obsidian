# Phase 4: CLEANUP

> Remove installer artifacts and obsolete files after successful installation.
> Do NOT delete anything without explicit human confirmation.

---

## Objective

Clean up files that are no longer needed after the documentation system is installed and reviewed.

## Precondition

- Phase 3 is complete AND the human has approved the final review
- Do NOT run this phase if the human flagged issues in Phase 3

## Steps

### 4.1 Identify Files Marked for Removal

During [[PHASES/02-design]], the migration plan tracked which existing files had their content
redistributed into the new doc structure. Cross-reference that plan to build a
candidate list.

Also detect any additional files that may now be redundant:

1. **Read the Phase 2 migration plan** — it lists files proposed for removal
2. **Verify content migration** — for each file on the list, confirm that its
   information now exists in the new docs:
    - Open the original file
    - Search the new docs for the same information
    - Mark as `verified` only if all meaningful content has been migrated
    - Record section-level evidence (source heading -> destination file/heading)
3. **Flag uncertainties** — if any content might have been lost, mark as `uncertain`

If the file is `AGENTS.md`, section-level verification is mandatory and must reference
the mapping produced in [[PHASES/02-design]] (recommended format: [[TEMPLATES/migration-map]]).

### 4.2 Detect Installer Directory

Check if `install-obsidian/` (this installer) exists in the repo root.

- If found, note its path and size
- If not found (installer was run from outside the repo), skip this step

### 4.3 Present Cleanup Report

Show the human a structured report of everything identified:

```markdown
## Cleanup Report

### Files with migrated content (verified)
- [ ] `AGENTS.md` — content moved to [[docs/project/overview]], [[docs/architecture/structure]]
- [ ] `path/to/old-file.md` — content moved to [[docs/features/workflow]]

### Files with uncertain migration
- [ ] `path/to/risky-file.md` — partial migration, some content may be lost

### Installer directory
- [ ] `install-obsidian/` — the installer itself (can be re-downloaded if needed)

### Files to preserve (do NOT delete)
- [list any files that were NOT migrated or should be kept]
```

### 4.4 Get Human Confirmation

For EACH item in the report, ask the human individually:

> "Delete `AGENTS.md`? Its content has been verified in:
> - [[docs/project/overview]] (sections X, Y)
> - [[docs/architecture/structure]] (section Z)
>
> [yes / no / skip]"

Rules:
- **Never batch-delete** — confirm each file individually
- **Never delete `uncertain` files** unless the human explicitly overrides
- **Never delete files not in the report** — if a file wasn't analyzed, don't touch it
- If the human says "no" or "skip" for any file, preserve it
- **Never delete `AGENTS.md`** unless every meaningful section is `verified` with section-level evidence

### 4.5 Execute Cleanup

After receiving confirmation for each item:

1. Delete only the files the human approved
   - Keep `AGENTS.md` if any section is `uncertain` or missing evidence
2. If `install-obsidian/` was approved for deletion, remove the entire directory
3. Verify no broken links were created by the deletion:
   - Search all docs for wiki links to deleted files
   - If broken links are found, report them immediately and offer to fix

### 4.6 Post-Cleanup Verification

- [ ] No broken wiki links remain
- [ ] No referenced files were accidentally deleted
- [ ] docs/_index.md still links to valid files
- [ ] CLAUDE.md Documentation Map still links to valid files

---

## Output

Present the cleanup result:

```markdown
## Cleanup Complete

### Deleted
- [list all deleted files]

### Preserved
- [list files the human chose to keep]

### Broken Links Fixed
- [list any links that were updated after deletion]

### Verification
- [checklist results]
```

If the installer directory (`install-obsidian/`) was deleted, note that this
conversation was driving the installer and the human should be aware it is gone.

---

## Related

- [[INSTALL]] — Main instruction flow
- [[PHASES/02-design]] — Phase 2: migration plan originates here
- [[PHASES/03-implement]] — Phase 3: must be complete before cleanup
- [[PHASES/05-optimize-links]] — Final pass after cleanup to optimize wiki links
