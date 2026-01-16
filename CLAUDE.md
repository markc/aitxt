# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Repository

This repository hosts the ai.txt specification at https://aitxt.ing.

```
/
├── index.html    # Documentation site
├── ai.txt        # Canonical specification
├── README.md     # GitHub entry point
├── CNAME         # Domain config
├── LICENSE       # CC0 public domain
├── aitxt         # Discovery script (bash)
└── aitxt.md      # Claude Code slash command
```

## Claude Code Tooling

The `/aitxt` slash command discovers and displays ai.txt files.

### Installation (Linux/macOS)

```bash
# Install discovery script
mkdir -p ~/.local/bin
cp aitxt ~/.local/bin/aitxt
chmod +x ~/.local/bin/aitxt

# Install Claude Code command
mkdir -p ~/.claude/commands
cp aitxt.md ~/.claude/commands/aitxt.md
```

Ensure `~/.local/bin` is in `$PATH`. Restart Claude Code to load the command.

### Usage

```
/aitxt                      # Current directory
/aitxt ~/Dev/myproject      # Local path
/aitxt https://example.com  # Remote URL
```

The script cascades up the directory/URL tree to find ai.txt, follows linked ai.txt files (depth=1), and displays a graph of discovered contexts.

## Editing Guidelines

- The canonical spec is `/ai.txt` — keep it minimal and self-contained
- No external ai.txt links in the spec (they get auto-followed)
- Documentation belongs in `index.html`, not the spec
- All frontmatter fields remain optional
