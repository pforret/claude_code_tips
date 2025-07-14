# Essential MCP tools

## Best practices for agentic coding

> Setup & Customization:
> - Create CLAUDE.md files with project-specific commands, conventions, and guidelines
> - Configure allowed tools for safety and efficiency
> - Install GitHub CLI for better GitHub integration
>
> Expanding Capabilities:
> - Use bash tools and custom scripts
> - Leverage Model Context Protocol (MCP) servers
> - Create custom slash commands for repeated workflows
>
> Workflow Strategies:
> - Explore, Plan, Code, Commit approach: Read files → Make detailed plan → Implement → Commit/PR
> - Test-Driven Development: Write tests first → Confirm failure → Implement → Commit incrementally
>
> Optimization Tips:
> - Be specific in instructions and use visual references
> - Course-correct early and often
> - Use /clear to maintain a focused context
> - Employ multi-Claude workflows for complex tasks
>
> Advanced Techniques:
> - Use headless mode for automation
> - Employ "Safe YOLO mode" for uninterrupted work
> - Use Claude for codebase exploration and Q&A

* https://www.anthropic.com/engineering/claude-code-best-practices

## Context7

> Context7 pulls up-to-date, version-specific documentation and code examples directly from the source. Paste accurate, relevant documentation directly into tools like Cursor, Claude, or any LLM. Get better answers, no hallucinations, and an AI that actually understands your stack.

* https://context7.com/

## VisionCraft

> While other context providers like Context 7 aim to supply LLMs with up-to-date documentation, VisionCraft offers distinct advantages for developers seeking precision, breadth, and efficiency. VisionCraft boasts access to over 100,000 libraries, all kept current in real-time through our proprietary Raven engine, ensuring you're always working with the latest information.

* https://github.com/augmentedstartups/VisionCraft-MCP-Server

## Gemini CLI Integration for Claude Code MCP Server

> A complete setup guide for integrating Google's Gemini CLI with Claude Code through an MCP (Model Context Protocol) server. This provides automatic second opinion consultation when Claude expresses uncertainty or encounters complex technical decisions.

* https://gist.github.com/AndrewAltimit/fc5ba068b73e7002cbe4e9721cebb0f5

## Microsoft Playwright MCP

> A Model Context Protocol (MCP) server that provides browser automation capabilities using Playwright. This server enables LLMs to interact with web pages through structured accessibility snapshots, bypassing the need for screenshots or visually-tuned models.

* https://github.com/microsoft/playwright-mcp

## Chunkhound

> Transform your codebase into a searchable knowledge base. ChunkHound provides AI assistants with intelligent code search capabilities using natural language and regex patterns.

* https://github.com/ofriw/chunkhound

## Octocode

> The perfect code assistant that can help understand anything. Octocode provides AI-powered advanced search with heuristic discovery and smart fallbacks to understand connections between repositories and NPM packages across any privilege level you have.

* https://github.com/bgauryy/octocode-mcp