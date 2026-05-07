# install-obsidian — Project Hub

> Operational hub for AI agents working in this repository.
> Stable/non-negotiable rules live in `./.claude/rules/`.

---

## Read First

- [[README]] — project overview
- [[INSTALL]] — execution flow for AI agents
- [[PRINCIPLES]] — design rules

---

## Directory Tree (Authoritative)

```text
install-obsidian/
├── .claude-plugin/
│   ├── marketplace.json
│   └── plugin.json
├── .claude/
│   └── rules/
│       ├── coding-behavior-rules.md
│       ├── security-rules.md
│       └── stable-rules.md
├── agents/
│   └── install-obsidian-agent.md
├── commands/
│   └── install.md
├── PHASES/
├── skills/
│   └── install-obsidian-skill/
│       ├── README.md
│       └── SKILL.md
├── TEMPLATES/
├── CHANGELOG.md
├── CONTRIBUTING.md
├── INSTALL.md
├── PRINCIPLES.md
├── README.md
└── decisions.md
```

---

## Rule Layers

1. **Stable rules (immutable)**: read all files in `./.claude/rules/` first.
   - [[.claude/rules/stable-rules]] — project-wide stable rules
   - [[.claude/rules/security-rules]] — security constraints
   - [[.claude/rules/coding-behavior-rules]] — Karpathy-inspired coding behavior (think before coding, simplicity, surgical changes, goal-driven execution)
2. **Operational rules (editable)**: use this `CLAUDE.md` for workflow/navigation.
3. **Task-specific instructions**: follow user instructions in current session.
4. **Hybrid strategy**: preserve installer core requirements; apply llm-wiki-inspired practices as a complementary layer.

---

## Definition of Done (Session)

- [ ] Requested change is implemented with minimal scope.
- [ ] Related docs/instructions are updated when behavior changed.
- [ ] Verification commands were run for affected stack:
  - TypeScript: `tsc --noEmit`
  - Otherwise: run equivalent existing validation commands in repo
- [ ] Commit is scoped to one issue/change set.
- [ ] `decisions.md` updated when design/strategy decisions were made.
- [ ] `CLAUDE.md` reviewed and updated to reflect current project state.

---

## Session Closeout

At the end of every session, run a final pass:

1. Update `CLAUDE.md` to match current project state
2. Update `decisions.md` for any new lasting decisions
3. Confirm links and paths still point to existing files

## Refresh Update Mode

- `/install-obsidian:update <range>` means delta-only refresh for the specified commit window.
- Keep refresh edits scoped to affected docs/hubs; do not silently expand into a full reinstall flow.

---

## Related

- [[INSTALL]]
- [[PRINCIPLES]]
- [[CHANGELOG]]
- [[decisions]]
