# Slide 86: When NOT to Use AI Agents

## Core Message
**The Limits of Autonomy: Strategic Restraint**

### 1. Objective
To prevent catastrophic failure by defining the "Outer Bounds" of the technology. Knowing when *not* to use AI is as important as knowing when to use it.

### 2. Critical Analysis & Rationale
*   **The "Empathy Gap":** Agents simulate empathy; they don't feel it. In high-emotion situations, simulation is offensive.
*   **The "Probabilistic Risk":** Agents are never 100% correct. In scenarios where "99% is a failure" (Nuclear Launch), agents cannot be the final decision maker.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **High-Stakes, Irreversible Decisions:** Launching missiles, surgery, deleting production databases.
*   **Undefined Success:** If a human can't define "good," AI can't do it.
*   **Unstable Data:** If the rules change every 5 minutes, the agent will fail.
*   **Relationship-Critical:** Firing employees, apologies.

#### b. Advanced Insights (Deeper Look)
*   **The Expected Value Calculation:** `EV = (Benefit of Autonomy) - (Cost of Failure * Probability of Failure)`. If EV is negative, do NOT automate.
*   **Edge-Case Fragility:** AI is trained on the "Average." In "Black Swan" events (Unknown Unknowns), human intuition is superior to silicon reasoning because humans can reason from *first principles* outside the training distribution.

### 4. When to Use?
*   **Roadmap Pruning:** Killing bad ideas before they start.
*   **Ethical Review:** Ensuring the company stays human-centric.

### 5. Examples

#### a. Basic (The Wedding Vow)
*   *Bad Idea:* Using AI to write wedding vows. (Misses the point of vows).

#### b. Intermediate (The Production Delete)
*   *Bad Idea:* An agent that autonomously deletes "unused" servers without human approval. (Risk of deleting the wrong thing is too high).

#### c. PhD / Advanced (The Moral Dilemma)
*   *Concept:* **The Trolley Problem.**
*   *Scenario:* An autonomous vehicle faces a choice between hitting a pedestrian or crashing the car. This decision requires a moral framework that is not settled in society, let alone in code. **Rule:** Agents should not make moral choices; they should follow policy set by humans.

### 6. Implementation in Agentic AI
*   **Guardrails:** Implement "Human-Required" tags in your workflow engine for sensitive steps.

### 7. Why This Matters?
*   **Brand Reputation:** AI-driven PR disasters (e.g., Air Canada's chatbot promising refunds it shouldn't) are costly.
*   **Safety:** Physical safety is paramount.

### 8. What Problem Does It Solve?
*   **Over-Automation:** The tendency to try to automate everything, leading to diminishing returns and high risk.

### 9. Architecture Deep Dive
*   **Air-Gapping:** Physically disconnecting critical control systems from the Agent network to prevent accidental execution.

### 10. Common Practices & Pitfalls
*   **Pitfall:** "Human-in-the-Loop" becoming "Human-on-the-Loop."
    *   *Correction:* Ensure the human is actually paying attention, not just rubber-stamping agent actions.
*   **Practice:** "The Newspaper Test." If this went wrong and ended up on the front page, would it destroy us?

### 11. Reflection Questions
1.  *What is the one task in your company that must NEVER be automated?*
2.  *Does your agent know how to say 'I don't know'?*