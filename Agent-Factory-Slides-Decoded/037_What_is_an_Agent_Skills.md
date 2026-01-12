# Slide 37: What are Agent Skills?

## Core Message
**Standardized, Modular Expertise Packages**

### Detailed Analysis (Original Context)

#### 1. Definition
> "An Agent Skill is a standardized, modular package that provides an AI agent with the specific procedures, logic, and tools it needs to perform a defined job role."

#### 2. Anatomy
*   **`SKILL.md` (The "Manual"):** High-level instructions.
*   **`PROMPTS/`:** Optimized system prompts.
*   **`TOOLS/`:** Scripts (Python, JS) for execution.
*   **`DOCS/`:** Reference material.

#### 3. Characteristics
*   **Modular:** Add/Remove easily.
*   **Standardized:** Common format (AgentSkills.io).
*   **Composable:** Load multiple skills (Coder + Auditor).

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To define the "Unit of Knowledge" in the Agent Factory. Skills are the *currency* of the new economy.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** A folder that teaches an agent how to do a job.
*   **Advanced Insights:** **Procedural vs. Declarative.** Skills combine Declarative knowledge (`DOCS`) with Procedural knowledge (`TOOLS` + `SKILL.md`). This mirrors how humans learn (Reading a book + Doing exercises).

#### 3. Examples
*   **Basic:** A "Greeting Skill" (Instructions on how to say hello).
*   **Intermediate:** An "SEO Skill" (Checklist for keyword density + Python script to check meta tags).
*   **PhD / Advanced:** A "Forensic Accounting Skill" (Complex logic trees for fraud detection, access to anomaly detection ML models via local scripts, and legal reference docs).

#### 4. Implementation in Agentic AI
*   **Format:** The industry is converging on `SKILL.md` as the entry point.

#### 5. Why This Matters?
*   **Asset Class:** You can *sell* a folder. You can *license* a folder. This is the "Product" of the Factory.
*   **Portability:** A folder works on your machine and on the cloud.

#### 6. Architecture Deep Dive
*   **The Loading Mechanism:** When an agent starts, it "mounts" these folders into its context window (Progressively).

#### 7. Reflection Questions
*   *Can you zip up your job description and email it to an agent? (That's what a Skill is).*