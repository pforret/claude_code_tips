# Folder and file structure for Claude Code

When using AI coding assistants like Claude Code, it's essential to provide them with structured context and instructions to ensure high-quality code generation. This document outlines the recommended folder and file structure to optimize the AI's performance in your coding projects.
To help optimize the code quality of AI-generated code, you should create and maintain specific Markdown files within your project's root folder or under the `.claude/` subfolder. These files serve to provide essential context and instructions to AI coding assistants like Claude Code, guiding them towards producing more accurate, consistent, and high-quality results.

Here is a list of recommended Markdown files and their purposes:

### Files in the Project Root Directory

*   **`CLAUDE.md`**:
    *   This is a **special file that Claude automatically reads into context** at the start of every session when you run Claude in that folder.
    *   **Purpose for Code Quality**:
        *   **Code Style Guidelines**: Document preferred coding styles, such as using ES modules (import/export) syntax over CommonJS (require), or destructuring imports.
        *   **Testing Instructions**: Include guidelines for testing, like preferring single tests over the whole test suite for performance, or general unit test patterns and coverage expectations.
        *   **Core Files and Utility Functions**: List important files or architectural decisions that Claude should always be aware of when making changes.
        *   **Repository Etiquette**: Mention branch naming, merge vs. rebase strategies, or other project-specific conventions.
        *   **Developer Environment Setup**: Specify tools, compilers, or environment variables necessary for the project.
        *   **Project Awareness**: Detail project architecture, technology stack, and current sprint goals, which ensures the AI generates code aligned with the project's vision.
        *   **Documentation Standards**: Define docstring formats and commenting practices.
    *   **Recommendation**: Keep it concise to avoid consuming too much context. This file should typically be **checked into Git and shared with your team** so everyone benefits from consistent AI guidance.

*   **`CLAUDE.local.md`**:
    *   This file is **for your personal preferences and configurations**.
    *   **Purpose for Code Quality**: You can use it to store personal aliases, preferred bash commands, or temporary instructions that you don't want to share with the team or commit to the repository. This helps streamline your individual workflow without cluttering shared project guidelines. You should usually `.gitignore` this file.

*   **`planning.md`**:
    *   This file serves as the **project vision**, outlining the architecture, technology stack, and required tools.
    *   **Purpose for Code Quality**: By providing a clear project blueprint, `planning.md` ensures Claude understands the foundational decisions, leading to code that adheres to the overall design. It helps prevent the AI from making assumptions or proposing solutions that deviate from the intended architecture.

*   **`tasks.md`**:
    *   This file is a **living list of concrete, actionable tasks** for the project, often organized by milestones.
    *   **Purpose for Code Quality**: Claude Code can be instructed to read `tasks.md` before starting work, mark completed tasks, and add new tasks it discovers. This ensures the AI is always working on relevant, uncompleted tasks, maintaining progress and avoiding redundant work. It acts as a **living project roadmap** that Claude checks off as it goes, ensuring continuity even across new sessions.

*   **`INITIAL.md`** (or similar, for feature requests):
    *   This file is used to **describe what you want to build**, providing specific functionality and requirements.
    *   **Purpose for Code Quality**: It's crucial for generating a comprehensive "Product Requirements Prompt" (PRP) which acts as a detailed blueprint for the AI. This ensures that the AI's initial understanding of the task is precise, leading to more accurate and aligned code generation from the outset.

*   **`README.md`**:
    *   While not exclusively for AI, a well-maintained `README.md` can provide **general project context**.
    *   **Purpose for Code Quality**: AI models can leverage this information to understand the project's purpose, main features, and setup instructions, which indirectly contributes to better code generation by providing foundational understanding.

### Files under the `.claude/` Subfolder

*   **`.claude/settings.json`** (or `~/.claude.json` for global settings):
    *   This file allows you to **customize the set of allowed and disallowed tools** that Claude Code can use, and other session settings.
    *   **Purpose for Code Quality/Safety**: By customizing the allowlist (e.g., `Edit` for file edits, `Bash(git commit:*)` for Git commits) and `disallowedTools` (e.g., `Bash(rm:*)`, `Bash(sudo:*)`), you can control what actions Claude can take, ensuring it operates within safe and desired boundaries. This helps prevent accidental data loss or insecure code execution. You can also configure context settings like `maxTokens`.

*   **`.claude/commands/`** (for custom slash commands):
    *   This folder stores Markdown files that define **reusable prompt templates or workflows** accessible via slash commands (e.g., `/optimize`, `/test`).
    *   **Purpose for Code Quality**: You can create commands for specific quality-related tasks, such as:
        *   **`/optimize.md`**: "Analyze the performance of this code and suggest three specific optimizations".
        *   **`/test.md`**: "Generate comprehensive unit tests for the current file with edge cases".
        *   **`/docs.md`**: "Create detailed documentation for this module including usage examples".
        *   **`/fix-github-issue.md`**: A command to analyze and fix a GitHub issue, including steps like searching the codebase, implementing changes, running tests, and ensuring linting/type checking.
    *   These commands ensure that complex, multi-step operations related to code quality are performed consistently and thoroughly. They can include special keywords like `$ARGUMENTS` to pass parameters, making them highly flexible.

*   **`.claude/config/architecture.md`** (or similar, within `.claude/config/` for sub-rules):
    *   This file can be used to store **specific architectural rules** or constraints relevant to a particular part of the codebase.
    *   **Purpose for Code Quality**: For example, in an Android project, it might define rules about "Clean Architecture violation detection". By feeding this to the AI, it can validate complex refactoring decisions and ensure code adheres to these deeper architectural patterns, beyond just style guides.

*   **`PRPs/` folder** (for Product Requirements Prompts):
    *   This folder contains detailed implementation blueprints that are generated from initial feature requests.
    *   **Purpose for Code Quality**: PRPs include comprehensive context and documentation, step-by-step implementation plans with validation gates, error handling patterns, and test requirements. They serve as structured instructions for the AI, ensuring it executes tasks accurately and produces high-quality, verified code.

*   **`examples/` folder**:
    *   This folder holds **relevant code examples and patterns** that the AI can learn from.
    *   **Purpose for Code Quality**: AI coding assistants perform significantly better when they can see patterns to follow. This includes code structure patterns (module organization, import conventions), testing patterns (test file structure, mocking), and integration patterns (API clients, database connections). Providing examples helps the AI generate code that is consistent with your existing codebase's quality standards.

By systematically setting up and utilizing these Markdown files, you can provide Claude Code with the rich, structured context it needs to optimize its code generation, leading to improved code quality, reduced errors, and greater consistency across your projects.