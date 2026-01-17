# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a documentation repository containing curated lists of MCP (Model Context Protocol) servers and Claude Skills/Hooks. No build system or tests - just markdown files.

**Files:**
- `README.md` - Main landing page with links to other resources
- `mcp-servers.md` - MCP servers list with installation instructions
- `claude-skills.md` - Claude Skills and Hooks list

## GitHub Operations

**IMPORTANT:** Always use `gh` (GitHub CLI) instead of `git` directly for any GitHub operations like pushing, creating PRs, or managing issues.

```bash
# Push changes
gh repo sync

# Create PR
gh pr create --title "Title" --body "Description"

# View repo
gh repo view
```

For basic git operations (commit, staging), use `git` as normal since `gh` doesn't replace those.

## Content Format

When adding new entries to either list, follow the existing format:

1. Add to Table of Contents with category count and anchor links
2. Add entry under appropriate category section with:
   - `### Name` heading
   - Description paragraph
   - `🔗 [GitHub](url)` link
   - **CLI Installation:** code block
   - **JSON Configuration:** code block
   - `---` separator

## Adding MCP Servers

MCP servers go in `mcp-servers.md` under the appropriate category. If the category doesn't exist, create it and add to the Table of Contents.

## Adding Claude Skills/Hooks

Skills go in `claude-skills.md`. Skills use simpler installation instructions (often just referencing the source repo) while Hooks include setup commands.
