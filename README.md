# ai.txt

A proposed web standard for AI-readable website summaries.

## What is ai.txt?

Just as `robots.txt` tells search engine crawlers how to behave, `ai.txt` tells AI assistants what a website is about.

When someone asks an AI assistant about a business, the AI typically has to crawl multiple web pages, parse complex HTML, and piece together information from navigation menus, footers, and scattered content. This is slow, error-prone, and often misses important details buried in subpages—or worse, inside images.

An `ai.txt` file solves this by providing a single, plain text summary of everything an AI might need to know:

- Contact details
- Services offered
- Pricing
- Technical specifications
- Business hours
- Key policies

The AI fetches one small file and immediately has complete context.

## Format

The format is deliberately simple: **plain text with minimal markdown headings** for structure.

- No HTML parsing required
- No JavaScript rendering
- No cookie consent popups to navigate
- Any AI system can fetch and understand it immediately

Place the file at the root of your website: `https://example.com/ai.txt`

## Example

```
# Example Business

## About
Example Business is a web development agency based in Sydney, Australia.
Founded in 2020, we specialize in modern web applications.

## Services
- Custom web development
- E-commerce solutions
- API development
- Technical consulting

## Pricing
- Consultation: Free initial 30-minute call
- Hourly rate: $150 AUD
- Project-based: Starting from $5,000 AUD

## Contact
- Email: hello@example.com
- Phone: +61 2 1234 5678
- Address: 123 Main Street, Sydney NSW 2000

## Hours
Monday-Friday: 9am-5pm AEST
```

## Benefits

**For visitors:** Get accurate information about businesses through AI assistants instead of hallucinated or outdated details.

**For businesses:** Control your AI-facing narrative rather than leaving it to chance. As AI assistants become a primary way people discover and evaluate services, having a clear `ai.txt` becomes as important as having a clear website.

## Related Standards

- `robots.txt` - Instructions for search engine crawlers
- `sitemap.xml` - Site structure for search engines
- `security.txt` - Security contact information
- `humans.txt` - Information about the people behind the website

## Sites Using ai.txt

See [SITES.md](SITES.md) for a community-maintained list of websites using ai.txt.

To add your site, submit a pull request adding your domain to the list.

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a pull request.

## License

This specification is released into the public domain via [CC0](LICENSE).
