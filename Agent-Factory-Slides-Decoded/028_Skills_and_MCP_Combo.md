# Slide 28: Skills and MCP Combination

## Core Message
**The How-To and The With-What**

### Detailed Analysis (Original Context)

#### 1. Core Comparison
| Component | Agent Skills | MCP (Model Context Protocol) |
| :--- | :--- | :--- |
| **Metaphor** | **The "How-To"** | **The "With-What"** |
| **Identity** | "Expertise Packs" | "Data Pipe" |
| **Contents** | Modular folders with `SKILL.md`. | Protocol for connectivity. |
| **Example** | "Analyze financial statements." | Connection to SQL Database. |
| **Goal** | **Standardizing expertise.** | **Enabling live data access.** |

#### 2. The Relationship
You use a **Skill** to define the process and an **MCP** to give the agent the data it needs to perform that process.

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To clarify the distinct roles of **Agent Skills** and **MCP**. Skills are the *Procedure* (Software); MCP is the *Hardware/Connection* (I/O).

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Skills = Recipe Book. MCP = Pantry/Stove.
*   **Advanced Insights:** **Stateless vs Stateful.** Skills are often stateless text. MCP servers are stateful connections. **Portability.** Skills are highly portable; MCP servers require infrastructure.

#### 3. Examples
*   **Basic:** Writing Haiku. Skill: "How to write." MCP: None.
*   **Intermediate:** Financial Audit. Skill: "Check transactions > $5k." MCP: QuickBooks API.
*   **PhD / Advanced:** **Autonomous Surgery.** Skill: "Appendectomy Procedure" (Logic). MCP: "Da Vinci Robot Interface" (Motor Control).

#### 4. Implementation in Agentic AI
*   **Structure:** `/skills/audit/SKILL.md` + `/mcp/server.py`.
*   **Execution:** Agent loads Skill, connects to MCP.

#### 5. Why This Matters?
*   **Separation of Concerns:** Update the "Recipe" without changing the "Stove."

#### 6. Architecture Deep Dive
*   **Execution Flow:** Agent reads Skill (Observe) -> Skill says "Fetch" (Plan) -> Agent calls MCP (Act) -> MCP returns Data (Result) -> Agent applies Logic (Reason).

#### 7. Reflection Questions
*   *Is your business logic hidden in API wrappers (Bad) or exposed in Skills (Good)?*
*   *Can you swap out your database (MCP) without breaking your agent's behavior (Skill)?*