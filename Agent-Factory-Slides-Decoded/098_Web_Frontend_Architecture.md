# Slide 98: Web Frontend Architecture

## Core Message
**Technical Stack for the Dedicated App**

### Detailed Analysis (Original Context)

#### 1. The Tech Stack
*   **Frontend:** Next.js (React).
*   **Interaction:** OpenAI ChatKit / Vercel AI SDK.
*   **Backend:** FastAPI (Python).
*   **Logic:** Agent Skills & MCP.

#### 2. The Flow
`User Interface -> ChatKit -> FastAPI -> Agent Engine -> Tools`.

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To provide a concrete "Starter Kit" for the web channel.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Use modern, fast tools.
*   **Advanced Insights:** **Generative UI.** Don't just show a chat bubble. Use Next.js to render "Components" based on the agent's output. (e.g., If the agent says "Here is the sales chart," the frontend renders a real `Recharts` component, not an image). This is **Real-Time Interface Generation**.

#### 3. Examples
*   **Basic:** A text chat.
*   **Intermediate:** A chat with "Cards" for approvals.
*   **PhD / Advanced:** **Canvas-Based Autonomy.** An interface like "v0.dev" where the agent and user co-edit a shared workspace. The Frontend isn't a "Chat," it's a "Shared State Editor."

#### 4. Implementation in Agentic AI
*   **Library:** `Vercel AI SDK` for streaming and tool calls.

#### 5. Why This Matters?
*   **UX:** A custom frontend allows for a much better user experience than a raw chatbot.

#### 6. Architecture Deep Dive
*   **Streaming:** Using Server-Sent Events (SSE) to show the agent's "Reasoning" in real-time.

#### 7. Reflection Questions
*   *Is your UI helping the user, or just getting in the way?*