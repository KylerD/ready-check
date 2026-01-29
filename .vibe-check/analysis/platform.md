# Platform Analysis

**Scanned:** 2026-01-29

## Summary

This project is distributed via npm and runs locally via Node.js. It is not a hosted application and does not require platform deployment. It integrates with Claude Code as a plugin/skill.

## Findings

### Framework Identified

**Pure Node.js CLI application:**
- No web framework
- No frontend framework
- Built-in modules only: fs, path, os, readline

### Compatible Platforms

**npm ecosystem:**
- Distributed via npm registry
- Installed via `npx vibe-check-cc`
- Requires Node.js >= 16.0.0

**Claude Code integration:**
- Requires Claude Code CLI to be installed
- Installs to `~/.claude/` (global) or `./.claude/` (local)

### Hosting Config Files

**None found:**
- No vercel.json
- No netlify.toml
- No render.yaml
- No fly.toml
- No railway.json
- No Procfile
- No app.yaml

Not applicable — this is a local CLI tool, not a hosted service.

### Complexity Signals

**Kubernetes:**
- No k8s/ directory
- No kubernetes/ directory
- No helm/ directory
- No deployment manifests

**Microservices:**
- Single-purpose tool
- No docker-compose.yml
- No multi-service architecture

**Complexity assessment: Low**
- Simple file-based installer
- Hook script for secret scanning
- Markdown templates and documentation

### Cost Signals

**Not applicable:**
- No cloud resources
- No serverless functions
- No database costs
- No bandwidth costs
- Runs locally on user's machine

### File Handling

**Local filesystem only:**
- Reads package files from npm cache
- Writes to Claude config directories
- No uploads to external services

### Managed Services in Use

**None:**
- No auth0, clerk, supabase, firebase
- No neon, planetscale, upstash
- No resend, sendgrid
- All operations are local

### Distribution

**npm package:**
- File: `package.json`
- Name: `vibe-check-cc`
- Version: 1.0.0
- Binary: `vibe-check-cc`

## Evidence Files

Key files examined:
- `package.json` — npm configuration
- `bin\install.js` — Installation logic
- `.gitignore` — No platform-specific ignores
