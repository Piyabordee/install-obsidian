# Template: Feature Doc

> Use for: user-facing features with non-obvious workflows
> Location: `docs/features/<feature-name>.md`

---

## Structure

```markdown
# [Feature Name]

> One-line description of what this feature does.

---

## Overview
[What is this feature? Why does it exist? What problem does it solve?]

## When to Read This

### Trigger

- (fill from doc content)

### Read With

- `path/to/file.md` [[wiki-link]] — reason

## Flow / User Journey
[Step-by-step walkthrough of how a user interacts with this feature.
Use numbered steps or a sequence diagram if helpful.]

## Key Files
[Table of files involved in this feature and their roles.
Only include files that are NOT obvious from the feature name.]

## Configuration
[Any config options related to this feature.
Table format: config key, default, purpose.]

## Design Origin
- Spec: [[path-to-spec]]
- Plan: [[path-to-plan]]
(Include only if a spec/plan exists. Omit entire section if not.)

---

Related: [[linked-doc-1]] | [[linked-doc-2]]
```

## Guidelines

- **Flow section** is the most important — it's what makes this doc valuable
- **Key Files** should explain WHY each file matters, not just list them
- **Configuration** is optional — omit if feature has no config
- Every feature doc should link to at least one architecture doc

---

## Related

- [[INSTALL]] — How this template is used during implementation
- [[TEMPLATES/architecture-doc]] — Feature docs link to architecture docs
- [[TEMPLATES/project-doc]] — Project overview connects to feature docs
- [[PHASES/03-implement]] — Phase that creates feature docs
