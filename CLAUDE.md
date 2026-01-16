# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Project Purpose

This repository documents **ai.txt**—a universal standard for AI-readable context about any resource (websites, projects, folders, services, etc.). The spec itself is written in ai.txt format at `/ai.txt`, demonstrating the concept through dogfooding.

## Repository Structure

```
/
├── index.html    # Human-friendly landing page
├── ai.txt        # The specification itself (in ai.txt format)
├── README.md     # GitHub entry point
├── CNAME         # aitxt.ing domain
├── LICENSE       # CC0 public domain
├── aitxt         # Discovery script for CLI/shell usage
└── aitxt.md      # Claude Code slash command definition
```

## Key Philosophy

- **Simplicity first:** All frontmatter fields are optional. Plain text prose is primary.
- **Low barrier to entry:** Non-technical users should write ai.txt files in minutes without learning schemas.
- **Humans first, AI second:** Files should read naturally and make sense to both people and AI agents.
- **Extensibility without pollution:** Complex requirements (database imports, strict validation) are handled by separate profiles, not in the base spec.

## Understanding the Spec

The canonical reference is `/ai.txt` at https://aitxt.ing/ai.txt. It contains:
- Full specification with examples
- Format and frontmatter guidance (all optional)
- Usage examples for websites, projects, local folders
- How AI agents should discover and use ai.txt files

Do not edit the spec based on assumptions. Always check `/ai.txt` for the current understanding.

## Claude Code Integration

This repository includes tooling for Claude Code's `/aitxt` slash command, enabling AI agents to discover and read ai.txt context files.

### Components

- **`aitxt`** — Bash script that discovers ai.txt files by cascading up the directory tree (local) or URL path (remote)
- **`aitxt.md`** — Claude Code slash command definition that invokes the script

### Installation (Linux)

1. **Install the discovery script:**
   ```bash
   mkdir -p ~/.local/bin
   cp aitxt ~/.local/bin/aitxt
   chmod +x ~/.local/bin/aitxt
   ```
   Ensure `~/.local/bin` is in your `$PATH`.

2. **Install the Claude Code slash command:**
   ```bash
   mkdir -p ~/.claude/commands
   cp aitxt.md ~/.claude/commands/aitxt.md
   ```

3. **Restart Claude Code** to discover the new command.

4. **Verify installation:**
   ```bash
   # Test the script directly
   aitxt ~/Dev/some-project
   aitxt https://example.com
   ```

   In Claude Code:
   ```
   /aitxt
   /aitxt ~/Dev/myproject
   /aitxt https://aitxt.ing
   ```

### How It Works

The `aitxt` script:
- Accepts a local path or HTTP URL (defaults to current directory)
- For local paths: walks up the directory tree looking for `ai.txt`
- For URLs: tries the path, then cascades to parent URLs
- Outputs the found ai.txt content or an error if not found

The Claude Code command:
- Runs the script with any provided arguments
- Summarizes the ai.txt content for the user
- Highlights key project info, constraints, and linked contexts

## When Reviewing PRs

1. Check that changes align with the philosophy of simplicity and low barrier to entry
2. Verify examples are accurate and up-to-date with the current spec in `/ai.txt`
3. Ensure documentation doesn't add unnecessary complexity or mandatory fields
4. Point contributors to `/ai.txt` as the canonical reference
