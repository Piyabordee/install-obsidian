# PRINCIPLES — Design Philosophy

> The rules that guide every documentation decision.
> Read this before designing any doc tree.

---

## Core Principles

### 1. Docs follow the codebase, not the other way around

Documentation structure must reflect the ACTUAL repo structure. Do not impose a predefined folder tree. Instead:

- Analyze what the repo actually contains
- Identify real subsystems, workflows, and important files
- Create docs only where they add genuine value

### 2. Hub-and-spoke architecture

```
CLAUDE.md (hub)
    ├── links to → docs/_index.md (navigation)
    ├── links to → docs/project/* (project knowledge)
    ├── links to → docs/architecture/* (structure knowledge)
    ├── links to → docs/features/* (behavior knowledge)
    └── links to → docs/reference/* (stable reference)
```

- **CLAUDE.md** = front door. Compact. Link-heavy. No encyclopedia.
- **docs/_index.md** = second door. Full navigation map.
- **Category folders** = rooms. Each doc = one focused topic.

### 3. Every doc earns its existence

Before creating a doc, answer:

- Does this doc contain information NOT derivable from reading the code?
- Does this doc help a newcomer (human or AI) understand the system faster?
- Would this doc be missed if it were deleted?

If the answer to all three is "no", do not create it.

### 4. Link generously, duplicate never

- Use wiki links: `[[docs/project/overview]]`
- When information exists elsewhere, link to it instead of rewriting it
- Every doc should have a `Related:` section at the bottom

### 5. CLAUDE.md is for AI onboarding

CLAUDE.md should contain ONLY:

- Project identity (name, stack, version)
- Read-first links
- Quick commands
- Working rules
- Documentation map (links to all docs)
- Key warnings for risky areas
- Doc Workflow (so AI knows to auto-create docs for new features)

CLAUDE.md should NOT contain:

- Detailed architecture explanations
- Full dependency lists
- Code examples
- Troubleshooting guides

### 6. Design Origin tracks provenance

When a feature doc was created from a design spec or implementation plan, add a `## Design Origin` section:

```markdown
## Design Origin
- Spec: [[path-to-spec]]
- Plan: [[path-to-plan]]
```

This helps AI agents understand where a feature came from and find the original design decisions.

### 7. Optimize for the graph, but usefulness first

- Wiki links make Obsidian graph meaningful
- Hub docs (CLAUDE.md, _index.md) should connect to many spokes
- Spoke docs should connect to related spokes
- But never add links that don't help navigation — visual prettiness is secondary

---

## Category Guide

| Category | When to create | Key questions to answer | Template |
|----------|---------------|------------------------|----------|
| `docs/project/` | Always | What is this? What changed? What's broken? | [[TEMPLATES/project-doc]] |
| `docs/architecture/` | When codebase has identifiable structure | How does it fit together? What are the layers? | [[TEMPLATES/architecture-doc]] |
| `docs/features/` | When features have non-obvious workflows | How does this feature work end-to-end? | [[TEMPLATES/feature-doc]] |
| `docs/integrations/` | When external tools/libraries have non-trivial usage | How is [tool] used? Where are the binaries? | [[TEMPLATES/integration-doc]] |
| `docs/build/` | When build/packaging is non-trivial | How to build? How to release? | [[TEMPLATES/build-doc]] |
| `docs/testing/` | When testing approach matters | How to test? What's the strategy? | [[TEMPLATES/testing-doc]] |
| `docs/reference/` | When config/paths/constants need explanation | What does this constant mean? How does path resolution work? | [[TEMPLATES/reference-doc]] |

Not every repo needs every category. Create only what the codebase justifies.

---

## Anti-Patterns to Avoid

| Anti-pattern | Why it's bad |
|-------------|-------------|
| One doc per folder regardless of value | Creates noise, dilutes graph |
| Copying README into docs/overview.md | Duplication, maintenance burden |
| Giant CLAUDE.md with everything | AI context waste, hard to update |
| Empty docs "for completeness" | Worse than no docs — misleading |
| Static hardcoded paths in templates | Breaks when used in different repos |
| No links between docs | Isolated nodes, graph is useless |

---

## Success Criteria

The documentation system is successful when:

1. A new AI agent can read CLAUDE.md and immediately know where to find information
2. The Obsidian graph shows meaningful clusters, not isolated islands
3. Adding a new feature doc is a 5-minute task (template + fill + link)
4. No doc contains information that's obvious from reading the code
5. Every doc has at least 2 incoming links from other docs

---

## Related

- [[INSTALL]] — How these principles are applied in practice
- [[README]] — Project overview
- [[PHASES/01-analyze]] — Phase 1 uses these principles to analyze repos
- [[PHASES/02-design]] — Phase 2 designs doc trees following these rules
- [[PHASES/03-implement]] — Phase 3 implements docs based on these principles

### Template References

| Principle | Relevant Template |
|-----------|------------------|
| Hub-and-spoke architecture | [[TEMPLATES/hub-claude-md]], [[TEMPLATES/index-doc]] |
| Every doc earns its existence | [[TEMPLATES/project-doc]], [[TEMPLATES/feature-doc]] |
| Link generously, duplicate never | [[TEMPLATES/architecture-doc]], [[TEMPLATES/reference-doc]] |
| Optimize for the graph | [[TEMPLATES/integration-doc]], [[TEMPLATES/testing-doc]] |
