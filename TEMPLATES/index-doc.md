# Template: Index Doc (_index.md)

> Use for: docs/_index.md — the documentation navigation hub
> Location: `docs/_index.md`

---

## Structure

```markdown
# [Project Name] — Documentation Index

> Navigation hub for all project documentation.
> Start here to find what you need.

---

## Quick Links

- [[CLAUDE]] — Project hub (AI reads this first)
- [[README]] — User-facing introduction

---

## Project

| Doc | Description |
|-----|-------------|
| [[docs/project/<name>]] | [one-line description] |

## Architecture

| Doc | Description |
|-----|-------------|
| [[docs/architecture/<name>]] | [one-line description] |

## Features

| Doc | Description |
|-----|-------------|
| [[docs/features/<name>]] | [one-line description] |

## Integrations

| Doc | Description |
|-----|-------------|
| [[docs/integrations/<name>]] | [one-line description] |

## Build & Testing

| Doc | Description |
|-----|-------------|
| [[docs/build/<name>]] | [one-line description] |
| [[docs/testing/<name>]] | [one-line description] |

## Reference

| Doc | Description |
|-----|-------------|
| [[docs/reference/<name>]] | [one-line description] |

---

## External Resources

- [Link to external docs, APIs, etc. if applicable]
```

## Guidelines

- **Include only categories that have docs** — remove empty sections entirely
- **Every entry must link to a real file** — no placeholders
- **Organize by category** matching the folder structure under `docs/`
- **Description should answer** "what will I learn by reading this?"
- Keep this file compact — it's a map, not an encyclopedia
