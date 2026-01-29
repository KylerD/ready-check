# Data Analysis

**Scanned:** 2026-01-29

## Summary

This project does not use a database. It operates entirely on the local filesystem, reading and writing markdown and JSON files. The generated assessment output is stored in `.vibe-check/` in the target project.

## Findings

### Database

**None:**
- No database client libraries
- No database connection code
- No schema files
- No migrations

### Data Storage

**Local filesystem only:**
- Reads from user's Claude Code config directory
- Writes assessment output to `.vibe-check/` in target project

**Output structure (written by agents, not this tool directly):**
```
.vibe-check/
├── summary.md
├── report.md
├── action-plan.md
├── metadata.json
├── analysis/
│   └── *.md
└── checklist/
    ├── index.md
    └── item-*.md
```

### Configuration Data

**File: `scripts\secret-patterns.json`**
- Static JSON file with 50+ regex patterns
- Read at runtime by secret scanner

**File: `hooks\hooks.json`**
- Hook configuration
- Installed to user's Claude config

### Backup Configuration

**Not applicable:**
- No persistent data store
- Generated output can be regenerated
- Users may git-commit `.vibe-check/` if desired

### Connection Handling

**Not applicable:**
- No database connections
- No connection pooling
- No retry logic needed

### Data Persistence

**File-based:**
- Assessment results written as markdown/JSON files
- Metadata stored in `metadata.json` for machine-readable access
- Files can be committed to git for tracking over time

## Evidence Files

Key files examined:
- `package.json` — No database dependencies
- `scripts\secret-patterns.json` — Static configuration data
- `templates\` — Output file templates
