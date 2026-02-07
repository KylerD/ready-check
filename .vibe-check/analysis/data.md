# Data Analysis

**Scanned:** 2026-02-07

## Summary

No database usage in this project. Data is stored as local markdown and JSON files. The tool reads/writes to user's filesystem in `.claude/` directories. No migrations, backups, or connection strings.

## Findings

### Database

**None:**
- No Prisma, Mongoose, Sequelize, TypeORM, or Drizzle
- No PostgreSQL, MySQL, SQLite, or MongoDB clients
- No Redis or caching layer

### Schema/Migrations

**None:**
- No `prisma/schema.prisma`
- No `migrations/` directory
- No database schema files

### Data Storage

**Local filesystem (JSON/Markdown):**

**JSON files:**
- `scripts/secret-patterns.json` - Secret detection patterns (read-only)
- `~/.claude/settings.json` - Claude settings (read/write)

**Markdown files:**
- Input: Agent configs, templates, commands (read-only)
- Output: `.vibe-check/` directory with analysis results

### Connection Strings

**None:**
- No `DATABASE_URL`
- No `MONGODB_URI`
- No `REDIS_URL`

### Backup Configuration

**None:**
- No backup scripts
- No dump/restore functionality
- Data is user-managed local files

### Data Flow

1. User runs `npx vibe-check-cc`
2. Tool copies markdown files to `~/.claude/` or `./.claude/`
3. Claude Code reads these files when user runs `/vibe-check:check`
4. Assessment results written to `.vibe-check/` in project directory

## Evidence Files

Key files examined:
- `package.json` - No database dependencies
- `bin/install.js` - Local file operations only
- `scripts/secret-patterns.json` - Static JSON data
