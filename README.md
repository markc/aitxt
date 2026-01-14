# ai.txt

A universal standard for AI-readable context about any resource.

Just as `robots.txt` tells search engines how to behave, `ai.txt` tells AI assistants what something is about.

## Learn More

**For humans:** https://aitxt.ing — explains why ai.txt matters and how it works

**For the specification:** https://aitxt.ing/ai.txt — the complete spec written in ai.txt format

**For AI developers:** Read `/ai.txt` to understand discovery, parsing, and usage guidelines

## Quick Concept

Place `ai.txt` at any path to describe it:

```
# Your Project

Brief description of what this is.

## What We Offer

Features and capabilities...

## What We Don't Offer

Explicit limitations to prevent AI hallucination...
```

Optional metadata at the top (YAML frontmatter):

```
---
updated: 2026-01-14
scope: /products/
parent: https://example.com/ai.txt
---
```

Everything is optional. Write what matters.

## Discovery

When an AI agent encounters `/products/widgets/`, it looks for:
1. `/products/widgets/ai.txt`
2. `/products/ai.txt`
3. `/ai.txt`

Same logic works for filesystem paths and HTTP URLs.

## Why This Matters

- **Stop AI hallucination:** Put the truth in one place
- **Control your narrative:** Tell AI assistants exactly what you are
- **Simple and readable:** Humans and AI both understand plain text
- **Works everywhere:** HTTP, local folders, any path structure

## License

CC0 Public Domain.
