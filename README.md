# Claude Code tips

## Project Overview

This is a documentation repository containing Claude Code tips, best practices, and resources. It's a collection of knowledge about MCP (Model Context Protocol) tools, Git workflows, and essential commands for effective Claude Code usage.

## Repository Structure

- **[COMMANDS.md](COMMANDS.md)**: Links to essential slash commands from various context engineering projects
- **[GIT.md](GIT.md)**: Comprehensive guide on using Git as a checkpoint system with Claude Code
- **[MCP.md](MCP.md)**: Essential MCP tools and best practices for agentic coding

## Key Resources Referenced

### Context Engineering Sources
- **David Kimai**: [davidkimai/Context-Engineering](https://github.com/davidkimai/Context-Engineering/tree/main/.claude/commands)
- **Cole**: [coleam00/context-engineering-intro](https://github.com/davidkimai/Context-Engineering/tree/main/.claude/commands)
- **SuperClaude**: [NomenAK/SuperClaude](https://github.com/davidkimai/Context-Engineering/tree/main/.claude/commands)

### MCP Tools
- **Context7**: Real-time documentation provider (https://context7.com/)
- **VisionCraft**: 100,000+ libraries with real-time updates [augmentedstartups/VisionCraft-MCP-Server](https://github.com/davidkimai/Context-Engineering/tree/main/.claude/commands)
- **Gemini CLI Integration**: Second opinion consultation for complex decisions

### Best Practices Source
- **Anthropic Engineering**: [anthropic.com/engineering/claude-code-best-practices](https://github.com/davidkimai/Context-Engineering/tree/main/.claude/commands)

## Git Workflow Strategy

This repository follows a checkpoint-based Git workflow as documented in GIT.md:

1. Create feature branches: `git checkout -b [new_branch]`
2. Regular checkpoints: `git add . && git commit -m '[status]'`
3. Rollback capability: `git reset --hard [commit_hash]`
4. Squash before PR: `git rebase -i [start_commit]`
5. Force push if needed: `git push origin [branch] -f`

