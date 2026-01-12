# Slide 44: General Purpose Agents Stack

## Core Message
**The Layered Architecture: Agent + Skills + MCP + Model**

### Detailed Analysis (Original Context)

#### 1. The Stack (Top to Bottom)
1.  **General Agent:** The Brain / Orchestrator (Claude Code).
2.  **Agent Skills:** The Logic / Knowledge (`SKILL.md`).
3.  **MCP Servers:** The Tools / Data (Git, SQL).
4.  **Model:** The Raw Intelligence (Claude 3.5, GPT-4).

#### 2. The "Formula"
**General Purpose Agent = Brain + Knowledge + Connectivity**

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To define the reference architecture. This visualization helps developers understand *where* to inject their code.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** It's a sandwich. Model at bottom, Agent on top, Skills/MCP in the middle.
*   **Advanced Insights:** **Interchangeability.** Because the layers are decoupled, you can swap the Model (e.g., from GPT-4 to Llama-3) without rewriting the Skills. This protects against model obsolescence.

#### 3. Examples
*   **Basic:** Stacking blocks.
*   **Intermediate:** Switching from OpenAI SDK to Anthropic SDK while keeping the same `SKILL.md`.
*   **PhD / Advanced:** **Dynamic Stack Reconfiguration.** An agent detects it is low on budget, so it swaps the "Model Layer" from GPT-4 (Expensive) to Haiku (Cheap) for the next simple task, then swaps back.

#### 4. Implementation in Agentic AI
*   **Config:** `model: "claude-3-opus"`, `skills: ["./coding"]`, `mcp: ["github"]`.

#### 5. Why This Matters?
*   **Future-Proofing:** Don't hard-code your logic into the model (Fine-tuning). Put it in the Skill layer.
*   **Cost Management:** Swap models based on task difficulty.

#### 6. Architecture Deep Dive
*   **The "Context Bus":** Data flows up and down this stack via the Context Window.

#### 7. Reflection Questions
*   *Is your architecture loosely coupled or tightly coupled?*