# Stack Analysis

**Scanned:** 2026-01-29

## Summary

This is a Claude Code plugin/skill package called "vibe-check-cc" — a production readiness assessment tool. It is a pure JavaScript/Node.js project with no framework dependencies, designed to be installed via npx and integrate with Claude Code's command system.

## Findings

### Primary Language

**JavaScript (Node.js):**
- File: `package.json:35`
- Runtime requirement: Node.js >= 16.0.0
- No TypeScript configuration found
- Two JavaScript files: `bin/install.js` and `scripts/scan-secrets.js`

### Project Type

**Claude Code Plugin/Skill:**
- File: `package.json:9-11`
- Binary entry point: `vibe-check-cc` pointing to `./bin/install.js`
- Distributed via npm with `npx vibe-check-cc` invocation
- Contains markdown-based commands, agents, templates, and references

### Package Structure

**File: `package.json:26-33`**

Published files include:
- `bin/` — Installation scripts
- `commands/` — Slash command definitions (6 commands)
- `agents/` — Agent definitions (3 agents: mapper, assessor, fixer)
- `references/` — Reference documentation (5 files)
- `templates/` — Output templates (6 files)

### Dependencies

**No runtime dependencies:**
- File: `package.json`
- No `dependencies` or `devDependencies` sections
- Uses only Node.js built-in modules: `fs`, `path`, `os`, `readline`, `child_process`

### Configuration Files

**Claude settings:**
- File: `.claude\settings.local.json`
- Contains permission settings for development testing

**Hooks configuration:**
- File: `hooks\hooks.json`
- Defines PreToolUse hook for secret scanning

## Evidence Files

Key files examined:
- `package.json` — Package manifest with metadata and structure
- `bin\install.js` — Main entry point (447 lines)
- `scripts\scan-secrets.js` — Secret scanning hook (129 lines)
- `.gitignore` — Git ignore patterns
