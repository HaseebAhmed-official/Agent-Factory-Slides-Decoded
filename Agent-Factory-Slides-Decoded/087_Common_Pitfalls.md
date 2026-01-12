# Slide 87: Common Pitfalls in Agent Implementation

## Core Message
**How Agent Factories Fail: Avoiding the Trap**

### Detailed Analysis (Original Context)

#### 1. Top 4 Pitfalls
1.  **Over-Automating Too Fast:** Building "CEO Agent" before the "Data Entry Agent."
2.  **Ignoring Edge Cases:** Assuming data is always perfect.
3.  **No Monitoring:** The "Silent Failure" where the agent burns tokens doing the wrong thing.
4.  **Vendor Lock-in:** Building in a format that only works on one platform.

#### 2. The Warning
"The most dangerous agent is **Confident and Wrong**. You need Checks and Balances."

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To provide a "Post-Mortem" before the project starts.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Start small, watch the logs, use standards.
*   **Advanced Insights:** **The "Recursive Spend" Trap.** An agent gets stuck in a loop: "I failed, let me retry. I failed again, let me retry..." Each retry costs $1.00. Without a `max_retries` guardrail, a simple bug can cost $10,000 in a single night. **Semantic Drift.** Over a long conversation, the agent's understanding of the goal "drifts" away from the original Spec.

#### 3. Examples
*   **Basic:** Forgetting to set a token limit.
*   **Intermediate:** Hard-coding API keys in the prompt (Security pitfall).
*   **PhD / Advanced:** **Prompt Fragility.** Relying on a "Magic Phrase" that works in GPT-4 but causes a total logic collapse in Claude 3.5. Solution: Use **Agent Skills** (Standardized Logic) and **Evals** (Cross-Model testing).

#### 4. Implementation in Agentic AI
*   **Checklist:** A pre-deployment checklist for every agent.

#### 5. Why This Matters?
*   **Economic Survival:** Managing the "Burn Rate" of your agents.

#### 6. Architecture Deep Dive
*   **The Watchdog Pattern:** A low-cost "Supervisor Agent" that does nothing but monitor the "Worker Agent" for loops or nonsense.

#### 7. Reflection Questions
*   *What is your 'Kill Switch' for runaway token spend?*
*   *Are you building 'Disposable Scripts' or 'Maintainable Systems'?*
