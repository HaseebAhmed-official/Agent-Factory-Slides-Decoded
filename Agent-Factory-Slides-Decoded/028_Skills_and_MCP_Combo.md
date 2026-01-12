# Slide 28: Skills and MCP Combination

## Core Message
**The How-To and The With-What: Orchestrating Capability**

### 1. Objective
To clarify the distinct but complementary roles of **Agent Skills** and **MCP**. This slide establishes the mental model: Skills are the *Procedure* (Software), MCP is the *Connection/Data* (I/O).

### 2. Critical Analysis & Rationale
*   **Separation of Concerns:** If you mix logic (Skill) with connectivity (MCP), your system becomes brittle. Decoupling them allows you to update the "Rules" without fixing the "Pipe."
*   **The Standardized Workforce:** This combo is what allows the "Agent Factory" to produce consistent results across different domains.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **Agent Skills (The "How-To"):** Procedural Knowledge. Markdown files, logic, checklists. (e.g., "The 10 steps to audit a tax return").
*   **MCP (The "With-What"):** Live Data Access. Database connections, API wrappers. (e.g., "Connection to the IRS database").
*   **The Synergy:** Skill + MCP = A functional Digital Employee.

#### b. Advanced Insights
*   **Chef Analogy:**
    *   *Skill:* The Recipe (Instructions).
    *   *MCP:* The Pantry/Stove (Tools and Ingredients).
    *   *Agent:* The Chef (The reasoning engine that follows the recipe using the tools).
*   **Stateless vs. Stateful:** Skills are often stateless text files. MCP servers are stateful (maintaining DB connections).
*   **Portability:** Skills are highly portable (Git-based). MCP servers require hosting infrastructure.

### 4. When to Use?
*   **Design Phase:** "We need a new capability. Do we need to write instructions (Skill) or connect a new system (MCP)?"
*   **Debugging:** "The agent knows *what* to do (Skill) but can't find the data (MCP)."

### 5. Examples

#### a. Basic (Writing)
*   *Skill:* "How to write a Haiku."
*   *MCP:* None needed (Model internal knowledge).

#### b. Intermediate (Financial Audit)
*   *Skill:* "Rules for GAAP compliance."
*   *MCP:* QuickBooks API connection.

#### c. PhD / Advanced (Autonomous Medical Diagnosis)
*   *Skill:* "Diagnostic Decision Tree" (Logic based on medical journals).
*   *MCP:* "Live Patient Vitals" (Streaming data from IoT sensors).
*   *Workflow:* The agent reads the vitals (MCP), applies the decision tree (Skill), and outputs a diagnosis.

### 6. Implementation in Agentic AI
*   **Folder Structure:**
    *   `/skills/audit_pro/SKILL.md`
    *   `/mcp/stripe_server.py`

### 7. Why This Matters?
*   **Auditability:** You can audit the `SKILL.md` to ensure the agent is following company policy.
*   **Swappability:** Swap the SQL DB for a NoSQL DB (Update MCP) without changing the business logic (Skill).

### 8. What Problem Does It Solve?
*   **The "Monolithic Agent" Problem:** Prevents building giant, unmaintainable prompt files where instructions and tool definitions are tangled.

### 9. Architecture Deep Dive
*   **The Execution Cycle:**
    1. Agent reads Skill.
    2. Agent identifies need for Data.
    3. Agent calls MCP tool.
    4. Agent applies Skill logic to MCP result.

### 10. Common Practices & Pitfalls
*   **Pitfall:** Putting business logic inside the MCP server code.
    *   *Correction:* Keep MCP servers "dumb." Put the logic in the human-readable `SKILL.md`.
*   **Practice:** "Mocking." Use a mock MCP server to test your Skills before connecting to production data.

### 11. Reflection Questions
1.  *Is your business logic hidden in code (Bad) or exposed in Skills (Good)?*
2.  *Can your agent work if the internet is down? (Depends on the MCP).*
