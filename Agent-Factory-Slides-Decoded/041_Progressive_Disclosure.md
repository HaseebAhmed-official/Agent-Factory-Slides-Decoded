# Slide 41: Skills are Progressively Disclosed

## Core Message
**Managing Complexity through Reference: The "Hyperlink" Model for AI Context**

### 1. Objective
To teach "Token Management" and "Cognitive Load Management" for AI. Just as humans shouldn't memorize an encyclopedia to answer a simple question, agents shouldn't load massive documentation files into their context window unless necessary.

### 2. Critical Analysis & Rationale
*   **The "Lost in the Middle" Phenomenon:** LLMs perform worse when the critical information is buried in the middle of a massive prompt. Small, focused contexts yield higher accuracy.
*   **Economic Necessity:** Loading 100k tokens costs money. Loading 1k tokens costs pennies. Progressive disclosure is a cost-optimization strategy.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **The Problem:** If you put 10,000 lines of instructions into a single prompt, the AI gets confused and expensive.
*   **The Solution:** A `SKILL.md` file shouldn't contain *everything*. It should act as a **Map** or **Table of Contents**.
*   **The Mechanism:** The `SKILL.md` contains links or references to sub-documents (`docs/pricing.md`). The Agent only reads the sub-document if the user asks about pricing.

#### b. Advanced Insights (Deeper Look)
*   **Just-in-Time (JIT) Knowledge:** This mimics how operating systems manage memory (Paging). We keep the "Working Set" small and page in data from the "Disk" (Filesystem) only on a "Page Fault" (Missing information).
*   **Semantic Routing:** The top-level `SKILL.md` acts as a router. It directs the attention of the model to the specific sub-file required, preventing "Context Pollution."

### 4. When to Use?
*   **Complex Domains:** HR Policy bots (don't load the whole handbook). Legal bots (don't load all case law).
*   **Multi-Step Workflows:** Step 1 instructions shouldn't clutter the context when the agent is on Step 5.

### 5. Examples

#### a. Basic (The FAQ Bot)
*   *Structure:* `SKILL.md` lists topics. `docs/refunds.md` and `docs/shipping.md` contain details.
*   *Action:* User asks "Where is my package?" Agent reads `shipping.md`.

#### b. Intermediate (The Coder)
*   *Structure:* `SKILL.md` contains high-level architecture. `docs/api_v1.md` and `docs/api_v2.md` contain specs.
*   *Action:* User asks "Update the V2 endpoint." Agent reads `api_v2.md` and ignores V1.

#### c. PhD / Advanced (Hierarchical Memory Management)
*   *Concept:* **Recursive Context Swapping.**
*   *Scenario:* An agent is debugging a massive codebase. It starts with a "Map" of the directory structure. It "drills down" into `src/auth/`, reading only those files. Once the auth issue is resolved, it **Unloads** those files from its context window to free up space before moving to the `src/database/` module. It actively manages its own cognitive load.

### 6. Implementation in Agentic AI
*   **Tool:** `read_file(path)` is the primitive.
*   **Instruction:** "If you need more details on X, read file Y."

### 7. Why This Matters?
*   **Accuracy:** Focused agents hallucinate less.
*   **Scalability:** You can have a 10GB knowledge base but only use 10k tokens at a time.

### 8. What Problem Does It Solve?
*   **The Context Window Limit:** Even with 1M token windows, filling them up makes the model slow and dumb.

### 9. Architecture Deep Dive
*   **The Tree Structure:** Root (General) -> Branch (Category) -> Leaf (Specific). The agent traverses the tree based on user intent.

### 10. Common Practices & Pitfalls
*   **Pitfall:** Circular References.
    *   *Correction:* Ensure your documentation tree is a Directed Acyclic Graph (DAG).
*   **Practice:** "Summary Headers." Put a 1-sentence summary of what's in the sub-file in the main `SKILL.md` so the agent knows *why* to read it.

### 11. Reflection Questions
1.  *Are you 'stuffing' the prompt or 'linking' the context?*
2.  *Does your agent know how to look things up, or does it just guess?*
