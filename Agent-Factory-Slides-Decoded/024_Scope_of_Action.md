# Slide 24: Authority Defines the Scope of Action

## Core Message
**Coding Agents vs. General Agents: Defining the Bounds**

### Detailed Analysis (Original Context)

#### 1. Comparison Table
| Feature | Coding Agent (e.g., Cursor) | General Agent (Claude Code) |
| :--- | :--- | :--- |
| **Scope** | Software development. | **Any business domain.** |
| **Identity** | Developer's pair programmer. | **Digital employee.** |
| **Habitat** | Embedded in developer tooling (IDE). | Operates across **system-level tools**. |
| **Built For** | Developers. | **Anyone solving problems.** |
| **Example Tasks** | "Write tests", "Refactor module". | "Plan your 2026", "Draft emails". |

#### 2. Detailed Analysis
*   **Habitat:** A Coding Agent lives in VS Code (Guest). A General Agent lives in the Terminal (Master).
*   **Identity:** Shift from helper (Pair Programmer) to worker (Digital Employee).

---

### Strategic Deep Dive (GEMINI.md Extensions)

#### 1. Objective
To clearly distinguish between the specialized "Coding Agent" (Cursor) and the generalized "General Agent" (Claude Code). Clarifying *where* they live and *what* they can touch.

#### 2. Step-by-Step Explanation
*   **Basic Insights:** Cursor = IDE/File scope. Claude Code = OS/Cloud scope.
*   **Advanced Insights:** **Permissions Boundary:** Coding Agents lack system permissions. General Agents *are* system wrappers. **Context Boundary:** Coding Agents see Code. General Agents see System State (processes, network).

#### 3. Examples
*   **Basic:** Cursor renames a variable. Claude Code refactors, tests, commits, and pushes.
*   **Intermediate:** Cursor cannot install Python. Claude Code checks for Python, installs via Homebrew, sets up venv.
*   **PhD / Advanced:** **Cross-System Orchestration.** Migration task (AWS to Azure). Claude Code uses AWS CLI to dump, SCP to transfer, Azure CLI to restore. A Coding Agent is helpless here.

#### 4. Implementation in Agentic AI
*   **Tool Access:** General Agent has `bash`, `curl`. Coding Agent has `insert_text`.

#### 5. Why This Matters?
*   **Tool Selection:** Don't use Cursor to manage infrastructure.
*   **Security:** General Agents are more dangerous (Shell access).

#### 6. Architecture Deep Dive
*   **Scope Hierarchy:** Line (Copilot) -> File (Cursor) -> Repo (Goose) -> System (Claude Code).

#### 7. Reflection Questions
*   *Does your agent live in the 'Editor' or the 'Terminal'?*
*   *Are you limited by the walls of your IDE?*