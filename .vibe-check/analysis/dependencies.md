# Dependencies Analysis

**Scanned:** 2026-02-07

## Summary

This project has zero npm dependencies. It uses only Node.js built-in modules. No lock file exists because there are no packages to lock. No vulnerability audit is possible or needed.

## Findings

### Lock File

**None:**
- No `package-lock.json`
- No `yarn.lock`
- No `pnpm-lock.yaml`
- Reason: No dependencies to lock

### Dependencies

**Zero runtime dependencies:**
- File: `package.json` has no `dependencies` field
- Uses only Node.js built-ins: `fs`, `path`, `os`, `readline`

**Zero dev dependencies:**
- File: `package.json` has no `devDependencies` field
- No test framework, no linter, no bundler

### Vulnerability Audit

**Not applicable:**
- `npm audit` would return empty (no dependencies)
- No CVEs possible with zero dependencies

### Node.js Built-in Modules Used

**bin/install.js:3-6:**
```javascript
const fs = require('fs');
const path = require('path');
const os = require('os');
const readline = require('readline');
```

**scripts/scan-secrets.js:14-15:**
```javascript
const fs = require('fs');
const path = require('path');
```

### Package Files Distributed

**From package.json `files` field:**
- `bin/`
- `commands/`
- `agents/`
- `references/`
- `templates/`
- `README.md`

## Evidence Files

Key files examined:
- `package.json` - No dependencies declared
- `bin/install.js:3-6` - Built-in module imports
- `scripts/scan-secrets.js:14-15` - Built-in module imports
