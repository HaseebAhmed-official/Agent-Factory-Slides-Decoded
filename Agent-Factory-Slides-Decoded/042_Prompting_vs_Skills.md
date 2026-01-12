# Slide 42: Manual Prompting vs. Agent Skills

## Core Message
**From Disposable Conversations to Reusable IP**

### Detailed Analysis (Original Context)

#### 1. Comparison Table
| Feature | Manual Prompting (Disposable) | Agent Skills (Reusable IP) |
| :--- | :--- | :--- |
| **Persistence** | Lost when chat ends. | Stored in **Git/File system**. |
| **Logic** | Probabilistic (Vibe). | **Deterministic** (Script). |
| **Scalability** | One-off. | **Mass-producible**. |
| **Auditability** | Hard to track. | **Version controlled**. |

#### 2. The "Aha!" Moment
"Prompting is a **conversation**. A Skill is an **Asset**. You cannot build a business on a conversation, but you can build a factory on Assets."

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To shift the mindset from "Chatting with AI" to "Engineering AI."

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Prompts are fleeting thoughts. Skills are written books.
*   **Advanced Insights:** **IP Valuation.** A company with 1,000 documented Skills has tangible IP. A company with employees who are "good at prompting" has volatile human capital. **Regression Testing.** You can test a Skill; you can't test a "vibe."

#### 3. Examples
*   **Basic:** Typing "Fix this code" vs. Running `claude run refactor-skill`.
*   **Intermediate:** Saving your best prompts in a Google Doc vs. Saving them in `prompts/` folder committed to GitHub.
*   **PhD / Advanced:** **Automated Optimization.** Using DSPy to *rewrite* the prompts inside the Skill folder based on performance metrics, effectively "compiling" the Skill for better results.

#### 4. Implementation in Agentic AI
*   **Artifact:** The repository *is* the product.

#### 5. Why This Matters?
*   **Business Value:** Investors buy Assets, not ephemeral interactions.
*   **Consistency:** Skills ensure Employee A and Employee B get the same AI output.

#### 6. Architecture Deep Dive
*   **Persistence Layer:** Git acts as the database for the Skills.

#### 7. Reflection Questions
*   *If you left your job today, would your AI expertise stay behind? (Only if it's a Skill).*