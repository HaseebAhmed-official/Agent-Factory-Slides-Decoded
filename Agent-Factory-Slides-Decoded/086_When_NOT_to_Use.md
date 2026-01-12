# Slide 86: When NOT to Use AI Agents

## Core Message
**The Limits of Autonomy: Strategic Restraint**

### Detailed Analysis (Original Context)

#### 1. The 4 "Red Zones"
1.  **High-Stakes, Irreversible Decisions:** Nuclear launch, major surgery (autonomous).
2.  **Undefined Success Criteria:** If a human can't define "good," AI can't do it.
3.  **Unstable / Rapidly Changing Data:** Logic becomes outdated too fast.
4.  **Relationship-Critical Tasks:** Firing an employee, high-value apologies.

#### 2. The "Empathy Gap"
"Agents excel at Logic; they fail at Empathy. Use them for the 'Math,' not the 'Soul' of the business."

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To prevent catastrophic failure by defining the "Outer Bounds" of the technology.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Don't use AI for everything. Some things need humans.
*   **Advanced Insights:** **The Cost of Hallucination.** In low-stakes tasks (Writing a poem), the cost of a mistake is zero. In high-stakes tasks (Administering medication), the cost is infinite. Use the **Expected Value Calculation** to decide: `(Benefit of Autonomy) - (Cost of Failure * Probability of Failure)`. If negative, do NOT automate.

#### 3. Examples
*   **Basic:** Don't use AI to write your wedding vows (unless you're lazy).
*   **Intermediate:** Don't use AI to autonomously trade 100% of company treasury without human caps.
*   **PhD / Advanced:** **Edge-Case Fragility.** An AI trained on "normal" market conditions fails during a "Black Swan" event because its "Reasoning" is bounded by its training distribution. In "Unknown Unknown" scenarios, human intuition is superior to silicon reasoning.

#### 4. Implementation in Agentic AI
*   **Strategy:** Implement "Human-Required" tags in your workflow engine.

#### 5. Why This Matters?
*   **Brand Reputation:** AI-driven PR disasters are hard to recover from.
*   **Safety:** Physical safety is paramount.

#### 6. Architecture Deep Dive
*   **Air-Gapping:** Keeping critical controls disconnected from the Agent network.

#### 7. Reflection Questions
*   *What is the one task in your company that must NEVER be automated?*
*   *Does your agent know how to say 'I don't know'?*
