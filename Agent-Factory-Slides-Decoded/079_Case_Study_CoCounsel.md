# Slide 79: Case Study: CoCounsel (Legal AI)

## Core Message
**The $650 Million "Skill" Model: High-Value Expertise Packaging**

### 1. Objective
To show the "Unicorn" potential of the Agent Factory. CoCounsel is the ultimate proof that you don't need to invent the LLM; you just need to own the **Skill Layer**.

### 2. Critical Analysis & Rationale
*   **The "Expertise" Premium:** Lawyers bill at $500+/hour. This makes "Legal Labor" the highest-value target for automation.
*   **The Trust Wall:** CoCounsel didn't win because they had "Better AI." They won because they had **Better Guardrails** and **Verified Skills**.

### 3. Step-by-Step Explanation

#### a. Basic Insights
*   **The Story:** CoCounsel (by Casetext) built a "Digital Legal Assistant."
*   **The Tasks:** Document review, memo drafting, deposition prep.
*   **The Pricing:** **"Seat" model** (~$500/month per user).
*   **The Exit:** Acquired by Thomson Reuters for **$650 Million** in 2023.

#### b. Advanced Insights (Deeper Look)
*   **Vertical AI Advantage:** CoCounsel focused on one "Vertical" (Law) and went deep. They didn't try to be a "General Assistant." They built a "Legal Specialist."
*   **RAG over Case Law:** Their secret sauce wasn't the LLM (they used GPT-4). It was the **Context Layer**—their proprietary database of millions of law cases and the **Reasoning Skills** to analyze them accurately.
*   **The Citation Engine:** A critical "Skill" they built was the ability for the agent to **cite its sources**. In Law, an answer without a citation is a hallucination. They built a deterministic tool to verify every sentence against a real legal document.

#### 4. When to Use?
*   **Product Visioning:** When deciding whether to build a "General Tool" or a "Specialized Employee."
*   **Exit Strategy:** Explaining to investors how a "Wrapper" can be worth $600M+. (Answer: It's a **Skill Folder**, not a wrapper).

#### 5. Examples

##### a. Basic (The PDF Summarizer)
*   *Action:* User uploads a contract, AI says "It looks okay." (Low value).

##### b. Intermediate (The Policy Checker)
*   *Action:* AI checks the contract against 5 specific company policies. (Medium value).

##### c. PhD / Advanced (The Autonomous Litigator)
*   *Concept:* **Multi-Agent Legal Strategy.**
*   *Scenario:* A law firm receives 10,000 discovery documents. A "Lead Counsel Agent" spawns 50 "Reviewer Agents." Each reviewer identifies a specific type of evidence (e.g., "Mention of Price Fixing"). A "Synthesis Agent" takes those findings and drafts a 50-page "Motion to Dismiss," citing every relevant case in the last 20 years. The work of 100 junior associates done in 2 hours for $200 in tokens.

#### 6. Implementation in Agentic AI
*   **Pillar Focus:** Pillar 6 (Evals) and Pillar 8 (Composable Skills).

#### 7. Why This Matters?
*   **The "Logic" Moat:** CoCounsel proves that the "Moat" (competitive advantage) is in the **Instructions and Verification**, not the underlying model.

#### 8. What Problem Does It Solve?
*   **The "Document Overload" Problem:** Large-scale litigation is physically impossible for humans to read. Agents make it possible.

#### 9. Architecture Deep Dive
*   **The Verified RAG Pipeline:** `Query -> Vector Search -> Context Retrieval -> LLM Reasoning -> Deterministic Citation Check -> Output`.

#### 10. Common Practices & Pitfalls
*   **Pitfall:** Hallucinating a law.
    *   *Correction:* Use a **Deterministic Backend** (Slide 101) to verify every citation before showing it to the user.
*   **Practice:** "Zero-Data Retention." For legal clients, ensure the agent doesn't "Learn" from their sensitive data.

#### 11. Reflection Questions
1.  *Which high-value vertical (Law, Medicine, Finance) is ripe for a 'CoCounsel' equivalent?*
2.  *What is the 'Citation' equivalent in your industry? (How do you prove the agent is right?)*
3.  *Would you pay $500/mo for a digital employee that never makes a mistake?*
4.  *Are you building a 'Search Tool' or an 'Assistant'?*
