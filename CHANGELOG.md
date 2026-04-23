# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- TEMPLATES/migration-map.md — standard section-by-section migration map template for AGENTS.md and legacy docs
- INSTALL.md definition of done and mandatory post-install validation checklist
- CLAUDE.md — repository operational hub with directory tree, DoD, and session closeout
- .claude/rules/security-rules.md — stable security constraints separated from CLAUDE.md
- .claude/rules/stable-rules.md — stable project constraints separated from CLAUDE.md
- decisions.md — persistent design decision log for context resets
- PHASES/05-optimize-links.md — final phase for link-quality optimization in `CLAUDE.md` + `docs/`
- Hybrid strategy guidance across docs: preserve installer core and apply llm-wiki-inspired practices as a complementary layer
- Hybrid practicality gates and drift-guard checkpoints in installation workflow phases
- Template-level support for context/rationale capture and lightweight decision trace

### Changed
- INSTALL.md now requires installation mode selection (`strict` default or `adaptive`)
- README.md now documents strict vs adaptive output expectations
- PHASES/02-design.md now requires full AGENTS.md section mapping before Phase 3
- PHASES/03-implement.md now includes a 100% AGENTS.md migration coverage gate
- PHASES/04-cleanup.md now requires section-level migration evidence before deleting AGENTS.md
- TEMPLATES/hub-claude-md.md now requires stable rules in `./.claude/rules/`, directory tree, DoD, and session closeout
- INSTALL.md and PHASES/03-implement.md now include stable rules separation, decisions.md, and verification/closeout expectations
- INSTALL.md and README.md now include a final Optimize Links phase for duplicate/valueless link cleanup
- README.md now explicitly defines the hybrid model (`install-obsidian core` + `llm-wiki-inspired` layer)
- PRINCIPLES.md now adds hybrid doctrine and context/rationale-first anti-drift principles
- PHASES/01-05 now include systematic + flexible checkpoints and stronger anti-duplication guidance

## [1.0.0] - 2026-04-18

### Added
- Initial release of install-obsidian instruction set
- INSTALL.md — step-by-step AI agent instructions
- PRINCIPLES.md — documentation design philosophy
- PHASES/ — four-phase execution workflow (Analyze, Design, Implement, Cleanup)
- TEMPLATES/ — document structure templates (architecture, feature, project, reference, index, hub-claude-md)
- README.md — project overview and usage guide
- LICENSE — Unlicense (public domain)
- .gitignore — OS and editor file exclusions
- CHANGELOG.md — version tracking
- CONTRIBUTING.md — contributor guidelines
