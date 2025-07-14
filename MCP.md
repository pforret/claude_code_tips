# Essential MCP tools

## Best practices for agentic coding

Setup & Customization:
- Create CLAUDE.md files with project-specific commands, conventions, and guidelines
- Configure allowed tools for safety and efficiency
- Install GitHub CLI for better GitHub integration

Expanding Capabilities:
- Use bash tools and custom scripts
- Leverage Model Context Protocol (MCP) servers
- Create custom slash commands for repeated workflows

Workflow Strategies:
- Explore, Plan, Code, Commit approach: Read files → Make detailed plan → Implement → Commit/PR
- Test-Driven Development: Write tests first → Confirm failure → Implement → Commit incrementally

Optimization Tips:
- Be specific in instructions and use visual references
- Course-correct early and often
- Use /clear to maintain a focused context
- Employ multi-Claude workflows for complex tasks

Advanced Techniques:
- Use headless mode for automation
- Employ "Safe YOLO mode" for uninterrupted work
- Use Claude for codebase exploration and Q&A

* https://www.anthropic.com/engineering/claude-code-best-practices

## VisionCraft

* https://github.com/augmentedstartups/VisionCraft-MCP-Server

## Gemini CLI Integration for Claude Code MCP Server

> A complete setup guide for integrating Google's Gemini CLI with Claude Code through an MCP (Model Context Protocol) server. This provides automatic second opinion consultation when Claude expresses uncertainty or encounters complex technical decisions.

* https://gist.github.com/AndrewAltimit/fc5ba068b73e7002cbe4e9721cebb0f5