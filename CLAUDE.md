# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Purpose

This repository documents the **ai.txt** specification—a web standard for AI-readable website summaries. Unlike `robots.txt` which only lives at the root, `ai.txt` can be placed in any folder with cascading discovery.

## Repository Structure

```
/
├── index.html    # Specification (HTML)
├── ai.txt        # Directory of known sites (dogfooding the spec)
├── README.md     # Quick reference
├── CNAME         # aitxt.ing domain
└── LICENSE       # CC0 public domain
```

## Key Concepts

**Cascading:** ai.txt in any folder, discovered by walking up the tree
**Linking:** `@domain.com/path#section` syntax for references
**Hierarchy:** `Parent:` metadata links to broader context
**Metadata:** `ai.txt:`, `Updated:`, `Scope:`, `TTL:`
**Negative assertions:** `## We Do Not Offer` prevents hallucination
**AI Guidelines:** `## AI Guidelines` instructs AI behavior

## Maintaining the Directory

The site directory lives in `/ai.txt` using `@domain` links. When reviewing PRs:
1. Verify the site has a valid ai.txt accessible via HTTPS
2. Add as `@domain.com` under `## Known Sites`
3. Check the ai.txt follows the spec format
