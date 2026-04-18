# Template: Architecture Doc

> Use for: structural patterns, subsystem design, layer descriptions
> Location: `docs/architecture/<topic>.md`

---

## Structure

```markdown
# [Architecture Topic]

> One-line description of this architectural aspect.

---

## Overview
[What is this architectural pattern/layer/subsystem?]

## Structure
[Visual representation — tree diagram, layer diagram, or composition table.
Show how parts relate to each other.]

## Component Reference
[Table of components with their location and responsibility.
Only include non-obvious components.]

## How to Extend
[When someone needs to add to this architecture, what do they do?
Step-by-step guide for common extension patterns.]

## Design Origin
(Omit if not applicable)

---

Related: [[linked-doc-1]] | [[linked-doc-2]]
```

## Guidelines

- **Structure** section should make the architecture visible at a glance
- **How to Extend** is critical — it's the main reason this doc exists
- Architecture docs should link to feature docs that implement the patterns
- Do NOT list every file — only the ones that define the architecture

---

## Related

- [[INSTALL]] — How this template is used during implementation
- [[TEMPLATES/feature-doc]] — Feature docs link to architecture docs
- [[TEMPLATES/reference-doc]] — Reference docs complement architecture docs
- [[TEMPLATES/index-doc]] — Index doc links to all architecture docs
