# Slide 31: The Workflow

## Core Message
**The Manufacturing Pipeline: Spec -> Builder -> Manufacturing -> Product**

### Detailed Analysis (Original Context)

#### 1. The 4-Step Pipeline
1.  **Spec (The Blueprint):**
    *   **Action:** Human expert writes a detailed specification in natural language (Markdown).
    *   **Content:** Defines persona, goals, constraints, and success criteria.
2.  **Builder (The Architect):**
    *   **Action:** A **General Agent** (Claude Code) reads the Spec.
    *   **Role:** Interprets requirements and plans technical implementation.
3.  **Manufacturing (The Production):**
    *   **Action:** The Builder generates code, scripts, and `SKILL.md` files.
    *   **Verification:** Agent runs tests (TDD) to ensure code matches Spec.
4.  **Production-Ready (The Product):**
    *   **Outcome:** A **Custom Agent or Skill** ready for enterprise deployment.

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To outline the standard operating procedure (SOP) for the Agent Factory. This slide transforms "Creativity" into "Manufacturing."

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Input = Idea (Spec). Machine = Agent (Builder). Output = Product (Skill).
*   **Advanced Insights:** **TDD Integration.** The "Manufacturing" step isn't just writing code; it's *verifying* it. The General Agent writes a test, fails it, writes code, passes it. **Recursive Improvement.** If the product fails validation, the Builder loops back to the Spec to ask for clarification.

#### 3. Examples
*   **Basic:** Spec: "Make a calculator." Builder: Writes `calc.py`. Product: Working calculator script.
*   **Intermediate:** Spec: "Make a Lead Scraper for LinkedIn." Builder: Identifies need for Selenium, writes scraper, adds error handling. Product: `scraper.py` + `instructions.md`.
*   **PhD / Advanced:** **Self-Healing Pipeline.** Spec: "Maintain 99.9% uptime on API." Builder: Deploys monitoring agent. Product: An agent that watches logs and *dynamically patches* the server code if it crashes.

#### 4. Implementation in Agentic AI
*   **Tooling:** `spec-kit-plus` (hypothetical or internal tool) -> `claude` -> `pytest`.

#### 5. Why This Matters?
*   **Reliability:** You move from "I hope it works" to "It passed the test suite."
*   **Scalability:** You can run this pipeline 100 times in parallel.

#### 6. Architecture Deep Dive
*   **The Pipeline:** `User Intent` -> `Spec File` -> `CI/CD for Agents` -> `Deploy`.

#### 7. Reflection Questions
*   *Do you have a written Spec before you start coding?*
*   *Are you testing your agents before deploying them?*
