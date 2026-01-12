# Slide 40: Skills can include scripts as tools

## Core Message
**Turning Documentation into Action (Hybrid Logic)**

### Detailed Analysis (Original Context)

#### 1. How it works
`SKILL.md` tells the agent *when* to use `tools/generate_report.py`.

#### 2. Power of Hybrid Logic
*   **Markdown:** Reasoning ("Why/When").
*   **Script:** Execution ("How").

#### 3. Why better than Pure Prompts?
*   **Determinism:** Scripts do exactly what they are told.
*   **Math/Logic:** LLMs are bad at math; Python is good at math.

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To explain the "Neuro-Symbolic" nature of robust skills. Combining the fuzzy brain (LLM) with the precise hands (Scripts).

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Don't ask ChatGPT to do math. Ask it to write a script that does math.
*   **Advanced Insights:** **Hard-Coded Reliability.** If a regulation requires a specific formula, you code that formula in Python. You don't let the LLM "hallucinate" the formula. The LLM simply *calls* the function.

#### 3. Examples
*   **Basic:** A script that returns the current date (`datetime.now()`).
*   **Intermediate:** A script that connects to the company LDAP to look up a user's manager.
*   **PhD / Advanced:** **Local Model Invocation.** A script that calls *another* smaller, specialized AI model (e.g., a local OCR model) to process an image and return text to the main agent.

#### 4. Implementation in Agentic AI
*   **Shebang:** `#!/usr/bin/env python3`.
*   **Interface:** CLI arguments (`sys.argv`) and Stdout (`print`).

#### 5. Why This Matters?
*   **Trust:** You can audit the script line-by-line. You can't audit a neural network.
*   **Performance:** Scripts run in milliseconds.

#### 6. Architecture Deep Dive
*   **Tool Definition:** The `SKILL.md` defines the "Schema" of the script (Input/Output) so the Agent knows how to call it.

#### 7. Reflection Questions
*   *What parts of your workflow require 100% precision? Are those in Scripts or Prompts?*