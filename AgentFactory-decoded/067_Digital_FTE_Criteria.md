# Slide 67: What Defines a Digital FTE?

## Core Message
**A Digital FTE is an AI worker engineered for predictability and purpose.**
It is distinct from a chatbot. To qualify as a "Digital FTE," an agent must meet four specific criteria.

---

## 1. The Four Defining Characteristics

### 1. Defined Role
*   **Concept:** Specialization.
*   **Detail:** It is assigned a specific job function (e.g., "Junior Compliance Auditor") rather than being a generic assistant.
*   **Why:** Narrowing the scope reduces hallucinations and allows for clear performance metrics (KPIs) similar to a human job description.

### 2. Uses Tools & APIs
*   **Concept:** Agency (The ability to act).
*   **Detail:** It interacts with other systems and data sources to complete tasks. It doesn't just talk; it *does*.
*   **Technical Enabler:** **MCP (Model Context Protocol)**. This connects the agent to SQL databases, CRMs (Salesforce), and communication platforms (Slack).

### 3. Operates Continuously
*   **Concept:** Persistence.
*   **Detail:** It is designed for persistent, ongoing work, not just on-demand queries. It works 168 hours a week (24/7).
*   **Example:** An agent that wakes up every hour to check a folder for new PDF invoices, processes them, and goes back to sleep. It doesn't wait for a user to say "Process this."

### 4. Predictable Cost & Behavior
*   **Concept:** Engineering Standards.
*   **Detail:** Its operational parameters are controlled and measurable.
    *   **Behavior:** Enforced via **Guardrails** and **Specs** (Deterministic logic). It follows company policy perfectly.
    *   **Cost:** Predictable token usage allowing for fixed pricing.

---

## 2. Technical & Business Glossary

### **Predictability**
In AI engineering, this refers to the ability to trust the output. A "Creative" writer bot is low predictability. A "Digital FTE" must be high predictability (Deterministic). We achieve this by moving logic out of the LLM and into Python scripts (`tools.py`) wherever possible.

### **Agency**
The capacity of an AI system to take actions in the real world (e.g., sending an email, writing to a database) rather than just outputting text.

### **KPI (Key Performance Indicator)**
A measurable value that demonstrates how effectively a company is achieving key business objectives. For a Digital FTE, KPIs might be "Time to Response," "Accuracy Rate," or "Cost per Task."
