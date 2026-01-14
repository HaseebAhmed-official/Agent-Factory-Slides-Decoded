# Deep Dive into the License Model

## Core Message
**In the world of Spec-Driven Development, the "License" isn't just for software—it's for the Skill Folder and Agents.**
*Selling the Blueprint: Scalability without Operational Overhead.*

The License model treats the **Skill Folder** (`SKILL.md` + `tools/`) as the product itself. Instead of hosting the service, you sell the **Intellectual Property (IP)** or the "Brain" of the agent to be run by others.

---

## 1. The Three License Types

### Type A: White-Label License
*   **What is being sold?** The right to **rebrand** your Agent Skill, MCP, or Agents as their own.
*   **The Mechanism:** You deliver the source code (Skill Folder) to an Agency or Value-Added Reseller (VAR). They change the name, logo, and pricing, and sell it to their clients.
*   **Revenue Style:** **High Upfront Fee + Royalty.**
    *   *Example:* You sell your "Dental Appointment Agent" to a Dental Marketing Agency for $20,000 + 10% of every subscription they sell.
*   **Strategic Value:** **Distribution Leverage.** You leverage someone else's existing sales force and client base.

### Type B: Enterprise Site License
*   **What is being sold?** The right to use a Skill, MCP, and Agents **unlimited times** across a whole organization.
*   **The Mechanism:** A large corporation downloads your Skill Folder and deploys it on their internal, secure infrastructure.
*   **Revenue Style:** **Annual Recurring Revenue (ARR).**
    *   *Example:* A hospital chain pays $150,000/year for your "HIPAA Compliance Checker" skill.
*   **Strategic Value:** **Security & Compliance.** This is the primary path for Defense, Healthcare, and Banking sectors.

### Type C: Developer License
*   **What is being sold?** The right to use your Skill and MCP as a **"sub-module"** in their own agents.
*   **The Mechanism:** Access to a private repository. Other developers `import` your skill into their complex agent projects.
*   **Revenue Style:** **Usage-based or Flat Tier.**
*   **Strategic Value:** **Ecosystem Building.** You become a utility provider for other AI builders.

---

## 2. Strategic Strategy: 1-to-1 vs. 1-to-Many

### The Direct Path (1-to-1 Sales)
*   **The Grind:** You sell directly to the end-user.
*   **The Burden:** You handle sales, support, and hosting.
*   **The Limit:** Scaling is linear. To get 1,000 customers, you need a sales team to talk to 1,000 people.

### The Leverage Path (1-to-Many Leverage)
*   **The Leverage:** You sell to a **Distributor** (e.g., a software provider already serving 50,000 customers).
*   **The Multiplier:** With one handshake, you gain access to their entire user base.
*   **The Freedom:** You focus purely on the IP (`SKILL.md`). The Partner handles the sales calls, Tier 1 Support, and Server Ops.

---

## 3. Technical Implementation Details

### How to Deliver a License?
A license in the Agent Factory is a technical delivery method:
1.  **The Container:** You package your `SKILL.md` and `tools.py` into a Docker container or a private MCP Server.
2.  **The Lock:** You include a license key verification script in the container startup logic.
3.  **The Update:** You provide a private registry endpoint where the client's system pulls updates automatically.

### "Zero-Knowledge" Skills
For high-value IP, techniques such as hosting the reasoning logic on a secure enclave can keep the "Secret Sauce" prompts hidden from the licensee while allowing them to run the agent locally.

---

## 4. Technical & Business Glossary

*   **ARR (Annual Recurring Revenue):** Predictable revenue expected every year. Site Licenses are typically multi-year contracts, providing high business valuation.
*   **White-Label:** A product produced by one company rebranded by another to appear as their own.
*   **VAR (Value-Added Reseller):** A company that adds features or services to an existing product before reselling it.
*   **Air-Gapped:** Systems physically isolated from the public internet for security. The License Model is often the only way to deploy in these environments.
*   **Sub-Module:** A smaller unit of logic that performs a specific task within a larger system.
