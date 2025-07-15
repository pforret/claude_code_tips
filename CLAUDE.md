# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a documentation repository containing Claude Code tips, best practices, and resources. It's a collection of knowledge about MCP (Model Context Protocol) tools, Git workflows, and essential commands for effective Claude Code usage.

This repository is licensed under the MIT License, encouraging open collaboration and knowledge sharing in the Claude Code community.

## Repository Structure

- **COMMANDS.md**: Links to essential slash commands from various context engineering projects
- **GIT.md**: Comprehensive guide on using Git as a checkpoint system with Claude Code
- **MCP.md**: Essential MCP tools and best practices for agentic coding
- **VERSION.md**: Current version tracking (0.0.3)
- **README.md**: Empty placeholder file

## Key Resources Referenced

### Context Engineering Sources
- **David Kimai**: https://github.com/davidkimai/Context-Engineering/tree/main/.claude/commands
- **Cole**: https://github.com/coleam00/context-engineering-intro/tree/main/.claude/commands
- **SuperClaude**: https://github.com/NomenAK/SuperClaude/tree/master/SuperClaude/Commands

### MCP Tools
- **Context7**: Real-time documentation provider (https://context7.com/)
- **VisionCraft**: 100,000+ libraries with real-time updates (https://github.com/augmentedstartups/VisionCraft-MCP-Server)
- **Gemini CLI Integration**: Second opinion consultation for complex decisions

### Best Practices Source
- **Anthropic Engineering**: https://www.anthropic.com/engineering/claude-code-best-practices

## Git Workflow Strategy

This repository follows a checkpoint-based Git workflow as documented in GIT.md:

1. Create feature branches: `git checkout -b [new_branch]`
2. Regular checkpoints: `git add . && git commit -m '[status]'`
3. Rollback capability: `git reset --hard [commit_hash]`
4. Squash before PR: `git rebase -i [start_commit]`
5. Force push if needed: `git push origin [branch] -f`

## Development Commands

This is a documentation-only repository with no build process, tests, or complex development setup. The primary workflow involves:

- **View files**: Standard file reading and editing
- **Update version**: Modify VERSION.md manually
- **Git operations**: Use the checkpoint workflow documented in GIT.md

## Working with This Repository

When making changes:
1. Follow the Git checkpoint strategy from GIT.md
2. Update VERSION.md for significant changes
3. Maintain the documentation structure and external links
4. Reference the MCP best practices when suggesting improvements

This repository serves as a knowledge base rather than executable code, focusing on documentation and resource curation for Claude Code users.