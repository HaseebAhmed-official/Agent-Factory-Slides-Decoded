# Slide 65: Deep Dive into the License Model

## Core Message
**In the world of Spec-Driven Development, the "License" isn't just for software—it's for the Skill Folder and Agents.**
*Selling the Blueprint: Scalability without Operational Overhead.*

This slide treats the **Skill Folder** (`SKILL.md` + `tools/`) as the product itself. Instead of hosting the service, you sell the **Intellectual Property (IP)** or the "Brain" of the agent.

---

## 1. The Three License Types

### Type A: White-Label License
*   **What is being sold?** The right to **rebrand** your Agent Skill, MCP, or Agents as their own.
*   **Revenue Style:** **High Upfront Fee + Royalty.**
*   **Target:** Marketing Agencies, Consultancies, Value-Added Resellers (VARs).
*   **Scenario:** You build a "Real Estate Lead Qualifier." An agency buys a White-Label license, renames it "RealtyBot 5000," puts their logo on it, and resells it to 1,000 real estate agents. You get a cut of every sale.

### Type B: Enterprise Site License
*   **What is being sold?** The right to use a Skill, MCP, and Agents **unlimited times** across a whole organization.
*   **Revenue Style:** **Annual Recurring Revenue (ARR).**
*   **Target:** Fortune 500s, Governments, Hospitals.
*   **Scenario:** A bank needs a "Fraud Detection Agent" but cannot use cloud AI due to security laws. They buy a Site License to download your Skill Folder and run it locally on their secure servers for 10,000 employees.

### Type C: Developer License
*   **What is being sold?** The right to use your Skill and MCP as a **"sub-module"** in their agents or SubAgent.
*   **Revenue Style:** **Usage-based or Flat Tier.**
*   **Target:** Other AI Engineers.
*   **Scenario:** You build a complex "PDF Table Extractor" skill. Other developers building "Accountant Agents" don't want to rebuild that hard part. They pay a monthly fee to `import` your skill into their agent.

---

## 2. Strategic Deep Dive: 1-to-1 vs. 1-to-Many

### The FTE Model (1-to-1 Sales)
*   **Dynamics:** You sell directly to the end-user (e.g., Dr. Smith).
*   **Burden:** You handle sales, support, and hosting.
*   **Growth:** Linear. To get 1,000 customers, you need to talk to 1,000 people.

### The License Model (1-to-Many Leverage)
*   **Dynamics:** You sell to a **Distributor** (e.g., "MediSoft Systems").
*   **Leverage:** MediSoft already has 50,000 doctors as customers. By licensing your skill to them, you instantly reach 50,000 users with **one deal**.
*   **Benefit:** You focus purely on the IP (`SKILL.md`). The Distributor handles the sales, support, and hosting headaches.

---

## 3. Technical & Business Glossary

### **ARR (Annual Recurring Revenue)**
The predictable revenue a business can expect every year from subscription-based customers.
*   *In Licensing:* A "Site License" is often sold as a multi-year contract (e.g., $50,000/year). This guarantees ARR, making the business more valuable to investors than one-time sales.

### **IP (Intellectual Property)**
Intangible property that is the result of creativity. In the Agent Factory, your **`SKILL.md`** (the prompt engineering and logic) and **`tools.py`** (the custom code) are your IP. The License Model monetizes this IP without requiring you to run the infrastructure.

### **White-Label**
A product or service produced by one company (you) that other companies (the agency) rebrand to make it appear as if they had made it. This allows you to stay "invisible" while leveraging the agency's brand trust and sales force.

### **Sub-Module / SubAgent**
In software architecture, a smaller unit of logic that performs a specific task within a larger system.
*   *Analogy:* If the "Accountant Agent" is the Car, the "PDF Reader Skill" is the Engine. You can license the Engine to many different Car manufacturers (Developer License).
