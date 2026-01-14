---
layout: default
title: ai.txt - AI-Readable Website Summaries
---

# ai.txt

A proposed web standard for AI-readable website summaries.

## The Problem

When someone asks an AI assistant about a business, the AI typically has to:
- Crawl multiple web pages
- Parse complex HTML
- Navigate cookie consent popups
- Piece together information from navigation menus, footers, and scattered content

This is slow, error-prone, and often misses important details buried in subpages—or worse, inside images.

## The Solution

An `ai.txt` file provides a single, plain text summary of everything an AI might need to know about a website:

```
https://example.com/ai.txt
```

One small file. Complete context. Immediate understanding.

## Format

Plain text with markdown headings. No HTML parsing, no JavaScript rendering, no special tools required.

```
# Business Name

## About
Brief description of the business.

## Services
- Service one
- Service two

## Pricing
- Basic: $X/month
- Pro: $Y/month

## Contact
- Email: hello@example.com
- Phone: +1 234 567 8900

## Hours
Monday-Friday: 9am-5pm
```

## Benefits

**For visitors:** Accurate information through AI assistants instead of hallucinated or outdated details.

**For businesses:** Control your AI-facing narrative. As AI assistants become a primary discovery channel, a clear `ai.txt` becomes as important as a clear website.

## Get Started

1. Create a plain text file named `ai.txt`
2. Add your business information using markdown headings
3. Place it at your website root: `https://yourdomain.com/ai.txt`
4. [Add your site to the directory](https://github.com/markc/aitxt)

## Browse Examples

See real-world implementations in the [ai.txt Directory](directory).

## Related Standards

| Standard | Purpose |
|----------|---------|
| `robots.txt` | Instructions for search engine crawlers |
| `sitemap.xml` | Site structure for search engines |
| `security.txt` | Security contact information |
| `humans.txt` | Information about the people behind the site |
| **`ai.txt`** | Structured information for AI assistants |

## Specification

See the full [specification and examples on GitHub](https://github.com/markc/aitxt).
