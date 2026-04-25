# flotilla-slim-agents

Six slim agents — `architect`, `engineer`, `planner`, `testing-qa`,
`release-engineer`, `orchestrator` — covering the AIDLC roles for any
project. Designed to be the minimal viable agent roster.

## Install via Flotilla

```bash
flotilla install slim-agents
```

This is a `kind: agent-pack` plugin — no Python package, just markdown.
Flotilla clones this repo into the project's `.flotilla/cache/` and
copies/symlinks `plugin/agents/*.md` into `.claude/agents/`.

## What's here

```
plugin/
└── agents/
    ├── architect.md
    ├── engineer.md
    ├── orchestrator.md
    ├── planner.md
    ├── release-engineer.md
    └── testing-qa.md
```

## Customising

The agents are intentionally short — clone the repo, edit the prompts,
and either:

- Use Flotilla with `--source <local-path>` to install from your fork
- Or, push your fork to GitHub and point Flotilla at it via `source:` in
  `.flotilla/manifest.yaml`.

## Provenance

These were originally bundled with the [Flotilla starter kit](https://github.com/ocgully/flotilla)
when Flotilla was a clone-and-go scaffold. After Flotilla became a
plugin marketplace, they were extracted to their own repo so they could
be versioned, forked, and replaced like any other plugin.
