# Slide 80: The "Agent Factory" Roadmap
## From Concept to Revenue: Building Digital Full-Time Equivalents (FTEs)

This document decodes the 30-day action plan outlined in Slide 80, expanding on the core phases, technical architectures, and quality assurance strategies required to build and monetize "Digital FTEs."

---

## 1. Phase 1: Discovery & Definition (Day 1–7)
**Goal:** Identify the "Knowledge Gap" where high-volume manual work creates a scalable business opportunity.

### 1.1. Opportunity Scanning: The Selection Criteria
Not every task should be an agent. We select tasks based on two critical factors:
*   **High-Volume Requirement:**
    *   **The Threshold:** The task must occur frequently (e.g., >1,000 times/month or 50+ times/day).
    *   **Why it matters:**
        *   *ROI:* Automating a task that happens 5 times a month yields negligible savings. Automating 5,000 tasks yields massive margin.
        *   *Data for Evals:* High volume provides the historical data needed to create "Golden Datasets" for testing.
*   **High-Judgment Requirement:**
    *   The task must require "thinking" (reasoning), not just "doing" (scripting).
    *   *Examples:* Lead Qualification (requires nuance), Code Review (requires context), Legal Intake (requires compliance knowledge).
    *   *Contrast:* Moving data from Excel Column A to B is a script, not an Agent.

### 1.2. The Economic Calculation
*   **Cost-per-Task Analysis:**
    *   **Human Cost:** ~$3.00 - $6.00 per task (Salary / Volume).
    *   **Agent Cost:** ~$0.25 - $0.50 per task (Compute + API Tokens).
    *   **The "Pro-Tip":** This ~90% cost reduction is the primary sales driver for Enterprise adoption.

---

## 2. Phase 2: Specification & Manufacturing (Day 8–14)
**Goal:** Translate human intent into executable code using **Spec-Driven Development (SDD)**.

### 2.1. Draft the Spec (`SPEC.md`)
The "Spec" is the source code. It is a natural language document that defines:
*   **Identity:** Role definition (e.g., "Senior Forensic Accountant").
*   **Context:** Knowledge base access and documentation.
*   **Guardrails:** Deterministic rules ("Never approve >$500 without human check").
*   **Output Standard:** JSON schemas or specific reporting formats.

### 2.2. The Builder (General Agent)
*   **Tool:** **Claude Code** (or similar General Agents like Goose).
*   **Workflow:** The Read-Think-Code-Execute loop.
    1.  **Read:** Consumes `SPEC.md`.
    2.  **Think:** Plans the directory structure and scripts.
    3.  **Code:** Writes the implementation.
    4.  **Execute:** Runs initial tests.

### 2.3. The Output (The Asset)
*   **Agent Skill Folder:** A modular, portable directory containing:
    *   `SKILL.md`: The "Brain" (System Prompt/Reasoning instructions).
    *   `tools.py`: The "Hands" (Deterministic scripts for math, formatting, API calls).

---

## 3. Phase 3: Integration & Hardening (Day 15–21)
**Goal:** Connect the brain to the world and verify reliability through rigorous testing.

### 3.1. Connectivity (MCP)
*   **Model Context Protocol (MCP):** The universal standard ("USB-C for AI") connecting the Agent to live data systems (SQL, Slack, CRM) and local filesystems.
*   **Role:** Enables the agent to *fetch* live state and *push* updates, moving beyond simple chat.

### 3.2. Quality Assurance: Agent Evals (Deep Dive)
**Agent Evals** are the "Unit Tests" for AI reasoning. They solve the problem of testing probabilistic models.

#### A. The Architecture of an Eval ("The Exam")
1.  **The Golden Dataset (Ground Truth):**
    *   **Definition:** A benchmark set of 50–100 pairs of `Input` + `Ideal Output`.
    *   **Source:** Real-world historical data (e.g., 50 past invoices processed correctly by humans).
    *   **Requirement:** The agent *must* pass this exam before deployment.
2.  **The Execution Engine (The Student):**
    *   Runs the Agent/Skill against the dataset in a sandboxed environment (no live emails).
3.  **The Scorer (The Grader):**
    *   Calculates the quality of the Agent's response compared to the Ground Truth.

#### B. Scoring Metrics
*   **Exact Match (Syntactic):**
    *   Output must be identical character-for-character.
    *   *Use Case:* Extraction of Tax IDs, Dates, Phone Numbers.
*   **Semantic Similarity (Vector Embeddings):**
    *   **Embeddings:** Converting text into mathematical vectors (lists of numbers).
    *   **Cosine Similarity:** Measuring the distance between vectors.
    *   *Use Case:* "Vibe checking." If the agent says "Greetings" instead of "Hi," the meaning is preserved even if the words differ.
*   **LLM-as-a-Judge:**
    *   Using a superior model (e.g., GPT-4o) to grade a faster model (e.g., GPT-4o-mini).
    *   *Method:* Sending a prompt: "Rate the accuracy of Student A's answer compared to the Answer Key on a scale of 1-5."

#### C. Critical Workflows
*   **Regression Testing:** Running the Golden Dataset after *every* change to `SKILL.md`. If accuracy drops (e.g., 98% -> 94%), it's a "Regression" (Model Drift), and deployment is blocked.
*   **Hallucination Rate:** Testing specifically for fabricated facts not present in the source context.

---

## 4. Phase 4: Deployment & Scaling (Day 22–30)
**Goal:** Transition from a prototype in a terminal to a production business asset.

### 4.1. Production Runtime
*   **Tools:** **OpenAI Agents SDK** or **Claude Agent SDK**.
*   **Action:** Wrapping the prototype `SKILL.md` and scripts into a standalone service.
*   **Environment:** **Cloud Native Backbone** (Docker, Kubernetes, Serverless).
    *   **Always On:** Runs 24/7 (168 hours/week) vs human 40 hours.
    *   **Security:** SOC2/GDPR compliance, encrypted storage.
    *   **Interface:** Connected to user-facing apps (Next.js dashboard, Slack bot).

### 4.2. Scaling Mechanics (The Scaling Paradox)
*   **Instant Duplication:** To handle 10x volume, you do not hire 10x people. You simply increase compute resources.
*   **Linear Cost vs. Exponential Output:**
    *   *Human:* Hiring is slow, expensive, and linear.
    *   *Agent:* Scaling is instant and marginal costs decrease with volume.

### 4.3. Monetization Pillars
*   **Digital FTE:** Selling the "role" (e.g., "Digital SDR") on a monthly subscription, tapping into headcount budgets.
*   **License:** Selling the IP (the Skill Folder) to enterprises for on-premise use.

---

## 5. Summary of Technical Terms
*   **Spec-Driven Development (SDD):** Documentation *is* code.
*   **SKILL.md:** The portable "brain" of the agent.
*   **General Agent:** The Builder (Claude Code).
*   **Custom Agent:** The Product (SDK-based).
*   **Probabilistic vs. Deterministic:** The core challenge of AI engineering, solved by Evals.
