# Integrations Analysis

**Scanned:** 2026-01-29

## Summary

This project integrates with Claude Code's plugin system. It does not make external API calls or connect to third-party services. All operations are local filesystem-based.

## Findings

### External Services

**None:**
- No external API calls
- No third-party service integrations
- No network requests in source code

### Claude Code Integration

**Hook System:**
- File: `hooks\hooks.json:4-16`
- Integrates with Claude Code's PreToolUse hook system
- Intercepts Write and Edit tool calls
- Runs secret scanner before allowing writes to .vibe-check/

**Command System:**
- Installs slash commands to `~/.claude/commands/vibe-check/`
- Commands: check, fix, refresh, discuss, help, map-codebase

**Agent System:**
- Installs agent definitions to `~/.claude/agents/`
- Agents: vibe-mapper, vibe-assessor, vibe-fixer

### SDK/Client Libraries

**None:**
- No external SDKs
- No API clients
- No database clients

### Webhook Handlers

**None:**
- No webhook endpoints
- Not a web service

### API Endpoints Called

**None:**
- No `fetch`, `axios`, or `http` calls
- All operations are local

### GitHub Integration

**Repository metadata only:**
- File: `package.json:23-25`
```json
"repository": {
  "type": "git",
  "url": "https://github.com/kylerd/vibe-check.git"
}
```
- No runtime GitHub API calls

## Evidence Files

Key files examined:
- `hooks\hooks.json` — Claude Code hook configuration
- `bin\install.js` — Local filesystem operations only
- `package.json` — Repository URL for npm metadata
