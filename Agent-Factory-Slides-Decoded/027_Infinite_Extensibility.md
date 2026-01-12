# Slide 27: Infinite Extensibility via MCP and Agent Skills

## Core Message
**Breaking the "Coder" Stereotype via Connectivity**

### Detailed Analysis (Original Context)

#### 1. The Enabler: MCP and Agent Skills
A General Agent isn't just a coder; it's a **Shape-Shifter**. Its role is defined by its "Hands" (MCP) and its "Knowledge" (Skills).

#### 2. Expanding the Role
*   **Slack MCP + Skill** -> Communications Manager.
*   **Salesforce MCP + Skill** -> RevOps Specialist.
*   **QuickBooks MCP + Skill** -> Financial Auditor.

#### 3. The Verdict
"A strictly defined 'Coding Agent' cannot send messages or audit finances. A General Agent can, provided you give it the right 'hands' (MCP) and 'procedures' (Agent Skill)."

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To explain how we turn a generic "Brain" (LLM) into a specialized "Expert" (Agent) without retraining. The combination of **MCP (Connectivity)** and **Skills (Knowledge)** allows infinite extensibility.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** LLMs are "Brains in a Jar." MCP plugs in tools; Skills plug in instructions.
*   **Advanced Insights:** **Decoupling.** We decouple Intelligence (LLM) from Capability (Code). **Dynamic Loading.** Hot-swap skills to change roles. **App Store Effect.** Ecosystems of MCP Servers and Skill Packs.

#### 3. Examples
*   **Basic:** File Reader (MCP) + Summarize Skill = Document Analyst.
*   **Intermediate:** GitHub + AWS + Slack MCPs + Deployment Skill = DevOps Bot.
*   **PhD / Advanced:** **Composable Agency.** An agent discovers and connects to 1,000 MCP servers in a registry to solve a novel task ("Plan a wedding"), downloading the "Wedding Planner Skill" on the fly.

#### 4. Implementation in Agentic AI
*   **Protocol:** JSON-RPC.
*   **Structure:** Client (Agent) <-> Server (Tool).

#### 5. Why This Matters?
*   **Standardization:** Plug-and-play integration.
*   **Scale:** Build a library of tools usable by any agent.

#### 6. Architecture Deep Dive
*   **MCP Architecture:** Hosts, Clients, Servers, Resources, Prompts, Tools.

#### 7. Reflection Questions
*   *Are you writing custom API wrappers or standard MCP servers?*
*   *What 'Skills' can you package?*