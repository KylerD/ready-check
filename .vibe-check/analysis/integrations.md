# Integrations Analysis

**Scanned:** 2026-02-07

## Summary

No external service integrations exist. This is a local-only CLI tool that reads and writes files on the local filesystem. It makes no network requests and has no API dependencies.

## Findings

### External Services

**None:**
- No Stripe, Twilio, SendGrid, or payment/messaging SDKs
- No AWS, GCP, or cloud provider SDKs
- No Firebase, Supabase, or BaaS SDKs
- No database clients

### API Calls

**None:**
- No `fetch`, `axios`, `http`, or `request` usage
- No network requests of any kind
- Tool operates entirely on local filesystem

### Webhook Handlers

**None:**
- No webhook endpoints
- Not a server application

### External URLs

**None in code:**
- No hardcoded API endpoints
- No external service URLs

### File Operations

**Local filesystem only:**
- File: `bin/install.js`
- Operations: `fs.readFileSync`, `fs.writeFileSync`, `fs.existsSync`, `fs.mkdirSync`, `fs.rmSync`, `fs.copyFileSync`, `fs.unlinkSync`, `fs.readdirSync`
- Scope: `~/.claude` (global) or `./.claude` (local) directories only

### GitHub Integration

**Repository URL only:**
- File: `package.json:18-21`
- URL: `https://github.com/kylerd/vibe-check.git`
- Purpose: npm package metadata, not runtime integration

## Evidence Files

Key files examined:
- `package.json` - No integration dependencies
- `bin/install.js` - Local filesystem operations only
- `scripts/scan-secrets.js` - stdin/stdout only
