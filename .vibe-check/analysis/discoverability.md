# Discoverability Analysis

**Scanned:** 2026-02-07

## Summary

No SEO or discoverability patterns exist. This is a CLI tool with no web presence - no HTML pages, no meta tags, no sitemap. Discoverability comes from npm registry and GitHub repository.

## Findings

### Meta Tags

**None:**
- No HTML files in project
- No `<title>` tags
- No `<meta>` description tags

### OpenGraph Tags

**None:**
- No `og:title`, `og:description`, `og:image`
- Not applicable for CLI package

### Twitter Card Tags

**None:**
- No `twitter:card`, `twitter:title`, `twitter:image`
- Not applicable for CLI package

### Sitemap

**None:**
- No `sitemap.xml`
- No sitemap generation
- Not applicable for CLI package

### robots.txt

**None:**
- No `robots.txt`
- Not applicable for CLI package

### Canonical URLs

**None:**
- No canonical URL configuration
- Not applicable for CLI package

### Discoverability Channels

**npm registry:**
- File: `package.json:8-15`
- Keywords: `claude`, `claude-code`, `production`, `readiness`, `security`, `infrastructure`, `devops`, `assessment`
- Description: "Production readiness assessment for Claude Code - identify gaps across security, infrastructure, and reliability"

**GitHub:**
- Repository: `https://github.com/kylerd/vibe-check.git`
- README.md exists at project root

## Evidence Files

Key files examined:
- `package.json` - npm discoverability metadata
- `README.md` - GitHub documentation
