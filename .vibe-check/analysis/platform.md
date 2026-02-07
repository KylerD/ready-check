# Platform Analysis

**Scanned:** 2026-02-07

## Summary

This is an npm package requiring Node.js >= 16. It runs locally on any platform with Node.js installed. No hosting platform needed - distributed via npm registry.

## Findings

### Framework

**None:**
- Pure Node.js CLI application
- No web framework
- No frontend framework

### Compatible Platforms

**npm registry (current):**
- File: `package.json`
- Installed via: `npx vibe-check-cc`
- No hosting required

**Local execution requirements:**
- Node.js >= 16.0.0 (per `engines` field)
- Works on: Windows, macOS, Linux
- Requires: Claude Code installed

### Hosting Config Files

**None:**
- No `vercel.json`
- No `netlify.toml`
- No `render.yaml`
- No platform-specific configuration

### Complexity Signals

**Very low complexity:**
- Zero dependencies
- Two JavaScript files total
- No build step
- No deployment pipeline visible in repo

### Cost Signals

**Zero runtime cost:**
- No server hosting
- No database
- No API calls
- User runs locally at no cost

### Managed Services

**None:**
- No Auth0, Clerk (auth)
- No Supabase, Firebase (BaaS)
- No Neon, PlanetScale (database)
- No Upstash (cache)
- No Resend, SendGrid (email)

### File Uploads

**None:**
- No multer, formidable, busboy
- No file upload handling

### Image Processing

**None:**
- No sharp, jimp, imagemin
- No image manipulation

### Pagination

**None:**
- No API responses to paginate

## Evidence Files

Key files examined:
- `package.json` - npm distribution config
- `bin/install.js` - Local file operations only
