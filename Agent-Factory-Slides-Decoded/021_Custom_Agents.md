# Slide 21: Custom Agents (OpenAI Agents SDK, Claude Agent SDK)

## Core Message
**The Power of Specialization: Building the Enterprise Assembly Line**

### 1. Objective
To define "Option B" (Custom Agents). While General Agents are for exploration, Custom Agents are for *production*. This slide explains the architecture of building specialized, reliable, and standardized digital workers using SDKs.

### 2. Critical Analysis & Rationale
*   **The Reliability Factor:** In an enterprise, "creativity" is often a bug, not a feature. If you are processing 10,000 insurance claims, you want 100% compliance with SOPs. Custom Agents provide this deterministic guardrail.
*   **The SDK vs. Chatbot:** Custom agents are *engineered*, not just *prompted*. They exist within a software development lifecycle (SDLC) with versioning, testing, and deployment stages.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **Definition:** Purpose-built software coded using a framework (OpenAI/Anthropic SDK).
*   **Key Trait:** **Reliability**. You trade flexibility for control. You define the exact steps, tools, and guardrails.
*   **Interface:** Often headless (API-based) or embedded in existing apps (Slack, Salesforce).

#### b. Advanced Insights
*   **Orchestration Logic:** Unlike General Agents that plan dynamically, Custom Agents often follow a **Directed Acyclic Graph (DAG)** or a strict **State Machine**. You define the flow: `Step A -> If Success -> Step B -> Else -> Step C`.
*   **State management:** Custom agents carry state. They know "I am currently at Step 3 of the Invoice Approval Process." This state is usually stored in a database (SQL/Redis), making the agent persistent and resilient to crashes.
*   **Hand-offs:** Specialized agents can "hand off" a task to another agent. E.g., a "Triage Agent" analyzes a request and hands it to a "Billing Agent."

### 4. When to Use?
*   **High Volume:** "Process 50,000 claims." (General Agents are too expensive/slow).
*   **Compliance:** "Must follow these exact 5 legal checks." (General Agents might skip one).
*   **Customer-facing:** Where safety and brand voice are non-negotiable.

### 5. Examples

#### a. Basic (The Form Filler)
*   *Task:* Collect user feedback.
*   *Agent:* Asks 3 specific questions, validates answers, saves to DB. (Rigid, reliable).

#### b. Intermediate (The Customer Service Rep)
*   *Task:* Handle returns.
*   *Agent:* Verifies order ID (Tool), checks return policy (RAG), generates label (Tool), emails user (Tool). Logic: "If order > 30 days, reject."

#### c. PhD / Advanced (The Swarm Node)
*   *Concept:* **Micro-Agent Architecture.**
*   *Scenario:* A "Software Factory" is composed of 50 Custom Agents. One is the "Linter," one is the "Tester," one is the "Committer." They communicate via a message bus (Kafka). They are small, stateless, and extremely fast. A General Agent oversees them as the "Manager."

### 6. Implementation in Agentic AI
*   **The SDK Stack:** Using `openai-agents` or `langgraph`.
*   **Code Pattern:**
    ```python
    agent = Agent(
        name="RefundBot",
        instructions="You process refunds based on the SOP in SKILL.md",
        tools=[verify_order, issue_refund]
    )
    ```

### 7. Why This Matters?
*   **Cost Control:** Optimized execution avoids paying for "General Reasoning" on specific tasks.
*   **Brand Safety:** Hard guardrails prevent "AI gone wild" PR disasters.

### 8. What Problem Does It Solve?
*   **The "Wildcard" Problem:** General Agents can be unpredictable. Custom Agents provide the stability required for enterprise contracts.

### 9. Architecture Deep Dive
*   **The Control Loop:** `Trigger -> Rule -> Action`.
*   **Persistence Layer:** Using Redis to maintain agent "Memory" across different user sessions.

### 10. Common Practices & Pitfalls
*   **Pitfall:** Hard-coding everything.
    *   *Correction:* Allow *some* LLM reasoning for edge cases (the "Fuzzy Logic" layer), but wrap it in deterministic validation.
*   **Practice:** Use "Evals First." Write the test cases before building the agent.

### 11. Reflection Questions
1.  *Do you need a 'Genius' (General) or a 'Worker' (Custom)?*
2.  *Can you draw the flowchart of your agent's logic? If yes, build a Custom Agent.*
