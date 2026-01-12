# Slide 20: General Agents (Claude Code, Goose)

## Core Message
**The Rise of the Digital Polymath**

### 1. Objective
To deep dive into "Option A": The General Agent. To explain what makes tools like Claude Code and Goose different from standard chatbots—specifically their ability to access the file system and manage their own execution loop.

### 2. Critical Analysis & Rationale
*   **The OS Interface:** These agents use the "Computer" as a tool. This is different from using "The Web" as a tool. Access to `bash` makes them omnipotent within the machine.
*   **The Loop:** The key differentiator is the *persistence* of the OODA loop. It keeps trying until it succeeds or you kill it.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **Identity:** These are "Agents in the Terminal." They live where the developer lives.
*   **Capabilities:** They can read files, edit code, run shell commands, and install packages.
*   **Zero-Shot Planning:** You give them a vague goal ("Fix the bug"), and they figure out the 10 steps to do it.

#### b. Advanced Insights
*   **The "Context Awareness":** Unlike a web chatbot (which knows nothing of your repo), these agents index your local file system. They have "Grounding" in your reality.
*   **The "OODA Loop" Optimization:** These tools are fine-tuned specifically for the *Reasoning Loop*. They know when to stop and check their work (e.g., running `npm test` after writing code).
*   **Tool-Use Native:** They treat the OS Shell as just another tool.

### 4. When to Use?
*   **Refactoring:** "Rename this variable across all 50 files."
*   **Onboarding:** "Explain how this authentication module works."
*   **Debugging:** "Run the tests, read the error, and fix the code."

### 5. Examples

#### a. Basic (The Fix)
*   *User:* "The app is crashing on startup."
*   *Agent:* Runs app -> Sees error -> Greps for error -> Edits config file -> Restarts app -> "Fixed."

#### b. Intermediate (The Migration)
*   *User:* "Convert this Python script to TypeScript."
*   *Agent:* Reads Python -> Writes TS -> Installs TS compiler -> Compiles -> Fixes type errors -> "Done."

#### c. PhD / Advanced (The Self-Architecting System)
*   *Concept:* **Recursive Architecture.**
*   *Scenario:* You ask the General Agent to "Improve the architecture of this project." It analyzes the dependency graph, identifies circular dependencies, creates a new folder structure, moves files, updates imports, runs tests to ensure nothing broke, and writes a PR description explaining the refactor.

### 6. Implementation in Agentic AI
*   **Installation:** `npm install -g @anthropic-ai/claude-code`
*   **Configuration:** `AGENTS.md` (Slide 51) is crucial here. It tells the General Agent the "Rules of the Road" for your specific repo.

### 7. Why This Matters?
*   **Productivity:** It is the closest thing to "Cloning yourself."
*   **The "Junior Dev" Replacement:** These agents effectively replace the "Junior Dev" role of basic bug fixing and refactoring.

### 8. What Problem Does It Solve?
*   **Context Switching:** You don't have to copy-paste code into ChatGPT. The agent is *in* the code.

### 9. Architecture Deep Dive
*   **The Shell Integration:**
    *   **Wrapper:** The Agent is a wrapper around `zsh` / `bash`.
    *   **I/O Interception:** It intercepts stdout/stderr to "See" the result of its actions.
    *   **Security:** It usually requires "Permission" for dangerous commands (like `rm -rf`).

### 10. Common Practices & Pitfalls
*   **Pitfall:** Trusting it blindly with `git push`.
    *   *Correction:* Always review the `git diff` before letting the agent commit. It *can* delete your work.
*   **Practice:** "Small Scopes." Don't say "Rebuild the app." Say "Refactor this component."

### 11. Reflection Questions
1.  *Have you installed a CLI agent yet? (If not, you are working too hard).*
2.  *Do you have an `AGENTS.md` file to guide your General Agent?*
