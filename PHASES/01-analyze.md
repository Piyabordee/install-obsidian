# Phase 1: ANALYZE

> Explore the repository. Discover its real structure.
> Do NOT create any files yet. Only read and report.

---

## Objective

Build a complete mental model of the repository by analyzing its actual structure, not assumptions.

## Steps

### 1.1 Surface Structure

```
- List all top-level files and folders
- Identify entry points for the language/framework used:
  - Python: main.py, app.py, manage.py, __main__.py
  - JavaScript/TypeScript: index.js, index.ts, App.tsx, main.ts
  - Go: main.go, cmd/
  - Rust: main.rs, lib.rs
  - Java/Kotlin: Application.java, Main.java, *Application.kt
  - C/C++: main.c, main.cpp
  - Ruby: config.ru, main.rb
  - PHP: index.php, artisan, public/index.php
  - C# / .NET: Program.cs, Startup.cs, *.csproj
  - Swift: AppDelegate.swift, @main, Package.swift
  - Dart/Flutter: lib/main.dart, pubspec.yaml
  - Elixir: mix.exs, lib/**/application.ex
  - For other languages: look for the main entry pattern of the framework
- Identify config files (package.json, pyproject.toml, Cargo.toml, etc.)
- Identify documentation already present (README, CHANGELOG, CONTRIBUTING, etc.)
- Identify build/packaging files (Dockerfile, Makefile, .spec, .iss, etc.)
```

### 1.2 Deep Structure

```
- Explore each major source directory (src/, lib/, app/, etc.)
- List all subdirectories and their apparent purpose
- Identify the deepest meaningful nesting level
- Note any monolithic files (>500 lines) that might indicate subsystems
```

### 1.3 Entry Points and Flow

```
- Trace from entry point to main initialization
- Identify what loads first, what depends on what
- Map the dependency direction (what imports what)
```

### 1.4 Key Patterns

```
- What framework is used? (Qt, React, Express, etc.)
- What architectural patterns exist? (MVC, mixins, plugins, etc.)
- How is configuration managed?
- How is testing done? (or not done?)
- How is building/packaging done? (or not done?)
```

### 1.5 External Dependencies

```
- What external tools/binaries are required?
- What package manager is used?
- What are the critical dependencies (not all, just the ones that shape the architecture)?
```

### 1.6 Existing Documentation

```
- What docs already exist?
- What docs have valuable information that should be preserved?
- What docs are outdated or empty?
- Is there an existing CLAUDE.md or AGENTS.md?
```

---

## Output

Present your findings as a structured analysis:

```markdown
## Analysis: [Repo Name]

### Type & Stack
[What kind of project? What technologies?]

### Structure Summary
[Key directories and their purposes]

### Entry Points
[How does the app start?]

### Architectural Patterns
[What patterns does the codebase use?]

### Key Subsystems
[List identifiable subsystems with their locations]

### External Dependencies
[Critical external tools/libraries]

### Existing Docs
[What documentation exists and its quality]

### Documentation Gaps
[What's missing? What would help onboarding?]

### Recommended Doc Categories
[Which categories from PRINCIPLES.md are justified?]
```

Wait for the human to acknowledge your analysis before proceeding to [[PHASES/02-design]].

---

## Related

- [[INSTALL]] — Main instruction flow
- [[PRINCIPLES]] — Design philosophy guiding your analysis
- [[PHASES/02-design]] — Next phase: design the doc tree
- [[TEMPLATES/project-doc]] — Template for project-level docs
- [[TEMPLATES/architecture-doc]] — Template for architecture docs
