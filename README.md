# Install Obsidian Brain

> Portable Obsidian documentation system installer for AI agents.
> Drop this folder into any repo. AI reads the instructions, analyzes your codebase, and builds a documentation brain automatically.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-Unlicense-green)

---

## What This Does

This is **not** a traditional installer. It is a set of Markdown instructions that AI agents (Claude Code, Copilot, Cursor, etc.) read to:

1. **Analyze** your repo structure
2. **Design** a documentation tree tailored to your codebase
3. **Create** interconnected Markdown docs optimized for Obsidian graph view

The result: your repo gains a living knowledge base that both humans and AI can navigate.

## How to Use

### Option A: With Claude Code

```bash
# 1. Copy this folder into your repo root
# macOS / Linux:
cp -r install-obsidian/ /path/to/your-repo/

# Windows (PowerShell):
Copy-Item -Recurse install-obsidian\ C:\path\to\your-repo\

# 2. Open Claude Code in your repo
cd /path/to/your-repo
claude

# 3. Tell Claude:
> Read install-obsidian/INSTALL.md and follow the instructions
```

### Option B: With any AI agent

Open `INSTALL.md` and follow the phases. Feed each phase file to your AI agent sequentially.

## What You Get

After installation, your repo will have:

```
your-repo/
├── CLAUDE.md              # Project hub (AI reads this first)
├── docs/
│   ├── _index.md          # Documentation navigation hub
│   ├── project/           # Project-level knowledge
│   ├── architecture/      # Structure and subsystem docs
│   ├── features/          # Feature workflow docs
│   ├── integrations/      # External dependency docs (if applicable)
│   ├── build/             # Build/packaging docs (if applicable)
│   ├── testing/           # Testing knowledge
│   └── reference/         # Stable reference docs
```

## Philosophy

- **Flex, not static** — AI analyzes YOUR repo, creates docs that match YOUR structure
- **Hub-and-spoke** — CLAUDE.md is the front door, docs/ are the rooms
- **Graph-friendly** — Wiki links between docs make Obsidian graph useful
- **Minimal** — Only creates docs where real knowledge exists, no empty placeholders

## Folder Contents

| File | Purpose |
|------|---------|
| [[INSTALL]] | Step-by-step instructions for AI agents |
| [[PRINCIPLES]] | Design principles and decision framework |
| [[CONTRIBUTING]] | Contributor guidelines |
| [[CHANGELOG]] | Version tracking |
| `TEMPLATES/` | Document structure templates (not content) |
| `PHASES/` | Sequential execution phases |

## After Installation

1. Open your repo in Obsidian
2. Enable "Detect all file types" in Obsidian settings
3. Ensure "Use [[Wikilinks]]" is enabled in Settings > Files & Links
4. The graph view should now show meaningful connections between docs
5. When you add new features, AI will follow the Doc Workflow in CLAUDE.md to create new docs automatically

## Requirements

- An AI agent capable of reading files and exploring a codebase
- The target repo must have identifiable structure (any language, any framework)
- Obsidian (optional, for graph view)

---

## License

Public domain. Use freely in any project.
