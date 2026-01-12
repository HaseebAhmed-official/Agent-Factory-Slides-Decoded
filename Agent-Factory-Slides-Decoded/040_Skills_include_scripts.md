# Slide 40: Skills can include scripts as tools

## Core Message
**Neuro-Symbolic Integration: Merging the 'Reasoning' of LLMs with the 'Precision' of Code**

### 1. Objective
To explain the "Hardware" of an Agent Skill. This slide teaches how to bridge the gap between "Talking about work" (Markdown) and "Doing the work" (Scripts).

### 2. Critical Analysis & Rationale
*   **LLMs are Probabilistic:** They might say 2+2=5 if the "vibe" is wrong.
*   **Scripts are Deterministic:** They *always* say 2+2=4.
*   **The Hybrid Advantage:** By including scripts *as tools* within a skill, we give the AI a "Calculator" and "Hands."

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **The Connection:** `SKILL.md` contains a sentence like: "Use the `./apply_template.py` script to update the file."
*   **The Script:** A Python or Bash file that does one specific technical task (e.g., formatting a PowerPoint, calling an API, running a SQL query).
*   **The Agent's Role:** The agent reads the instructions and decides *when* to execute the script.

#### b. Advanced Insights (Deeper Look)
*   **Actionable Documentation:** This is the birth of "Living Specs." The documentation doesn't just *describe* the process; it *contains* the code to execute the process.
*   **Schema Mapping:** The agent automatically infers the "Arguments" needed for the script based on the Markdown description. E.g., if the MD says "Pass the filename to the script," the agent handles the `sys.argv` mapping.
*   **Safe Execution:** Because the scripts are local to the Skill folder, the agent can run them in a restricted environment, providing a layer of security between the LLM and the OS.

### 4. When to Use?
*   **Data Processing:** CSV cleaning, Excel formatting, Image resizing.
*   **System Admin:** Creating users, checking logs, restarting services.
*   **Compliance:** Running a specific check that requires 100% accuracy.

### 5. Examples

#### a. Basic (The Formatter)
*   *Script:* `format_json.js`.
*   *MD:* "If the output is messy, run this script to beautify it."

#### b. Intermediate (The Jira Sync)
*   *Script:* `sync_tickets.py`.
*   *MD:* "When a task is marked 'Done' in the Spec, run this script to update Jira."

#### c. PhD / Advanced (The Self-Correcting Toolchain)
*   *Concept:* **Recursive Debugging.**
*   *Scenario:* A Skill includes a script `run_simulation.py`. The `SKILL.md` says: "Execute the simulation. If the script returns an error, read the traceback, edit the `config.json` file in this folder, and retry until success." The agent uses the **Script's failure** as a learning signal to rewrite the **Script's input**.

### 6. Implementation in Agentic AI
*   **Pattern:** "Script-as-Tool."
*   **Interface:**
    *   **Input:** CLI Arguments or JSON file.
    *   **Output:** Stdout (printed to console) which the agent reads back into context.

### 7. Why This Matters?
*   **Trust:** You can audit the Python script. You can't audit the LLM's weights.
*   **Efficiency:** Running a script uses 0 tokens. Asking an LLM to perform complex logic uses thousands of tokens.

### 8. What Problem Does It Solve?
*   **The "LLM Math" Problem:** Stops the agent from hallucinating calculations.
*   **The "Hallucinated Tool" Problem:** By providing local scripts, the agent doesn't try to "guess" if a tool exists; it sees it in the folder.

### 9. Architecture Deep Dive
*   **The Tool-Calling Loop:**
    1.  LLM outputs a special token: `CALL_TOOL: scripts/process.py --input data.txt`.
    2.  Agent Runtime (e.g., Claude Code) intercepts the token.
    3.  Runtime executes the Python process.
    4.  Result is appended to the Conversation History.

### 10. Common Practices & Pitfalls
*   **Pitfall:** Writing one giant script.
    *   *Correction:* Many small, specialized scripts are easier for the AI to understand and call.
*   **Practice:** Use `pip install` sparingly. Keep your Skill scripts "Zero-Dependency" whenever possible for maximum portability.

### 11. Reflection Questions
1.  *What part of your workflow is too important to leave to an LLM's 'vibe'?*
2.  *Can you replace a 1,000-word prompt with a 10-line Python script?*
3.  *How do you handle errors when a script fails?*
