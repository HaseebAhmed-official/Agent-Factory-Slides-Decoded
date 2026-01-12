# Slide 22: Decision Matrix: How to Choose?

## Core Message
**A Strategic Framework for Architecture Selection**

### Detailed Analysis (Original Context)

#### 1. The Matrix
| Requirement | Choose General Agent (Claude Code, Goose) | Choose Custom Agent (OpenAI/Claude SDK) |
| :--- | :--- | :--- |
| **Task Type** | **Novel**, Problem-Solving. | **Repetitive**, Standardized. |
| **End User** | Developers / Technical Staff. | Non-Technical / Customers. |
| **Error Tolerance** | **High** (Human in the loop). | **Low** (Must be reliable). |
| **Cost Sensitivity** | Low (High value per task). | **High** (Volume optimization needed). |
| **Implementation** | **Instant** (Install & Run). | Weeks (Design & Build). |

#### 2. Detailed Breakdown
*   **Task Type:** Use General when you don't know the steps. Use Custom when you want to automate a known process.
*   **End User:** General agents are "Raw." Custom agents are "Polished."
*   **Cost:** General = High reasoning cost. Custom = Low cost at scale.

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To provide a definitive, logic-based framework for choosing between General and Custom Agents. Prevents "Architecture Mismatch."

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Axes: Novelty, User Technicality, Cost, Error Tolerance.
*   **Advanced Insights:** **The Lifecycle Theory.** Start with a General Agent to *discover* the process. Refactor into a Custom Agent for *scale*. **Cost Curve:** General = Linear cost scaling. Custom = Logarithmic cost scaling (high fixed, low marginal).

#### 3. Examples
*   **Basic:** Email. "Write to mom" (General). "Send 10k marketing emails" (Custom).
*   **Intermediate:** Coding. "Fix weird bug" (General). "Run linter" (Custom).
*   **PhD / Advanced:** **Hybrid Router (MoE).** A Master Gateway uses a classifier to route requests: Novelty > 0.8 -> General Agent; Novelty < 0.2 -> Custom Agent.

#### 4. Implementation in Agentic AI
*   **Router Pattern:** `if is_complex(task): claude.run() else: script.run()`.

#### 5. Why This Matters?
*   **Financial Health:** Using General Agents for everything bankrupts you.
*   **User Experience:** Using Custom Agents for novel tasks frustrates users.

#### 6. Architecture Deep Dive
*   **General:** Large Context, Chain-of-Thought.
*   **Custom:** Zero-shot, rigid tools.

#### 7. Reflection Questions
*   *Look at your last 10 AI tasks. Which quadrant do they fall in?*
*   *Are you 'over-serving' your users with expensive agents?*