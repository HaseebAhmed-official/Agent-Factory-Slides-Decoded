# Slide 19: The Core Strategic Decision

## Core Message
**General Agents vs. Custom Agents: Choosing Your Path**

### 1. Objective
To force a strategic choice. You cannot just "build an agent." You must decide: Are you building a flexible problem solver (General) or a reliable process executor (Custom)? This is the "Build vs. Buy" decision of the Agentic Era.

### 2. Critical Analysis & Rationale
*   **The Trade-off:** There is a fundamental trade-off between **Autonomy** and **Reliability**. High Autonomy (General) = Lower Reliability. Low Autonomy (Custom) = Higher Reliability.
*   **The Hybrid Solution:** The best architecture uses General Agents to *build* Custom Agents.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **Option A: General Agents (The Consultant).**
    *   *Examples:* Claude Code, Goose.
    *   *Trait:* Smart, flexible, expensive, requires supervision. Good for "figuring things out."
*   **Option B: Custom Agents (The Factory Worker).**
    *   *Examples:* OpenAI Agents SDK, Custom Python Scripts.
    *   *Trait:* Narrow, reliable, cheap, follows a script. Good for "doing the same thing 1,000 times."

#### b. Advanced Insights
*   **The "Spectrum of Autonomy":**
    *   *General:* High Autonomy (decides its own plan).
    *   *Custom:* Low Autonomy (follows a directed graph).
*   **The "Cost of Reasoning":** General agents use more tokens because they have to "think" for every step. Custom agents have the plan "hard-coded" (or prompt-coded), so they are cheaper.
*   **The "Hybrid" Strategy:** Use a General Agent to *build* the Custom Agent. (The Factory Model).

### 4. When to Use?
*   **General:** Exploration, Debugging, Coding, Research, Ad-hoc tasks.
*   **Custom:** Customer Support, Invoice Processing, Data Entry, Compliance Checks.

### 5. Examples

#### a. Basic (The Difference)
*   *General:* "Go find me a flight to anywhere in Europe." (Explores).
*   *Custom:* "Book flight UA123 for John Doe." (Executes).

#### b. Intermediate (The Business Choice)
*   *Scenario:* You run a marketing agency.
*   *Decision:* Use a **General Agent** to brainstorm campaign ideas (creative). Use a **Custom Agent** to post the tweets at 9 AM every day (mechanical).

#### c. PhD / Advanced (Dynamic Instantiation)
*   *Concept:* **Just-in-Time Agent Creation.**
*   *Scenario:* A General Agent receives a complex task. It realizes the task is repetitive. It *writes the code* for a lightweight Custom Agent to handle the repetition, spawns it, monitors it, and then kills it when the job is done. The General Agent acts as the "Manager" hiring a "Temp."

### 6. Implementation in Agentic AI
*   **General:** Use CLI tools (`claude`).
*   **Custom:** Use SDKs (`import { Agent } from 'openai-agents'`).
*   **Convergence:** The goal is to make Custom agents as smart as General agents, and General agents as reliable as Custom agents.

### 7. Why This Matters?
*   **Efficiency:** Using a General Agent for a Custom task is a waste of money (Tokens). Using a Custom Agent for a General task leads to failure (Rigidity).
*   **Architecture:** Your system needs both. One to think, one to do.

### 8. What Problem Does It Solve?
*   **The "One Size Fits All" Fallacy:** Developers try to use one agent for everything. This slide splits them into appropriate roles.

### 9. Architecture Deep Dive
*   **General Architecture:** ReAct Loop (Think -> Act -> Observe).
*   **Custom Architecture:** State Machine / DAG (Step 1 -> Step 2 -> Step 3).

### 10. Common Practices & Pitfalls
*   **Pitfall:** Over-using General Agents.
    *   *Correction:* Don't use Claude Code to scrape 1,000 websites. It's too slow/expensive. Write a script (Custom Agent) to do it.
*   **Practice:** "Prototype with General, Productionize with Custom."

### 11. Reflection Questions
1.  *Is your problem 'Novel' (General) or 'Repetitive' (Custom)?*
2.  *Are you paying 'Consultant' rates for 'Factory' work?*
