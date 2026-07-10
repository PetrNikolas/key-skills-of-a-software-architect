# Project context

This file provides full project context for AI assistants and contributors. It serves as the single source of truth for the purpose, structure, and conventions of this repository.

## Project purpose

The repository holds a **curated flat list of key skills and principles for software architects**. The goal is to provide a practical handbook for architects, not to write code. All content is in English.

## Contents

All content lives in a single file, `README.md`, under the heading `# Key Knowledge of a Software Architect`. It currently contains **29 entries**, each in the format:

```
- 💚 <principle/maxim> - <short explanation>.
```

Entries are in insertion order, not sorted alphabetically or by theme. There are no categories or subsections.

## Repository structure

```
.
├── README.md              # Main content — flat list of 29 principles
├── AGENTS.md              # Instructions for general AI agents
├── CLAUDE.md              # Instructions for Claude
├── GEMINI.md              # Instructions for Gemini
├── PROJECT_CONTEXT.md     # This file — full project context
├── LICENSE                # MIT License, © 2023 Petr Nikolas Prokop
├── .gitignore             # IntelliJ template (.idea, *.iml, out, gen)
├── .claude/settings.json  # Configuration for Claude Code (placeholder)
├── .codex/config.toml     # Configuration for Codex CLI (placeholder)
├── .gemini/settings.json  # Configuration for Gemini (placeholder)
└── .idea/                 # IntelliJ project files (gitignored)
```

## Contribution conventions

When working on this project, follow these rules:

- **Language:** English only.
- **Structure:** flat list with no categories, subsections, or introductory text.
- **Entry format:** exactly `- 💚 <principle> - <explanation>.` (hyphen, space, green heart 💚, space, text).
- **One entry = one principle** plus a short explanation separated by ` - `.
- **No code or rich formatting:** no bold, italics, code spans, links, or images.
- **Clarity and brevity:** the goal is a practical handbook, not an academic text.
- **New entries** are added as a new line at the end of the list in `README.md`, with no blank line between adjacent entries.

## Contribution checklist

Before appending a new principle to `README.md`, verify the draft against this checklist:

- [ ] **Language:** English. No Czech unless quoting.
- [ ] **Exact format:** line starts with `- 💚 ` (hyphen, space, green heart, space) — nothing else.
- [ ] **Single principle:** one core idea per entry, structured as `<principle> - <short explanation>.`
- [ ] **Separator:** a ` - ` (space-hyphen-space) between the maxim and the elaboration.
- [ ] **Termination:** entry ends with a period `.`.
- [ ] **No rich formatting:** no bold, italics, code spans, backticks, links, images, or nested lists.
- [ ] **No blank line** between the new entry and the existing ones.
- [ ] **Duplication check:** scan all existing entries in `README.md` and confirm the new principle does not overlap with an existing one. Common recurring themes to watch: trade-offs (quality vs cost vs time), complexity (essential vs accidental), technical debt, performance, people over technology, requirements over personal preference. If the idea already exists, refine the angle or discard.
- [ ] **Clarity & brevity:** a practitioner should grasp it in one read.

## Technical context

- **Repository type:** documentation-only — no build system, no dependencies, no code.
- **License:** MIT, Copyright © 2023 Petr Nikolas Prokop.
- **Author:** Petr Nikolas Prokop (`petr.prokop@systems4.cz`).
- **Remote:** `https://github.com/PetrNikolas/key-skills-of-a-software-architect.git`

## Git context

- **Main branch:** `main`
- **Local branches:** `main`, `feature/dhaka`
- **Workflow:** direct commits to `main` or via feature branches.

## References

- [`README.md`](README.md) — main content.
- [`AGENTS.md`](AGENTS.md) / [`CLAUDE.md`](CLAUDE.md) / [`GEMINI.md`](GEMINI.md) — instructions for individual AI tools.
