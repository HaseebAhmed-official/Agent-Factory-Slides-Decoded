# Slide 44: General Purpose Agents Stack

## Core Message
**The Layered Architecture: Agent + Skills + MCP + Model**

### 1. Objective
To define the reference architecture for the 2026 Agent Stack. This visualization helps developers understand *where* to inject their code and how the components interact.

### 2. Critical Analysis & Rationale
*   **Decomposition:** Monolithic architectures fail at scale. By breaking the agent into "Brain" (Model), "Orchestrator" (Agent), "Knowledge" (Skills), and "Hands" (MCP), we create a system that is modular, upgradeable, and robust.
*   **The "Sandwich" Model:** The value is in the middle (Skills/MCP). The bottom (Model) is a commodity. The top (Agent) is the runtime.

### 3. Step-by-Step Explanation

#### a. Basic Insights
1.  **Model (Bottom):** The Raw Intelligence (Claude 3.5, GPT-4). The "CPU" of the system.
2.  **MCP Servers:** The Tools / Data (Git, SQL). The "I/O" ports.
3.  **Agent Skills:** The Logic / Knowledge (`SKILL.md`). The "Software" running on the CPU.
4.  **General Agent (Top):** The Orchestrator (Claude Code). The "Operating System" that manages the resources.

#### b. Advanced Insights (Deeper Look)
*   **Interchangeability:** Because the layers are decoupled, you can swap the Model (e.g., from GPT-4 to Llama-3) without rewriting the Skills. This protects against model obsolescence.
*   **The "Formula":** `General Purpose Agent = Brain + Knowledge + Connectivity`. You need all three. A brain without connectivity is a chatbot. Connectivity without knowledge is a script.

### 4. When to Use?
*   **System Design:** When planning the architecture of a new agent.
*   **Debugging:** Identifying which layer is failing. (Is it a model hallucination? A skill logic error? Or an MCP connection failure?).

### 5. Examples

#### a. Basic (Stacking Blocks)
*   *Stack:* Claude 3.5 + "Chat Skill".

#### b. Intermediate (The Switch)
*   *Action:* Switching from OpenAI Agents SDK to Anthropic Agents SDK while keeping the same `SKILL.md` files. This proves the portability of the Skill layer.

#### c. PhD / Advanced (Dynamic Stack Reconfiguration)
*   *Concept:* **Runtime Optimization.**
*   *Scenario:* An agent detects it is low on budget. It dynamically swaps the "Model Layer" from GPT-4 (Expensive) to Haiku (Cheap) for the next simple task, then swaps back to GPT-4 for complex reasoning. The "Agent Layer" manages this virtualization transparently.

### 6. Implementation in Agentic AI
*   **Config:** `model: "claude-3-opus"`, `skills: ["./coding"]`, `mcp: ["github"]`.

### 7. Why This Matters?
*   **Future-Proofing:** Don't hard-code your logic into the model (Fine-tuning). Put it in the Skill layer so it survives model updates.
*   **Cost Management:** Swap models based on task difficulty.

### 8. What Problem Does It Solve?
*   **Vendor Lock-in:** By separating the layers, you are not beholden to one model provider.

### 9. Architecture Deep Dive
*   **The "Context Bus":** Data flows up and down this stack via the Context Window. The Agent Layer manages the bandwidth of this bus.

### 10. Common Practices & Pitfalls
*   **Pitfall:** Tight coupling. Hard-coding model-specific quirks into your Skills.
    *   *Correction:* Keep Skills generic and model-agnostic.
*   **Practice:** "Layered Testing." Test the MCP independently. Test the Skill with a mock MCP. Test the Agent with the real stack.

### 11. Reflection Questions
1.  *Is your architecture loosely coupled (good) or tightly coupled (bad)?*
2.  *If OpenAI disappeared tomorrow, could you swap in Anthropic without rewriting your business logic?*
