# Slide 20: General Agents (Claude Code, Goose)

## Core Message
**The Power of Generalization: The Digital Polymath**

### Detailed Analysis (Original Context)

#### 1. What it is
An autonomous agent living in your terminal/environment. It "lives" where the work happens (the file system).

#### 2. Key Features
*   **Zero-Shot Planning:** You give it the goal; it determines every sub-step itself.
*   **Deep Integration:** Direct access to local files, git history, and command line.
*   **Enhanced by MCP:** Plugs into external systems (databases) instantly.
*   **Enhanced by Skills:** Loads modular folders (`SKILL.md`) for specific procedures.

#### 3. Best For
*   **Complex Debugging:** Where the error is unknown.
*   **Ad-hoc Analysis:** "Why are sales down?"
*   **Reasoning Loop:** Reads, thinks, acts, self-corrects.

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To deep dive into "Option A": The General Agent. Explaining what makes tools like Claude Code/Goose different from chatbots—specifically filesystem access and the execution loop.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Agents in the Terminal. They read/write files and run commands.
*   **Advanced Insights:** **Context Awareness.** They index your repo/file system, giving them "Grounding." **OODA Loop Optimization.** Fine-tuned for the Reasoning Loop—they know when to stop and check their work (e.g., running tests after coding).

#### 3. Examples
*   **Basic:** User: "App crashing." Agent: Runs app, sees error, greps source, edits config, restarts. Fixed.
*   **Intermediate:** User: "Convert Python to TS." Agent: Reads Python, writes TS, installs compiler, fixes type errors.
*   **PhD / Advanced:** **Recursive Architecture.** User: "Improve architecture." Agent: Analyzes dependency graph, identifies circular deps, refactors folder structure, moves files, runs tests, writes PR.

#### 4. Implementation in Agentic AI
*   **Install:** `npm install -g @anthropic-ai/claude-code`.
*   **Config:** `AGENTS.md` (Slide 51) tells the General Agent the rules of the repo.

#### 5. Why This Matters?
*   **Productivity:** "Cloning yourself."
*   **Junior Dev Replacement:** Replaces the "Junior Dev" role for bug fixing/refactoring.

#### 6. Architecture Deep Dive
*   **Shell Integration:** Wrapper around `zsh`/`bash`. Intercepts `stdout`/`stderr` to "see" results.

#### 7. Reflection Questions
*   *Have you installed a CLI agent yet?*
*   *Do you have an `AGENTS.md` file?*