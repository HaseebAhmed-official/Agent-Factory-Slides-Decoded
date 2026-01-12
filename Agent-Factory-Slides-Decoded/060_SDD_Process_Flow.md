# Slide 60: SDD Process Flow

## Core Message
**The Lifecycle of an Agentic Project: From Constitution to Analysis**

### 1. Objective
To map the step-by-step execution flow of Spec-Driven Development. This slide provides the "State Machine" for an Agent Factory project.

### 2. Critical Analysis & Rationale
*   **The Importance of `/constitution`:** Before you build a feature, you must define the "Global Rules" (`AGENTS.md`). Without a constitution, agents are lawless.
*   **The `/clarify` Loop:** This is the most underrated step. If the AI doesn't understand the Spec, it MUST ask for clarification. Silicon-human communication is the bottleneck.

### 3. Step-by-Step Explanation

#### a. Basic Insights
1.  **/constitution:** Set global standards (`AGENTS.md`).
2.  **/specify:** Write the feature spec (`SPEC.md`).
3.  **/plan:** The agent proposes a technical architecture.
4.  **/tasks:** Break the plan into a checklist.
5.  **/implement:** The agent writes the code/skills.
6.  **/analyze:** Verify output against the Spec.

#### b. Advanced Insights (Deeper Look)
*   **The `/tasks` Granularity:** Large agents fail on large tasks. The `/tasks` step is a "Divide and Conquer" strategy. By breaking a goal into 10 small tasks, we increase the probability of success from 10% to 99%.
*   **The `/analyze` Phase (Evals):** This isn't just "Does it run?". It's "Does the logic match the intent?". We use **Semantic Analysis** to compare the resulting code's behavior with the Spec's requirements.
*   **Automated Project Management:** In this flow, the Agent acts as its own **Scrum Master**. It updates its own task list and reports progress.

### 4. When to Use?
*   **Daily Workflow:** Every new feature request should follow this 6-step loop.
*   **Automation:** Building a "Manager Agent" that forces other worker agents to stay in this loop.

### 5. Examples

#### a. Basic (Adding a Button)
*   *Specify:* Add 'Submit' button.
*   *Plan:* Edit `index.html`.
*   *Implement:* Add `<button>`.
*   *Analyze:* Check if button is visible.

#### b. Intermediate (DB Migration)
*   *Specify:* Move 'Users' to 'Accounts' table.
*   *Clarify:* "Should we keep the old IDs?" (Human: "Yes").
*   *Tasks:* 1. Create table. 2. Copy data. 3. Update references.
*   *Analyze:* Run SQL count on both tables.

#### c. PhD / Advanced (The Self-Correcting Factory)
*   *Concept:* **Recursive State Recovery.**
*   *Scenario:* The agent reaches the `/analyze` step and detects a failure. Instead of asking the human, it enters a sub-loop: it **Re-plans** based on the error log, updates its **Tasks**, and **Re-implements**. It only exits to the human if the sub-loop fails 3 times.

### 6. Implementation in Agentic AI
*   **Command Set:** Implement these as custom commands in your CLI (e.g., `agent /specify`, `agent /implement`).

### 7. Why This Matters?
*   **Predictability:** You always know what stage the project is in.
*   **Auditability:** Every step produces a document (Spec, Plan, Tasks, Analysis) that can be reviewed.

### 8. What Problem Does It Solve?
*   **The "Black Box" Execution:** Prevents the agent from "going dark" for 10 minutes and returning with a giant, broken codebase.

### 9. Architecture Deep Dive
*   **State Persistence:** The current "Step" is stored in a `.state.json` file, allowing the agent to "Resume" work if the connection is lost.

### 10. Common Practices & Pitfalls
*   **Pitfall:** Skipping `/plan` and going straight to `/implement`.
    *   *Correction:* AI often writes bad architecture if it doesn't plan first. Force the `/plan` step.
*   **Practice:** "Sign-off." A human must approve the `/plan` before the `/implement` step begins.

### 11. Reflection Questions
1.  *Which step in the flow are you currently skipping?*
2.  *How can you automate the '/analyze' step using another agent?*
3.  *What happens if an agent gets stuck in a '/clarify' loop?*
