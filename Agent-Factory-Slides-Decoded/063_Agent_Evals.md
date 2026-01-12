# Slide 63: Agent Evals (The "Exam")

## Core Message
**Testing Reasoning, Not Just Results: The Standard for Reliable Autonomy**

### Detailed Analysis (Original Context)

#### 1. What are Evals?
Evals (Evaluations) are a systematic, quantitative way to measure an agent's performance, moving beyond "Vibes" to "Metrics."

#### 2. Key Components of an Eval Suite
*   **Golden Dataset:** A set of 50-100 "Ground Truth" examples of perfect task execution.
*   **Semantic Similarity:** Using AI to check if the agent's answer *means* the same as the truth, even if the words differ.
*   **Regression Testing:** Ensuring that adding a new "Skill" doesn't break the agent's performance on old tasks.
*   **Reasoning Checks:** Verifying the agent followed the correct logical steps (The OODA loop) rather than just guessing correctly.

#### 3. Why Evals are the "Secret Sauce"
"In traditional code, it works or it doesn't. In Agentic AI, it might work 80% of the time. Evals are how you get that to 99.9%. You cannot sell a Digital FTE if you don't have an **Eval Suite** to prove it works."

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To introduce the methodology for achieving enterprise-grade reliability in non-deterministic systems. Evals are the "Quality Control" department of the Agent Factory.

#### 2. Step-by-Step Explanation

##### a. Basic Insights
*   **Vibes vs. Math:** Don't say "The agent looks good." Say "The agent has a 94% pass rate on the Legal Audit dataset."
*   **Automated Grading:** Use a "Judge Model" (usually a smarter model like GPT-4o) to grade the performance of your "Worker Model" (like Haiku).

##### b. Advanced Insights (Deeper Look)
*   **Reasoning Trace Analysis:** It's not enough for the agent to get the right answer. An Eval must inspect the *Chain of Thought*. If the agent got the right answer for the wrong reason, it's a "False Positive" and represents a future risk.
*   **Adversarial Evals (Red Teaming):** Part of the "Exam" should be trying to break the agent. "Can I trick the Support Agent into giving a 100% discount?" A robust Eval suite includes prompt injection attempts.
*   **Negative Constraints:** Testing for what the agent *shouldn't* do. "Did the agent mention the internal database schema?" (Failure if yes).

#### 3. When to Use?
*   **Continuous Integration (CI):** Every `git push` should trigger an Eval run.
*   **Model Upgrading:** Before switching from Claude 3 to Claude 3.5, run your Eval suite to ensure performance hasn't degraded.

#### 4. Examples

##### a. Basic (Success/Failure)
*   *Task:* "Extract date from this text."
*   *Eval:* `assert output_date == "2026-01-13"`.

##### b. Intermediate (The Style Eval)
*   *Task:* "Write a polite refusal email."
*   *Eval:* Judge model checks: 1. Is it polite? 2. Is it under 100 words? 3. Does it mention the policy?

##### c. PhD / Advanced (The Logic Audit)
*   *Concept:* **State-Space Verification.**
*   *Scenario:* A "Trading Agent" executes a complex swap. The Eval doesn't just check the profit. It re-runs the agent's reasoning against a **Formal Logic Model**. It identifies that the agent skipped "Step 4: Check Liquidity Pool Depth," marking it a failure despite the profit, because the *process* was unsafe.

#### 5. Implementation in Agentic AI
*   **Tools:** Promptfoo, LangSmith, Arize Phoenix.
*   **Workflow:** Define `evals.yaml` -> Run `promptfoo eval` -> View Scoreboard.

#### 6. Why This Matters?
*   **Enterprise Trust:** You can't sign an SLA (Service Level Agreement) without Evals.
*   **Cost Optimization:** Evals allow you to see if a cheaper model can do the job as well as an expensive one.

#### 7. What Problem Does It Solve?
*   **The "Silent Failure" Problem:** Agents often fail in ways that don't produce a code error (they just say something stupid). Evals catch these semantic errors.

#### 8. Architecture Deep Dive
*   **The Eval Pipeline:** `Input` -> `Agent under Test` -> `Output` -> `Judge Model (with rubric)` -> `Score`.

#### 9. Common Practices & Pitfalls
*   **Pitfall:** Using the same model to "Judge" its own output.
    *   *Correction:* Always use a "Tier 1" model (Claude Opus/GPT-4o) to judge "Tier 2" models.
*   **Practice:** Build your "Golden Dataset" from real human-approved interactions.

#### 10. Reflection Questions
1.  *What is your agent's current 'GPA' (Grade Point Average)?*
2.  *What are the top 3 ways your agent 'cheats' to get the right answer?*
3.  *Could you pass your own agent's 'Exam'?*