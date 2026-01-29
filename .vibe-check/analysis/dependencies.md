# Dependencies Analysis

**Scanned:** 2026-01-29

## Summary

This project has zero external dependencies. It uses only Node.js built-in modules. No package-lock.json exists because there are no dependencies to lock. No vulnerability audit is possible or needed.

## Findings

### Lock File

**No lock file present:**
- No `package-lock.json`
- No `yarn.lock`
- No `pnpm-lock.yaml`
- Not needed — project has no dependencies

### Dependencies

**File: `package.json`**

No `dependencies` section exists. The project uses only Node.js built-ins:

**bin/install.js imports:**
```javascript
const fs = require('fs');
const path = require('path');
const os = require('os');
const readline = require('readline');
```

**scripts/scan-secrets.js imports:**
```javascript
const fs = require('fs');
const path = require('path');
```

### DevDependencies

**None:**
- No `devDependencies` section in package.json
- No test framework
- No linter
- No build tools

### Vulnerability Audit

**Not applicable:**
- `npm audit` would report "found 0 vulnerabilities"
- No third-party code to audit

### Dependency Counts

- Production dependencies: 0
- Development dependencies: 0
- Total: 0

### Version Constraints

**Node.js engine requirement:**
- File: `package.json:34-36`
```json
"engines": {
  "node": ">=16.0.0"
}
```

## Evidence Files

Key files examined:
- `package.json` — No dependencies defined
- `bin\install.js` — Uses only Node.js built-ins
- `scripts\scan-secrets.js` — Uses only Node.js built-ins
