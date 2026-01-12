# Slide 22: Decision Matrix: How to Choose?

## Core Message
**The Strategic Framework for Architecture Selection**

### 1. Objective
To provide a definitive, logic-based framework for choosing between General and Custom Agents. This prevents "Architecture Mismatch" (using a expensive generalist for a simple script, or a rigid script for a creative problem).

### 2. Critical Analysis & Rationale
*   **The Economic Constraint:** Running everything on a General Agent (like Claude Code) is unsustainable at scale.
*   **The UX Constraint:** Technical users want the power of a General Agent; non-technical users want the simplicity of a Custom Agent.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **Task Type:** Novel/Problem-Solving (General) vs. Repetitive/Standardized (Custom).
*   **End User:** Developers/Architects (General) vs. Customers/Employees (Custom).
*   **Error Tolerance:** High (General - human checks) vs. Low (Custom - must be correct).
*   **Implementation:** Instant (General) vs. Weeks/Build phase (Custom).

#### b. Advanced Insights
*   **The Lifecycle Theory:** Start with a **General Agent** to *discover* the optimal process for a new task. Once the process is documented and stabilized, refactor it into a **Custom Agent** for production scaling.
*   **The Cost Curve:** General Agents have *Linear* cost scaling (High marginal cost). Custom Agents have *Logarithmic* cost scaling (High fixed cost, but low marginal cost due to token optimization).

### 4. When to Use?
*   **Project Kickoff:** Use this matrix to decide which SDK/tool to download first.
*   **Budget Planning:** Calculate the ROI based on projected volume.

### 5. Examples

#### a. Basic (The Email Task)
*   *Task:* "Write a unique apology to my 5 clients." -> **General**.
*   *Task:* "Send 10,000 marketing emails." -> **Custom**.

#### b. Intermediate (The Data Task)
*   *Task:* "Find out why this SQL query is slow." -> **General**.
*   *Task:* "Run this report every morning at 8 AM." -> **Custom**.

#### c. PhD / Advanced (The Hybrid Router)
*   *Concept:* **MoE (Mixture of Experts) Task Routing.**
*   *Scenario:* A "Master Gateway" receives a user request. It uses a small classifier model to check the request against this Matrix.
    *   If `Novelty > 0.8`, route to **Claude Code (General)**.
    *   If `Novelty < 0.2`, route to a **Python script (Custom)**.
    *   *Result:* Optimal cost/performance ratio achieved automatically.

### 6. Implementation in Agentic AI
*   **The Router Pattern:** A supervisor agent that directs traffic between general reasoning nodes and specialized action nodes.

### 7. Why This Matters?
*   **Financial Survival:** Using General Agents for everything will bankrupt an AI startup.
*   **User Trust:** Using Custom Agents for novel tasks will lead to "I don't understand" errors.

### 8. What Problem Does It Solve?
*   **The "Hammer/Nail" Fallacy:** Developers tend to use the tool they are most comfortable with for everything. This forces a deliberate, business-aligned choice.

### 9. Architecture Deep Dive
*   **General Agent:** Optimized for context retrieval and long-chain reasoning.
*   **Custom Agent:** Optimized for low latency and high consistency.

### 10. Common Practices & Pitfalls
*   **Pitfall:** Building a Custom Agent for a task that only happens once a month.
    *   *Correction:* Just use a General Agent. The human time to build is more expensive than the tokens.
*   **Practice:** "The Graduation Protocol." A process for moving tasks from General to Custom based on volume triggers.

### 11. Reflection Questions
1.  *Look at your last 10 AI tasks. Which quadrant of the matrix did they fall in?*
2.  *Are you 'over-serving' your users (using expensive agents for cheap tasks)?*
