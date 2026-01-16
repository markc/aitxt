---
description: Discover and display ai.txt context files from projects or websites
allowed-tools: Bash, Read, WebFetch
---

# Discover ai.txt

Run the aitxt discovery script to find ai.txt context files:

```bash
~/.local/bin/aitxt $ARGUMENTS
```

If no arguments provided, use the current working directory.

## After Running

1. **If found**: Read and summarize the ai.txt content, highlighting:
   - What the project/service does
   - Key constraints or limitations
   - Any linked ai.txt files worth exploring

2. **If not found**: Let the user know, and suggest they could create one

## Examples

- `/aitxt` — Check current directory
- `/aitxt ~/Dev/myproject` — Check a local project
- `/aitxt https://example.com` — Check a website
