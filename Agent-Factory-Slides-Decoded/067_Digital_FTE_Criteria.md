# Slide 67: What defines a Digital FTE?

## Core Message
**The Checklist for a Digital Employee**

### Detailed Analysis (Original Context)

#### 1. The Criteria
1.  **Defined Role:** Job title + responsibilities.
2.  **Uses Tools/APIs:** Interacts with systems.
3.  **Operates Continuously:** 24/7 monitoring.
4.  **Predictable Cost:** Fixed price vs. output.
5.  **Handles Ambiguity:** Figures out the "How."

#### 2. The Litmus Test
"If you can't describe it as a 'Job Role' on LinkedIn, it's not a Digital FTE."

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To distinguish "Software" from "Employees."

#### 2. Step-by-Step Explanation
*   **Basic Insights:** It acts like a person.
*   **Advanced Insights:** **Responsibility.** Software has features; Employees have *Responsibilities*. If the server crashes, software stops. An FTE tries to restart it or alerts a human. The "Sense of Duty" (programmed goal-seeking) is the differentiator.

#### 3. Examples
*   **Basic:** A script that runs once.
*   **Intermediate:** A Cron job that runs daily.
*   **PhD / Advanced:** **The Daemon Agent.** An agent that runs as a background process (`systemd`), monitors its own health, manages its own "vacation" (downtime for updates), and reports to a human manager weekly.

#### 4. Implementation in Agentic AI
*   **Code:** `while True: work()`.

#### 5. Why This Matters?
*   **Pricing:** You can't charge $2k/mo for a script. You can for an FTE.

#### 6. Architecture Deep Dive
*   **Keep-Alive:** Mechanisms to ensure the agent runs forever.

#### 7. Reflection Questions
*   *Does your agent wait for commands or seek work?*