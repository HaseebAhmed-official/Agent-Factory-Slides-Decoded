# Slide 60: Spec Driven Development Process (Visual Flow)

## Core Message
**The Lifecycle: Constitution -> Specify -> Plan -> Implement -> Verify**

### Detailed Analysis (Original Context)

#### 1. The Steps
1.  **Constitution (`AGENTS.md`):** Global rules.
2.  **Specify:** Feature Spec.
3.  **Plan:** Agent generates plan.
4.  **Tasks:** Break into steps.
5.  **Implement:** Agent writes code.
6.  **Analyze & Verify:** Run tests.

#### 2. The Feedback Loop
If verification fails, the agent loops back to **Plan** or **Implement**.

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To map the "Software Development Life Cycle" (SDLC) of the Agent Era.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** It's a circle, not a line.
*   **Advanced Insights:** **Automated PM.** The "Plan" and "Tasks" steps are usually done by a human Project Manager. Here, the Agent does them. The human only does "Specify" and "Verify." The middle is automated.

#### 3. Examples
*   **Basic:** Write spec -> Run agent -> Check code.
*   **Intermediate:** Agent generates a "Plan.md" for approval before writing code.
*   **PhD / Advanced:** **Multi-Agent Waterfall.** The "Architect Agent" writes the Plan. The "Coder Agent" implements it. The "QA Agent" verifies it. The human just watches the dashboard.

#### 4. Implementation in Agentic AI
*   **Orchestrator:** A script that manages this flow states.

#### 5. Why This Matters?
*   **Process Control:** Without a defined process, agents get lost in loops.
*   **Quality:** Verification is mandatory, not optional.

#### 6. Architecture Deep Dive
*   **State Machine:** `Idle -> Planning -> Coding -> Testing -> Done`.

#### 7. Reflection Questions
*   *Does your workflow allow the agent to 'Plan' before it 'Acts'?*