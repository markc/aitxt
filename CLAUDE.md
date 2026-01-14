# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Purpose

This repository documents the **ai.txt** specification—a proposed web standard for AI-readable website summaries. Similar to `robots.txt` for crawlers or `security.txt` for security contacts, `ai.txt` provides a single plain text file at a website's root containing structured information for AI assistants.

## Repository Structure

- `README.md` - Main specification documentation and examples
- `SITES.md` - Community-maintained directory of sites implementing ai.txt
- `CONTRIBUTING.md` - Guidelines for contributions
- `LICENSE` - CC0 public domain dedication

## Key Concepts

**ai.txt format:**
- Plain text with markdown headings for structure
- Located at website root: `https://example.com/ai.txt`
- No HTML, JavaScript, or special parsing required
- Contains: contact info, services, pricing, hours, policies

**This is a documentation-only repository** - no build system, tests, or application code. Changes involve editing markdown files.

## Maintaining SITES.md

When reviewing PRs that add sites to the directory:
1. Verify the site has a valid `/ai.txt` accessible via HTTPS
2. Ensure alphabetical ordering within categories
3. Check the ai.txt content follows the plain text + markdown headings format
