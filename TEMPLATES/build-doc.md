# Template: Build Doc

> Use for: build process, packaging, and release procedures
> Location: `docs/build/<topic>.md`

---

## Structure

```markdown
# [Build/Packaging Topic]

> One-line description of the build or packaging process.

---

## Overview
[What does the build produce? What platforms are targeted?]

## When to Read This

### Trigger

- (fill from doc content)

### Read With

- `path/to/file.md` [[wiki-link]] — reason

## Prerequisites
[Tools and versions required to build.
Table of tool, minimum version, and purpose.]

## Build Commands
[Step-by-step commands for common build tasks:
- Development build
- Production/release build
- Clean build
- Platform-specific builds if applicable]

## Build Output
[Where build artifacts go. What each artifact contains.
Table of output path and its purpose.]

## Release Process
[Steps to create a release — version bump, tagging, publishing.
Only if applicable to the project.]

## Troubleshooting
[Common build failures and how to fix them.]

---

Related: [[linked-doc-1]] | [[linked-doc-2]]
```

## Guidelines

- Include exact commands — this doc is a reference people follow step-by-step
- **Troubleshooting** should cover real failures, not hypothetical ones
- Only create this doc if the build process is non-trivial

---

## Related

- [[INSTALL]] — How this template is used during implementation
- [[TEMPLATES/testing-doc]] — Testing docs often reference build process
- [[TEMPLATES/integration-doc]] — Build may depend on external tools
- [[TEMPLATES/index-doc]] — Index doc links to all build docs
