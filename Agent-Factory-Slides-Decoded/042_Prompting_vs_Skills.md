# Slide 42: Manual Prompting vs. Agent Skills

## Core Message
**From Disposable Conversations to Reusable IP: The Assetization of AI Interaction**

### 1. Objective
To shift the mindset from "Chatting with AI" to "Engineering AI." This slide distinguishes between the ephemeral act of prompting and the durable act of building Skills.

### 2. Critical Analysis & Rationale
*   **The "Vibe" Economy:** Prompting is based on "Vibes." It's an art. It's hard to replicate.
*   **The "Asset" Economy:** Skills are based on "Files." They are assets. They can be versioned, sold, and licensed. A business cannot be built on vibes; it must be built on assets.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **Manual Prompting:** Typing into a chat box. Ephemeral. Lost when the window closes. High variability.
*   **Agent Skills:** Writing a `SKILL.md` file. Persistent. Saved in Git. Deterministic. High reproducibility.

#### b. Advanced Insights (Deeper Look)
*   **The "Prompt Engineering" Fallacy:** "Prompt Engineering" implies typing clever phrases. Real engineering involves **Version Control**, **Testing**, and **Deployment**. Skills enable true engineering practices for AI.
*   **Scalability of Expertise:** You can't clone your best prompt engineer. You *can* clone their Git repo. Skills allow you to "Copy/Paste" your best employee's brain.

### 4. When to Use?
*   **One-off:** Manual Prompting. (e.g., "Write a poem for my wife").
*   **Business Process:** Agent Skills. (e.g., "Write the Q3 Earnings Report").

### 5. Examples

#### a. Basic (The Fix)
*   *Prompt:* Typing "Fix this code" into ChatGPT.
*   *Skill:* Running `claude run refactor-skill` which applies a specific linting configuration.

#### b. Intermediate (The Best Practice)
*   *Prompt:* Copy-pasting your "Best Prompts" from a Google Doc.
*   *Skill:* A shared `prompts/` folder in the company repo that every developer's agent automatically accesses.

#### c. PhD / Advanced (Automated Optimization - DSPy)
*   *Concept:* **Self-Compiling Prompts.**
*   *Scenario:* You don't write the prompt manually. You write the "Goal" and a "Dataset." You use a framework like **DSPy** to mathematically optimize the instructions inside the `SKILL.md` file based on feedback metrics. The "Skill" writes itself to maximize performance.

### 6. Implementation in Agentic AI
*   **Artifact:** The repository *is* the product.
*   **Command:** `git commit -m "Updated skill logic"` vs "I typed a better prompt."

### 7. Why This Matters?
*   **Valuation:** Investors buy IP (Intellectual Property). A chat history is not IP. A repository of proprietary Skills is IP.
*   **Consistency:** Skills ensure Employee A and Employee B get the same AI output, regardless of their personal prompting ability.

### 8. What Problem Does It Solve?
*   **The "Key Person" Risk:** If your best prompter leaves, the capability stays in the `SKILL.md`.

### 9. Architecture Deep Dive
*   **Persistence Layer:** Git acts as the database for the Skills. The filesystem is the source of truth.

### 10. Common Practices & Pitfalls
*   **Pitfall:** Keeping "Golden Prompts" in a Notion doc.
    *   *Correction:* Move them to code immediately.
*   **Practice:** "Treat Prompts as Code." Lint them, test them, review them.

### 11. Reflection Questions
1.  *If you left your job today, would your AI expertise stay behind? (Only if it's a Skill).*
2.  *Is your company building 'Chat Logs' or 'Software Assets'?*
