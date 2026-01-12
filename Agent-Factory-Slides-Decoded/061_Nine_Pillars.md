# Slide 61: The Nine Pillars of the Agent Factory

## Core Message
**The Architectural Foundation**

### Detailed Analysis (Original Context)

#### 1. The List
1.  **CLI Agents:** Claude Code, Goose.
2.  **Markdown:** The language of Specs.
3.  **MCP:** Connectivity Standard.
4.  **AI IDEs:** Cursor, Windsurf.
5.  **Linux/Shell:** The OS.
6.  **TDD & Evals:** Testing reasoning.
7.  **SDD:** Spec-Driven Development.
8.  **Composable Skills:** Modular expertise.
9.  **Cloud-Native Deployment:** Docker, K8s.

#### 2. The Difference
"An amateur knows how to prompt. A professional masters these nine pillars."

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To provide a checklist for organizational maturity. If you are missing a pillar, your factory will collapse.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** You need more than just an LLM.
*   **Advanced Insights:** **Linux as the Agent OS.** Why Linux? Because agents need a deterministic, command-line driven environment to execute code. Windows/Mac GUIs are too "fuzzy" for agents. The "Headless Linux Container" is the natural habitat of the Digital FTE.

#### 3. Examples
*   **Basic:** Running a script.
*   **Intermediate:** Running a script in Docker (Pillar 9) triggered by a Spec (Pillar 7).
*   **PhD / Advanced:** **Self-Maintaining Factory.** An agent (Pillar 1) running on Linux (Pillar 5) uses TDD (Pillar 6) to verify a new Skill (Pillar 8) and deploys it to the Cloud (Pillar 9) automatically.

#### 4. Implementation in Agentic AI
*   **Audit:** Rate your team 1-5 on each pillar.

#### 5. Why This Matters?
*   **Holistic View:** Prevents "Tunnel Vision" where you focus only on the Model and forget the Infrastructure.

#### 6. Architecture Deep Dive
*   **The Dependency Graph:** Pillars 1-4 are "Dev Time." Pillars 5-9 are "Run Time."

#### 7. Reflection Questions
*   *Which pillar is your weakest link?*