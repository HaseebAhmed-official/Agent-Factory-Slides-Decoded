# Slide 58: SDD: Problem vs. Solution

## Core Message
**The Death of "Vibe Coding"**

### Detailed Analysis (Original Context)

#### 1. The Problem: "Vibe Coding"
*   **Ambiguity:** "Build me a login page."
*   **Hallucinations:** AI guesses details.
*   **Unpredictable:** Success depends on the prompt "vibe."

#### 2. The Solution: SDD
*   **Precision:** Detailed feature specs, schemas.
*   **Constraints:** AI follows the "Constitution."
*   **TDD:** Specs include test cases.
*   **Deterministic:** Success is defined by Spec criteria.

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To contrast the "Hobbyist" approach with the "Professional" approach.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Vibe Coding is fun but fragile. SDD is boring but robust.
*   **Advanced Insights:** **The "Vibe" Trap.** Vibe coding works for demos (80% complete). It fails for production (the last 20%). SDD handles the edge cases, error handling, and security that "Vibes" miss. It brings **Engineering Discipline** to AI generation.

#### 3. Examples
*   **Basic:** "Make it look cool." (Vibe).
*   **Intermediate:** "Use the color palette from `theme.json`." (Constraint).
*   **PhD / Advanced:** "Implement the 'Retry Pattern' with exponential backoff as defined in RFC 1234." (Engineering Spec).

#### 4. Implementation in Agentic AI
*   **Tool:** `spec-linter`. A tool that checks if your Spec is detailed enough *before* giving it to the Agent.

#### 5. Why This Matters?
*   **Reliability:** You cannot build a business on Vibes.
*   **Maintenance:** A Spec is documentation. A Vibe is lost the moment the chat closes.

#### 6. Architecture Deep Dive
*   **Validation Layer:** Spec -> Agent -> Code -> Test -> Result.

#### 7. Reflection Questions
*   *Are you 'Vibe Coding' your production app? (Stop it).*