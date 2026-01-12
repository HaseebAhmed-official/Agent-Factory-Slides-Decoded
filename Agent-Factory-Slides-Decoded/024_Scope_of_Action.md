# Slide 24: Authority Defines the Scope of Action

## Core Message
**Coding Agents vs. General Agents: Defining the Bounds of Authority**

### 1. Objective
To clearly distinguish between the *specialized* "Coding Agent" (like Cursor) and the *generalized* "General Agent" (like Claude Code). This slide clarifies *where* they live and *what* they can touch.

### 2. Critical Analysis & Rationale
*   **Location is Strategy:** Where an agent "lives" determines its power. An agent in a browser is limited to the web. An agent in an IDE is limited to code. An agent in the *Terminal* has authority over the whole machine.
*   **The Scope of "Truth":** Coding agents look for truth in the code. General agents look for truth in the *environment*.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **Coding Agent (Cursor):** Living in the IDE. Scope is limited to software development. Purpose is being a "Pair Programmer."
*   **General Agent (Claude Code):** Living in the Terminal. Scope is any business domain. Purpose is being a "Digital Employee."

#### b. Advanced Insights
*   **The Permissions Boundary:** A Coding Agent usually lacks permission to execute arbitrary system commands (safety). A General Agent *is* a system command wrapper.
*   **The Context Boundary:** A Coding Agent sees the *Code*. A General Agent sees the *System State* (running processes, network connections, file permissions).
*   **The Goal-Native Nature:** General agents take "Objectives" (Outcome-based); Coding agents take "Instructions" (Output-based).

### 4. When to Use?
*   **Writing Code:** Use Cursor (Coding Agent). It has better autocomplete and syntax highlighting.
*   **Managing Systems:** Use Claude Code (General Agent). It can restart servers, install dependencies, and manage git.

### 5. Examples

#### a. Basic (Variable Renaming)
*   *Cursor:* Renames `user_id` to `account_id` in 5 files. (Text editing).
*   *Claude Code:* Refactors the whole module, runs the test suite, and pushes a commit to GitHub. (Workflow execution).

#### b. Intermediate (DevOps)
*   *Cursor:* Helps you write a Dockerfile.
*   *Claude Code:* Builds the Docker image, runs the container, checks if the port is open, and fixes the config if it fails.

#### c. PhD / Advanced (Cross-System Migration)
*   *Scenario:* Move a database from AWS to Azure.
*   *Action:* Claude Code (General Agent) uses AWS CLI to dump data, uses `scp` to move it, uses Azure CLI to restore it, and updates the `.env` file. A Coding Agent in an IDE could never perform this cross-system dance.

### 6. Implementation in Agentic AI
*   **The CLI Layer:** Building tools that expose the OS shell to the LLM via a structured tool-calling interface.

### 7. Why This Matters?
*   **Tool Selection:** Don't try to use Cursor to manage your AWS infrastructure. Don't use Claude Code to autocomplete a single line of code.
*   **Security:** General Agents are higher risk because they have shell access.

### 8. What Problem Does It Solve?
*   **The "Last Mile" Problem:** Coding Agents write the code, but they can't *deploy* it. General Agents close the loop.

### 9. Architecture Deep Dive
*   **Scope Hierarchy:**
    1.  **Level 1 (Line):** Autocomplete.
    2.  **Level 2 (File):** Refactoring.
    3.  **Level 3 (Repo):** Project management.
    4.  **Level 4 (System):** OS Control (General Agents).

### 10. Common Practices & Pitfalls
*   **Pitfall:** Expecting an IDE-based agent to know why your server is lagging.
    *   *Correction:* Switch to a Terminal-based General Agent to inspect the processes (`top`, `lsof`).
*   **Practice:** "Pairing." Use both. One for the text, one for the system.

### 11. Reflection Questions
1.  *Does your agent live in the 'Editor' or the 'Terminal'?*
2.  *Are you limited by the walls of your IDE?*
