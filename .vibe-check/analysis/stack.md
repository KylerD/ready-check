# Stack Analysis

**Scanned:** 2026-02-07

## Summary

This is a Node.js CLI tool (npm package) that provides production readiness assessment for Claude Code. It consists of markdown configuration files, JavaScript CLI scripts, and templates. No frontend framework, no server runtime, no database.

## Findings

### Primary Language

**JavaScript (Node.js):**
- File: `package.json:1-28`
- Runtime: Node.js >= 16.0.0 (per `engines` field)
- Type: CLI tool distributed via npm

### Package Information

**Package manifest:**
- File: `package.json`
- Name: `vibe-check-cc`
- Version: `1.1.0`
- License: MIT
- Entry point: `./bin/install.js`

### Framework/Runtime

**None - pure Node.js CLI:**
- No web framework (no Express, Fastify, Koa, etc.)
- No frontend framework (no React, Vue, etc.)
- No build tools (no webpack, vite, etc.)
- Uses only Node.js built-in modules: `fs`, `path`, `os`, `readline`

### Dependencies

**Zero runtime dependencies:**
- File: `package.json` has no `dependencies` block
- No `devDependencies` block either
- Uses only Node.js built-in modules

### Source Files

**JavaScript files (2):**
- `bin/install.js` - CLI entry point (450 lines)
- `scripts/scan-secrets.js` - PreToolUse hook for secret scanning (129 lines)

**Configuration files (markdown):**
- `agents/` - Agent configuration files (3 files)
- `commands/` - Slash command definitions (6 files)
- `references/` - Reference documentation (5 files)
- `templates/` - Output templates (6 files)

## Evidence Files

Key files examined:
- `package.json` - Package manifest
- `bin/install.js` - CLI entry point
- `scripts/scan-secrets.js` - Secret scanner hook
- `.gitignore` - Git ignore rules
