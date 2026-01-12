# Slide 83: Blueprint for a Perfect Agent Spec (Part 1)

## Core Message
**The Three Foundational Pillars: Identity, Context, Logic**

### Detailed Analysis (Original Context)

#### 1. Identity (The Persona)
*   *What:* The role and tone.
*   *Example:* "Senior Tax Auditor with 20 years experience. Precise, skeptical, formal."

#### 2. Context (The World)
*   *What:* Data access and environmental knowledge.
*   *Example:* "Access to `transactions` SQL via MCP and `TAX_CODE.pdf`."

#### 3. Logic (The Guardrails)
*   *What:* The "Golden Rules" and constraints.
*   *Example:* "Never approve deductions > $5,000 without human flagging."

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To provide a structural template for high-fidelity agent instructions.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Define Who it is, What it knows, and What it can't do.
*   **Advanced Insights:** **Separation of Concerns.** By separating Identity from Logic, you can use the same "Auditor Persona" with different "Tax Code Contexts" for different countries. This makes your agent components **Modular** and **Reusable**.

#### 3. Examples
*   **Basic:** "You are a friendly bot."
*   **Intermediate:** "You are a Support Bot (Identity) with access to the Jira API (Context). You must never promise a refund (Logic)."
*   **PhD / Advanced:** **Dynamic Persona Modulation.** A Spec that allows the agent to adjust its "Logic" based on the "Context" (e.g., "In Emergency Mode, bypass standard approval logic but log all actions to the Emergency Ledger").

#### 4. Implementation in Agentic AI
*   **Format:** YAML frontmatter in `SKILL.md` for structured fields.

#### 5. Why This Matters?
*   **Safety:** Guardrails are the only thing preventing your agent from becoming a liability.

#### 6. Architecture Deep Dive
*   **The Persona Layer:** Acts as a "System Filter" for every response the model generates.

#### 7. Reflection Questions
*   *What is the 'Top 3' list of things your agent should NEVER do?*
*   *Does your agent have the context it needs to be successful?*
