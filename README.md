# ai.txt

A web standard for AI-readable website summaries.

**Specification:** https://aitxt.ing

## What is ai.txt?

Just as `robots.txt` tells search engine crawlers how to behave, `ai.txt` tells AI assistants what a website is about.

Place a plain text file at `https://example.com/ai.txt` containing structured information about your business. AI agents fetch one small file and immediately have complete context.

## Quick Start

Create `/ai.txt` at your website root:

```
# Your Business Name

Brief description of your business.

Updated: 2026-01-14
AI-Contact: corrections@example.com

## Services
- Service one
- Service two

## Pricing
- Basic: $X/month
- Pro: $Y/month

## Contact
Email: hello@example.com
Phone: +1 234 567 8900
Hours: Monday-Friday 9am-5pm

## We Do Not Offer
- 24/7 support
- Refunds after 30 days
```

## Features

### Discovery
- **Primary:** Fetch `https://example.com/ai.txt`
- **Alternate:** DNS TXT record at `_ai.example.com` pointing to the file URL

### Linking
Reference related sites with `@domain` syntax:
```
## See Also
@parent-company.com
@partner.org
```

### Negative Assertions
Prevent AI hallucination by explicitly stating what you don't offer:
```
## We Do Not Offer
- Weekend support
- International shipping
```

### Language Variants
```
/ai.txt      (default)
/ai.fr.txt   (French)
/ai.de.txt   (German)
```

### Metadata
```
Updated: 2026-01-14
Canonical: https://example.com/ai.txt
AI-Contact: corrections@example.com
```

## For AI Developers

1. Check DNS TXT record `_ai.example.com` first
2. Fall back to `https://example.com/ai.txt`
3. Respect `Canonical` field if present
4. Follow `@domain` links for additional context
5. Honor negative assertions — don't invent capabilities

## Sites Using ai.txt

See [SITES.md](SITES.md) or the [directory](https://aitxt.ing/directory.html).

## Contributing

Submit a pull request to add your site or improve the specification.

## License

Released into the public domain via [CC0](LICENSE).
