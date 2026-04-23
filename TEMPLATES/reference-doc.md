# Template: Reference Doc

> Use for: config systems, constants, paths, conventions
> Location: `docs/reference/<topic>.md`

---

## Structure

```markdown
# [Reference Topic]

> One-line description of what this reference covers.

---

## Overview
[Brief explanation of what this system/concept is.]

## Context Snapshot
[Scope and assumptions for this reference topic.]

## When to Read This

### Trigger

- (fill from doc content)

### Read With

- `path/to/file.md` [[wiki-link]] — reason

## Reference Table
[Primary content — table of entries with their values, locations, and purposes.
This is the main value of a reference doc.]

## How It Works
[Explanation of the mechanism — how values are determined, resolved, etc.]

## Platform Differences
(If applicable — how behavior differs across platforms/environments.)

## Common Mistakes
(If applicable — pitfalls that developers commonly hit.)

## Decision Trace
(Optional — include only reference-level decisions with lasting impact.)

- Decision: [what was chosen]
- Why: [reason/tradeoff]
- Impact: [what users/maintainers should preserve]

---

Related: [[linked-doc-1]] | [[linked-doc-2]]
```

## Guidelines

- **Reference Table** is the core — make it complete and accurate
- Values should come from actual code, not assumptions
- "How It Works" should explain the WHY, not just the WHAT
- Reference docs are stable — they change less frequently than feature docs
- Keep entries high-signal; avoid duplicating values already obvious from nearby docs

---

## Related

- [[INSTALL]] — How this template is used during implementation
- [[TEMPLATES/architecture-doc]] — Architecture defines what goes into reference
- [[TEMPLATES/index-doc]] — Index doc links to all reference docs
