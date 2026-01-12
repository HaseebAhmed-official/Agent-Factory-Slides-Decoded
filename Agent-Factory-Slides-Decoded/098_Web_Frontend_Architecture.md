# Slide 98: Web Frontend Architecture

## Core Message
**Technical Stack for the Dedicated App**

### 1. Objective
To provide a concrete "Starter Kit" for the web channel. This slide bridges the gap between the "Agent Backend" and the "Human User."

### 2. Critical Analysis & Rationale
*   **Streaming is Mandatory:** Agents are slow (thinking time). You must use "Streaming" (sending text as it generates) to keep the user engaged. A static loader feels broken.
*   **Generative UI:** The future of UI is not static buttons; it's UI generated on the fly by the agent to suit the context.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **Frontend:** Next.js (React). The industry standard.
*   **Interaction:** OpenAI ChatKit / Vercel AI SDK. Handles the streaming plumbing.
*   **Backend:** FastAPI (Python). The agent runtime.
*   **Logic:** Agent Skills & MCP.

#### b. Advanced Insights (Deeper Look)
*   **Generative UI:** Don't just show a chat bubble. Use Next.js to render "Components" based on the agent's output. (e.g., If the agent says "Here is the sales chart," the frontend renders a real `Recharts` component, not an image). This is **Real-Time Interface Generation**.
*   **Tool Call Visualization:** Show the user *what* the agent is doing ("Searching LinkedIn...", "Reading PDF..."). This builds trust and reduces perceived latency.

### 4. When to Use?
*   **Building the Web App:** This is your architecture diagram.
*   **UX Design:** Deciding how to display agent actions.

### 5. Examples

#### a. Basic (Text Chat)
*   *Action:* Simple ChatGPT clone.

#### b. Intermediate (Card UI)
*   *Action:* A chat that creates "Cards" for approvals (e.g., "Approve Refund"). The user clicks "Yes/No" on the card, which sends a payload back to the agent.

#### c. PhD / Advanced (Canvas-Based Autonomy)
*   *Concept:* **Shared Workspace (Co-Pilot Mode).**
*   *Scenario:* An interface like "v0.dev" or "Cursor" where the agent and user co-edit a shared workspace (Canvas). The Agent writes code on the right; the User previews it on the left. The Frontend isn't a "Chat," it's a **Shared State Editor**.

### 6. Implementation in Agentic AI
*   **Library:** `Vercel AI SDK` (`useChat`, `useCompletion`).
*   **Protocol:** Server-Sent Events (SSE).

### 7. Why This Matters?
*   **UX:** A custom frontend allows for a much better, richer user experience than a raw chatbot.
*   **Control:** You can inject your own branding and navigation.

### 8. What Problem Does It Solve?
*   **The "Wall of Text":** Breaks up text with interactive elements.

### 9. Architecture Deep Dive
*   **Streaming:** The backend yields chunks of data. The frontend hydrates the UI incrementally.

### 10. Common Practices & Pitfalls
*   **Pitfall:** Blocking the UI while the agent thinks.
    *   *Correction:* Always use async/non-blocking calls.
*   **Practice:** "Optimistic Updates." Show the user that the request was received immediately.

### 11. Reflection Questions
1.  *Is your UI helping the user, or just getting in the way?*
2.  *Can your agent render a button or a chart?*
