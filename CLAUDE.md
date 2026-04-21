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
├── .claude/
│   └── rules/
│       ├── security-rules.md
│       └── stable-rules.md
├── PHASES/
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
2. **Operational rules (editable)**: use this `CLAUDE.md` for workflow/navigation.
3. **Task-specific instructions**: follow user instructions in current session.

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

---

## Related

- [[INSTALL]]
- [[PRINCIPLES]]
- [[CHANGELOG]]
- [[decisions]]
