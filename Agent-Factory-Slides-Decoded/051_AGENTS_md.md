# Slide 51: AGENTS.md - The Project Constitution

## Core Message
**Universal Instructions for All Agents: One File to Rule Them All**

### 1. Objective
To solve the "Context Fragmentation" problem in multi-agent environments. `AGENTS.md` provides a centralized, human-readable, and machine-executable "Constitution" that ensures every AI worker (from different vendors or frameworks) follows the exact same project-specific rules, standards, and constraints.

### 2. Critical Analysis & Rationale
*   **The Onboarding Bottleneck:** Traditional onboarding for developers takes weeks. For AI agents, it must be instantaneous. `AGENTS.md` is the "Instant Onboarding" packet for the silicon workforce.
*   **Cross-Platform Consistency:** As organizations use multiple coding agents (Claude Code, Cursor, Copilot), they risk "Style Drift." `AGENTS.md` acts as the anchor, forcing consistent output regardless of the model's inherent biases.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **What is it?** A markdown file in the root directory that tells ANY AI agent how your project works.
*   **Who created it?** Initially championed by OpenAI, now an Agentic AI Foundation (AAIF) open standard.
*   **Universal Adoption:** Works with Claude Code, Codex, Goose, Cursor, Copilot, and custom SDKs.

#### b. Advanced Insights (Deeper Look)
*   **The Reference Pattern:** Using `@AGENTS.md` within agent-specific files (like `CLAUDE.md`) to include universal guidelines. This prevents **Instruction Duplication** and ensures a single source of truth for global rules while allowing for vendor-specific optimizations.
*   **Constraint Enforcement:** It's not just for "standards"; it's for "safety." You can define "Forbidden Zones" (e.g., "Do not modify files in `/security/` without a human review ticket").
*   **Environment Injection:** Modern AI coding environments (IDEs and CLIs) scan for this file on startup and inject its content into the "System Context," giving it higher priority than standard chat memory.

### 4. When to Use?
*   **Repository Setup:** Every new repository should start with an `AGENTS.md`.
*   **Multi-Contributor Projects:** When both humans and agents are modifying the same codebase.

### 5. Examples

#### a. Basic (The Style Guide)
*   *Content:* "Always use Tailwind CSS. Never use inline styles. Follow the Airbnb JavaScript Style Guide."

#### b. Intermediate (The Tech Stack)
*   *Content:* "Backend: FastAPI. DB: PostgreSQL. Auth: Auth0. All API endpoints must be documented in `openapi.json` before implementation."

#### c. PhD / Advanced (The Governance Model)
*   *Concept:* **Executable Project Policy.**
*   *Scenario:* The `AGENTS.md` defines a "Multi-Step Verification Protocol." It instructs agents that for any code change in the `core/` directory, they must: 1. Generate a unit test. 2. Run the test. 3. Scan for security vulnerabilities using a local script. 4. Record the reasoning in `DECISIONS.md`. Only then can they propose a PR.

### 6. Implementation in Agentic AI
*   **Placement:** `/root/AGENTS.md`.
*   **Structure:**
    *   `# Project Overview`
    *   `# Standards & Patterns`
    *   `# Forbidden Actions`
    *   `# Tooling & Commands`

### 7. Why This Matters?
*   **Velocity:** Zero-shot context for new agents.
*   **Accuracy:** Reduces hallucinations by providing grounded repo-specific truth.

### 8. What Problem Does It Solve?
*   **The "Grounding" Problem:** Agents often assume standard patterns that don't apply to your specific project. This file overrides those assumptions.

### 9. Architecture Deep Dive
*   **The Context Hierarchy:**
    1.  **Model System Prompt** (Generic).
    2.  **AGENTS.md** (Repo Constitution).
    3.  **SKILL.md** (Task Logic).
    4.  **User Prompt** (Task Intent).

### 10. Common Practices & Pitfalls
*   **Pitfall:** Writing too much fluff. Agents get distracted by long paragraphs.
    *   *Correction:* Use bullet points and strict imperatives ("Always", "Never", "Must").
*   **Practice:** "Auto-Update." Use a "Lead Architect Agent" to periodically update the `AGENTS.md` as the project architecture evolves.

### 11. Reflection Questions
1.  *If a robot joined your team today, what is the first thing it would break because it didn't know your rules?*
2.  *How do you handle rules that are specific to Claude but don't apply to Cursor?*