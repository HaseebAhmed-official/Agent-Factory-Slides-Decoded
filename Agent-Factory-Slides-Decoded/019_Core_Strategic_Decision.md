# Slide 19: The Core Strategic Decision

## Core Message
**Two Paths: General Agents vs. Custom Agents**

### Detailed Analysis (Original Context)

#### 1. The Two Paths
*   **Option A (General Agents):**
    *   *Identity:* The "Smart Consultant" (e.g., Claude Code, Goose).
    *   *Traits:* Flexible, Zero-Shot Planning, Reasoning Loop.
    *   *Use:* Complex, non-routine work.
*   **Option B (Custom Agents):**
    *   *Identity:* The "Assembly Line" (e.g., OpenAI SDK).
    *   *Traits:* Reliable, Specific, Guardrails, High-Volume.
    *   *Use:* Standardized workflows.

#### 2. Decision Matrix
*   **Task Type:** Novel (General) vs. Repetitive (Custom).
*   **End User:** Developer (General) vs. Customer (Custom).
*   **Cost:** High per-task (General) vs. Low per-task (Custom).

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To force a strategic choice. You cannot just "build an agent." You must decide: Are you building a flexible problem solver or a reliable process executor?

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Option A is the Consultant (smart/expensive). Option B is the Factory Machine (dumb/reliable).
*   **Advanced Insights:** **Spectrum of Autonomy.** General = High Autonomy. Custom = Low Autonomy. **Cost of Reasoning.** General agents pay a "reasoning tax" (tokens) for every step. Custom agents have the plan "hard-coded," making them cheaper. **Strategy:** Use General Agents to *build* Custom Agents.

#### 3. Examples
*   **Basic:** General: "Find me a flight to Europe." Custom: "Book flight UA123 for John."
*   **Intermediate:** Marketing Agency. General: Brainstorm campaign. Custom: Post tweets at 9 AM daily.
*   **PhD / Advanced:** **Just-in-Time Agent Creation.** A General Agent receives a complex task, realizes it's repetitive, writes code for a lightweight Custom Agent, spawns it, and manages it.

#### 4. Implementation in Agentic AI
*   **General:** CLI tools.
*   **Custom:** SDKs (`import { Agent } ...`).
*   **Convergence:** Making Custom agents smarter and General agents more reliable.

#### 5. Why This Matters?
*   **Efficiency:** Using General for custom tasks wastes money. Using Custom for general tasks fails.
*   **Architecture:** You need both—one to think, one to do.

#### 6. Architecture Deep Dive
*   **General:** ReAct Loop (Think -> Act -> Observe).
*   **Custom:** State Machine / DAG.

#### 7. Reflection Questions
*   *Is your problem 'Novel' or 'Repetitive'?*
*   *Are you paying 'Consultant' rates for 'Factory' work?*