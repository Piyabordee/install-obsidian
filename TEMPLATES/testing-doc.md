# Template: Testing Doc

> Use for: testing strategy, approach, and conventions
> Location: `docs/testing/<topic>.md`

---

## Structure

```markdown
# [Testing Topic]

> One-line description of the testing approach or strategy.

---

## Overview
[What is the testing strategy? What matters most in this project's tests?]

## Context Snapshot
[Test boundaries, confidence goals, and what this topic does not cover.]

## When to Read This

### Trigger

- (fill from doc content)

### Read With

- `path/to/file.md` [[wiki-link]] — reason

## Test Structure
[How tests are organized — directories, naming conventions, file patterns.
Table of test directories and what they cover.]

## Running Tests
[Commands to run tests — unit, integration, full suite.
Include any special flags or environment setup needed.]

## Writing New Tests
[Conventions to follow when adding tests:
- Where to put new test files
- Naming conventions
- Required setup/teardown patterns
- Mock/stub strategy if applicable]

## Coverage Expectations
[What areas must have tests? What's acceptable to skip?]

## Decision Trace
(Optional — use for durable test policy/tradeoff decisions.)

- Decision: [what was chosen]
- Why: [reason/tradeoff]
- Impact: [what contributors should do differently]

---

Related: [[linked-doc-1]] | [[linked-doc-2]]
```

## Guidelines

- Focus on project-specific conventions, not general testing theory
- **Writing New Tests** is the most valuable section — it guides contributors
- Only create this doc if testing approach is non-trivial or non-obvious
- Keep policy clear and short; avoid turning this doc into generic QA theory

---

## Related

- [[INSTALL]] — How this template is used during implementation
- [[TEMPLATES/build-doc]] — Build and testing docs are often paired
- [[TEMPLATES/integration-doc]] — Integration testing may reference this
- [[TEMPLATES/index-doc]] — Index doc links to all testing docs
