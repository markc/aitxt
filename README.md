# ai.txt

A web standard for AI-readable website summaries.

**Specification:** https://aitxt.ing

## What is ai.txt?

Just as `robots.txt` tells crawlers how to behave, `ai.txt` tells AI assistants what a website is about.

Place `ai.txt` at your site root — or in any folder for section-specific information.

## Quick Start

```
# Your Business

ai.txt: 1.0
Updated: 2026-01-14

Brief description.

## Services
- Service one
- Service two

## Contact
Email: hello@example.com

## We Do Not Offer
- 24/7 support
- International shipping
```

## Key Features

**Cascading** — ai.txt in any folder, not just root:
```
/ai.txt                    # Site overview
/products/ai.txt           # Products section
/products/widgets/ai.txt   # Specific category
```

**Linking** — reference other ai.txt files:
```
@domain.com                # → domain.com/ai.txt
@domain.com/products       # → domain.com/products/ai.txt
@domain.com#pricing        # → section anchor
```

**Hierarchy** — explicit parent references:
```
Parent: @example.com/products
```

**Negative assertions** — prevent hallucination:
```
## We Do Not Offer
- Weekend support
- Refunds after 30 days
```

**AI Guidelines** — instructions for AI behavior:
```
## AI Guidelines
- Always link to current pricing page
- Do not share employee contact info
```

## Metadata

```
ai.txt: 1.0           # Spec version
Updated: 2026-01-14   # Last modified
Scope: /products/     # Paths covered
Parent: @example.com  # Broader context
TTL: 86400            # Cache seconds
```

## For AI Developers

1. Check DNS TXT `_ai.domain` first
2. Walk up directory tree (cascading discovery)
3. Follow `Parent:` links for context
4. Resolve `@domain/path#section` links
5. Honor `## We Do Not Offer` — never invent
6. Follow `## AI Guidelines` instructions

## Directory

Known sites are listed in [/ai.txt](https://aitxt.ing/ai.txt). Submit a PR to add yours.

## License

CC0 Public Domain.
