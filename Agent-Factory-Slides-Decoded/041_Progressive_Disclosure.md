# Slide 41: Skills are Progressively Disclosed

## Core Message
**Managing Complexity through Reference**

### Detailed Analysis (Original Context)

#### 1. The Problem
If you put 10,000 lines of instructions into a single prompt, the AI gets confused (Lost in the middle phenomenon) and uses too many tokens.

#### 2. The Solution: Progressive Disclosure
A `SKILL.md` file shouldn't contain *everything*. It should act as a **Map**.

#### 3. How it works
1.  **Level 1:** `SKILL.md` (High-level overview + core logic).
2.  **Level 2:** References to other files:
    *   "For specific pricing rules, see `docs/PRICING_GUIDE.md`."
3.  **The Agent's Action:** The agent only reads the sub-documents **when it needs them**.

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To teach "Token Management" and "Cognitive Load Management" for AI. Just as humans shouldn't memorize an encyclopedia, agents shouldn't load everything into context.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Don't dump the whole manual. Give the Table of Contents.
*   **Advanced Insights:** **Context Window Optimization.** Using "Just-in-Time" loading reduces costs and increases accuracy. If the agent loads irrelevant data, it distracts from the current task (Attention mechanisms dilute).

#### 3. Examples
*   **Basic:** `SKILL.md` says "Read `rules.txt` if user asks about rules."
*   **Intermediate:** `SKILL.md` links to `docs/api_v1.md`, `docs/api_v2.md`. Agent chooses which one to read based on user request.
*   **PhD / Advanced:** **Hierarchical Memory.** The `SKILL.md` acts as the "Operating System Kernel," paging memory in and out. It can even *unload* context to free up space for reasoning.

#### 4. Implementation in Agentic AI
*   **Mechanism:** `read_file()` tool. The LLM decides when to call it.

#### 5. Why This Matters?
*   **Scalability:** You can have a 1GB knowledge base but only use 10k tokens at a time.
*   **Focus:** Focused agents hallucinate less.

#### 6. Architecture Deep Dive
*   **Tree Structure:** Root -> Branch -> Leaf. The agent traverses the tree.

#### 7. Reflection Questions
*   *Are you 'stuffing' the prompt or 'linking' the context?*
*   *Does your agent know how to look things up?*