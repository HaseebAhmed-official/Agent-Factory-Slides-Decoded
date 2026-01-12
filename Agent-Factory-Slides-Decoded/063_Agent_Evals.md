# Slide 63: Agent Evals (The "Exam")

## Core Message
**Testing Reasoning, Not Just Results**

### Detailed Analysis (Original Context)

#### 1. What are Evals?
A systematic way to measure performance.

#### 2. Components
*   **Golden Dataset:** 50 "perfect" examples.
*   **Semantic Similarity:** Checking if the meaning matches.
*   **Regression Testing:** Ensuring updates don't break old skills.
*   **Reasoning Checks:** Did it follow the right steps?

#### 3. The "Secret Sauce"
"You cannot sell a Digital FTE if you don't have an **Eval Suite** to prove it works."

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To bring QA (Quality Assurance) to AI.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Does it work?
*   **Advanced Insights:** **Model-Based Evals.** Using a "Teacher Model" (GPT-4) to grade the homework of a "Student Model" (Haiku). You prompt GPT-4: "Did the student follow the instructions? Rate 1-5." This allows automated grading of subjective tasks.

#### 3. Examples
*   **Basic:** `assert result == 42`.
*   **Intermediate:** `assert "succeeded" in response`.
*   **PhD / Advanced:** **Adversarial Evals.** An "Attacker Agent" tries to trick the "Worker Agent" into breaking policy. The Eval suite measures the Worker's resistance to attacks (Red Teaming).

#### 4. Implementation in Agentic AI
*   **Tools:** Promptfoo, LangSmith.

#### 5. Why This Matters?
*   **Confidence:** You can deploy on Friday if you have Evals.
*   **Sales:** You can show the client "99% Accuracy" on the datasheet.

#### 6. Architecture Deep Dive
*   **The CI Pipeline:** `git push` -> `run evals` -> `if score > 95%` -> `deploy`.

#### 7. Reflection Questions
*   *Do you have a 'Golden Dataset' for your problem?*