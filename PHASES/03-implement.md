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

Use the [[TEMPLATES/index-doc]] pattern:
- Navigation hub with links to all docs
- Organized by category
- Include existing related files (README, etc.)

### 3.3 Create Docs in Priority Order

For each approved doc:

1. **Choose the right template** from [[TEMPLATES/]]
2. **Fill with real information** from your Phase 1 analysis
3. **Add wiki links** to related docs
4. **Add Design Origin** if the feature has a spec/plan
5. **Add Related section** at the bottom
6. **Add context/rationale** where decisions are not obvious from code

Rules while writing:
- Every paragraph must contain information NOT obvious from the code
- Every doc must link to at least 2 other docs
- No doc should be a copy of something that already exists elsewhere
- Use the repo's actual terminology, not generic terms
- Keep each doc focused; split only when it improves retrieval and maintenance

### 3.4 Create CLAUDE.md

Use [[TEMPLATES/hub-claude-md]] as the structure guide:
- Keep it compact (<100 lines if possible)
- All links must point to real docs that exist
- Working Rules must be specific to THIS repo
- Doc Workflow section must be included
- Include an authoritative directory tree
- Keep stable/non-negotiable rules in `./.claude/rules/` (do not mix in CLAUDE.md)

### 3.5 Create Stable Rules + decisions.md

Create or update:

1. `./.claude/rules/` for stable rules (security/compliance/permanent constraints). Create all stable rule files referenced in CLAUDE.md (currently `stable-rules.md`, `security-rules.md`, `coding-behavior-rules.md`)—do not stop at `stable-rules.md` alone.
2. `decisions.md` for design rationale that must survive context resets

Rules:
- Stable rules must be linkable from CLAUDE.md
- decisions.md entries must include decision + rationale + impact
- Do not duplicate long explanations already covered in docs; link instead

### 3.6 Install Updating-Docs Skill

The `updating-docs` skill ships with this installer. Copy it to the target repo so future agents can maintain docs without re-learning the discipline:

```bash
# Read the skill from THIS installer repo and write to target
mkdir -p .claude/skills/updating-docs
```

1. Read the skill file from this installer repo at `.claude/skills/updating-docs/SKILL.md`
2. Write it to `<target>/.claude/skills/updating-docs/SKILL.md` (verbatim, no edits — the skill is generic by design)
3. Add a single line in `CLAUDE.md` "Read First" section: `.claude/skills/updating-docs` — Doc-update skill (read-first, write-second discipline)
4. If the target already has a `.claude/skills/` folder, merge carefully — preserve any existing skills, append the new one

This is a **core output** in both `strict` and `adaptive` modes.

### 3.7 Handle Existing Docs

Per the approved migration plan:
- Keep, redirect, or link existing docs as approved
- Do NOT delete anything the human hasn't explicitly approved for deletion
- If in doubt, preserve and link

### 3.8 Migration Coverage Gate (AGENTS.md)

If `AGENTS.md` exists:

1. Use the Phase 2 mapping table (or [[TEMPLATES/migration-map]]) as the source of truth
2. Verify each mapped section exists in its destination file/section
3. Produce a coverage summary:
   - `mapped sections: X/Y`
   - `verified migrated sections: X/Y`
   - `unmapped or uncertain sections: [list]`
4. Gate rule: coverage must be `Y/Y` (100%) before implementation can be considered complete
5. If any section is unmapped or uncertain, mark implementation as incomplete and return to migration work

### 3.9 Final Verification

After creating all docs:

- [ ] Every doc has real content (no empty placeholders)
- [ ] Every wiki link points to an existing file
- [ ] CLAUDE.md links to every doc in the Documentation Map
- [ ] docs/_index.md links to every doc
- [ ] Every doc has a Related section with at least 2 links
- [ ] Every created doc (except hub and index) has a "## When to Read This" section
- [ ] Every "When to Read This" has both Trigger and Read With subsections
- [ ] Every Read With entry uses the dual format: `path/file.md` [[wiki-link]] — reason
- [ ] Doc Workflow section exists in CLAUDE.md
- [ ] CLAUDE.md hub has a "## Task Routing" table derived from all Trigger sections
- [ ] Task Routing table uses backtick paths (not wiki links) for AI navigation
- [ ] CLAUDE.md contains an authoritative directory tree
- [ ] Stable rules exist in `./.claude/rules/` and are not mixed into CLAUDE.md
- [ ] decisions.md exists and includes key design choices
- [ ] `updating-docs` skill installed at `.claude/skills/updating-docs/SKILL.md`
- [ ] `updating-docs` skill referenced in `CLAUDE.md` "Read First"
- [ ] Verification commands passed for affected stack (`tsc --noEmit` for TypeScript repos)
- [ ] Work was committed in issue-scoped chunks
- [ ] CLAUDE.md updated at end of session
- [ ] No hardcoded assumptions from other repos
- [ ] No information was lost from existing docs (if migration)
- [ ] AGENTS.md migration coverage is 100% (if AGENTS.md exists)
- [ ] Migration evidence includes section-level destinations (not only file-level)
- [ ] Each major doc includes context/rationale, not only file summaries
- [ ] No low-signal duplicate-topic docs were created
- [ ] Hybrid model check passed (installer core preserved + inspired layer applied)

---

## Output

Present the result:

```markdown
## Implementation Complete

### Created
- [list all new files, including .claude/skills/updating-docs/SKILL.md]

### Modified
- [list all changed files, including CLAUDE.md Read First entry pointing to the skill]

### Preserved
- [list untouched files]

### Verification
- [checklist results, including skill installation]

### Migration Coverage (if AGENTS.md exists)
- mapped sections: [X/Y]
- verified migrated sections: [X/Y]
- unresolved sections: [list or "none"]
```

Wait for the human's final review.

---

## Related

- [[INSTALL]] — Main instruction flow
- [[PRINCIPLES]] — Design philosophy governing implementation
- [[PHASES/02-design]] — Previous phase: approved design
- [[PHASES/04-optimize-links]] — Next phase: optimize links
- [[TEMPLATES/architecture-doc]] — Architecture doc template
- [[TEMPLATES/feature-doc]] — Feature doc template
- [[TEMPLATES/project-doc]] — Project doc template
- [[TEMPLATES/reference-doc]] — Reference doc template
- [[TEMPLATES/hub-claude-md]] — CLAUDE.md hub template
- [[TEMPLATES/index-doc]] — Index doc template
- [[TEMPLATES/migration-map]] — Migration mapping template
- [[.claude/skills/updating-docs]] — Generic doc-update skill shipped with this installer
