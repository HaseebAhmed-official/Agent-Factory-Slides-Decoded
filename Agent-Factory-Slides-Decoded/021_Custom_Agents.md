# Slide 21: Custom Agents (OpenAI Agents SDK, Claude Agent SDK)

## Core Message
**The Power of Specialization: Building the Assembly Line**

### Detailed Analysis (Original Context)

#### 1. What it is:
A framework for building **AI Workflows**. Unlike General Agents that explore, Custom Agents are designed to follow a strict path.

#### 2. Key Features
1.  **Guardrails:**
    *   Strict control over what the agent can and cannot do. This is the "Safety first" approach.
2.  **Orchestration:**
    *   Define exact **Hand-offs** between multiple specialized agents.
    *   *Example:* Triage Agent (Identifies the problem) -> Support Agent (Fixes the problem).
3.  **UI/UX Flexibility:**
    *   Can be embedded directly into web apps, Slack, or internal company dashboards.
4.  **Enhanced by MCP and Agent Skills:**
    *   Like General Agents, they use MCP to connect to data and Skills to gain procedural knowledge.

#### 3. Best For:
*   **Standard Operating Procedures (SOPs):** Where there is a "right way" to do things.
*   **High-volume tasks:** e.g., processing 5,000 invoices per day.
*   **Customer-facing interactions:** Where safety and brand voice are non-negotiable.

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To define "Option B" (Custom Agents). While General Agents are for exploration, Custom Agents are for *production*. This slide explains the architecture of building specialized, reliable, and standardized digital workers using SDKs.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Definition: Purpose-built software coded using a framework (OpenAI/Anthropic SDK). Key Trait: **Reliability**. You trade flexibility for control.
*   **Advanced Insights:** Orchestration Logic: Often follows a **Directed Acyclic Graph (DAG)** or State Machine (`Step A -> Step B`). State Management: Persistent state in SQL/Redis allows resilience.

#### 3. Examples
*   **Basic:** Form Filler. Asks 3 specific questions, validates answers, saves to DB.
*   **Intermediate:** Return Handler. Verifies order ID, checks policy (RAG), generates label, emails user. Logic: "If > 30 days, reject."
*   **PhD / Advanced:** **Micro-Agent Architecture.** A "Software Factory" of 50 micro-agents (Linter, Tester, Committer) communicating via Kafka, overseen by a General Agent manager.

#### 4. Implementation in Agentic AI
*   **Code:** `agent = Agent(name="RefundBot", tools=[verify_order])`.
*   **Deployment:** Docker container on AWS Lambda.

#### 5. Why This Matters?
*   **Cost Control:** Optimized execution avoids paying for "General Reasoning" on specific tasks.
*   **Brand Safety:** Essential for customer-facing roles.

#### 6. Architecture Deep Dive
*   **Control Loop:** `Trigger -> Rule -> Action`. Contrast with General Agent's `Observe -> Think -> Act`.

#### 7. Reflection Questions
*   *Do you need a 'Genius' (General) or a 'Worker' (Custom)?*
*   *Can you draw the flowchart of your agent's logic? If yes, build a Custom Agent.*