# Template: Project Doc

> Use for: project-level knowledge (overview, repo map, fork changes, known issues)
> Location: `docs/project/<topic>.md`

---

## Structure

```markdown
# [Project Topic]

> One-line description.

---

## Overview
[The main content — varies by topic:]

### For overview.md:
- Project identity (name, type, repo URL)
- Stack/technology table
- Core features list
- Dependencies

### For repository-map.md:
- Package/source directory tree with annotations
- Support directories with purposes
- Entry points
- Migration map (if restructured)

### For fork-changes.md:
- Numbered list of changes from upstream
- Links to feature docs for each change

### For known-issues.md:
- High/Medium/Low priority sections
- Known limitations
- Technical debt items

---

Related: [[linked-doc-1]] | [[linked-doc-2]]
```

## Guidelines

- Project docs are the most stable — they change infrequently
- overview.md should be the first doc any newcomer reads
- repository-map.md should explain WHY folders exist, not just list them
- known-issues.md should be honest — don't hide problems

---

## Related

- [[INSTALL]] — How this template is used during implementation
- [[TEMPLATES/feature-doc]] — Features are documented separately
- [[TEMPLATES/index-doc]] — Index doc links to all project docs
- [[PHASES/01-analyze]] — Analysis feeds into project docs
