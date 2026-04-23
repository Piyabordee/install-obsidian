# Template: Migration Map

> Use for: section-by-section migration planning and verification (especially `AGENTS.md`)
> Location: `docs/project/migration-map.md` (or equivalent design artifact in Phase 2 output)

---

## Structure

```markdown
# Migration Map

> Source-to-destination map for migrated documentation.

---

## When to Read This

### Trigger

- (fill from doc content)

### Read With

- `path/to/file.md` [[wiki-link]] — reason

## Scope
- Source files: [e.g., AGENTS.md, old-doc.md]
- Migration mode: [strict/adaptive]
- Owner: [human/agent]
- Hybrid intent: [how installer core is preserved while inspired-layer improvements are applied]

## Section Mapping
| Source file | Source section | Destination file | Destination section | Migration method (rewrite/link/keep) | Verification evidence | Status |
|-------------|----------------|------------------|---------------------|---------------------------------------|-----------------------|--------|
| AGENTS.md | [section name] | [[docs/...]] | [heading] | rewrite | [dest heading + summary] | mapped |

Status values:
- `mapped` — planned destination exists
- `verified` — destination implemented and checked
- `uncertain` — partial or ambiguous migration
- `blocked` — cannot migrate without human decision

## Coverage Summary
- Total meaningful source sections: [N]
- Mapped sections: [N]
- Verified sections: [N]
- Uncertain/blocked sections: [list or "none"]

## Drift Guard Notes
- [confirm no duplicate-topic docs were introduced during migration]
- [confirm key rationale context was preserved, not only file references]

## Removal Candidates
| File | Eligible for removal? | Reason | Preconditions |
|------|------------------------|--------|---------------|
| AGENTS.md | no/yes | [why] | all sections verified + human approval |

---

Related: [[PHASES/02-design]] | [[PHASES/03-implement]] | [[PHASES/04-cleanup]]
```

## Guidelines

- Treat migration as section-level work, not file-level only
- Do not mark a file removable until all meaningful sections are verified
- Keep uncertain mappings visible and unresolved until human confirms
- Reuse this map in Phase 2 planning, Phase 3 verification, and Phase 4 cleanup
- Validate that migrated docs stay practical and high-signal (no template-only content)

---

## Related

- [[INSTALL]] — Main instruction flow with strict/adaptive mode and definition of done
- [[PHASES/02-design]] — Migration mapping is required here
- [[PHASES/03-implement]] — Migration coverage gate uses this map
- [[PHASES/04-cleanup]] — Cleanup verification references this map
