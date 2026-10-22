# R02 - Sensitive data leakage through generative AI tools (incl. shadow AI)

**Score: 20 (Critical)** - Likelihood 5 x Impact 4 | **Owner:** CISO (with Procurement and Engineering leads) | **Stages:** Source, Make, Plan, Enable

**Scenario.** A buyer pastes a supplier contract with NDA-protected pricing into a free public chatbot to 'summarize the termination clauses'. An engineer uploads a bill of materials (BOM) and drawings to an unapproved AI tool to find alternate parts. A planner installs a browser AI extension that can read every ERP screen they open. None of these tools are in IT's inventory (shadow AI).

**Why it matters.** This can breach supplier NDAs and customer contracts, expose personal data, and give away pricing leverage. Under consumer terms, inputs may be retained or used to improve the service, and data cannot be pulled back. Real-world analog: in 2023 Samsung found engineers had uploaded sensitive source code and meeting notes to ChatGPT, and temporarily restricted generative AI on company devices [S7][S8].

**Rating rationale.**

- Likelihood 5: Free AI tools are one browser tab away and save real time; without a sanctioned alternative and technical blocks, this is close to certain to happen.
- Impact 4: Contract breach, competitive harm, and possible personal-data breach; not rated 5 because a typical single paste exposes a limited amount of data.

**Preventive controls**

- Provide an approved enterprise AI tool with a contractual no-training clause and data-retention limit, so staff have a safe option (blocking alone drives workarounds).
- AI acceptable-use policy with a one-page 'never paste' list: supplier pricing and contracts, BOMs/drawings, customer data, personal data, export-controlled data.
- Secure web gateway / CASB rule blocking unapproved generative-AI domains on company devices.
- DLP rule blocking paste/upload of files labeled Confidential, or matching patterns (contract numbers, part-number formats, price tables), to any generative-AI domain.
- Browser-extension allow-list enforced through endpoint management.

**Detective controls**

- Weekly CASB discovery report of generative-AI sites and apps in use, compared to the approved AI inventory.
- DLP alert triage for generative-AI destinations, with trend reporting to the risk committee.

**Corrective controls**

- AI data-exposure playbook: identify what was shared, request deletion from the provider, have Legal check NDA and breach-notification duties, coach the user.

**Key risk indicators (KRIs)**

- Unique users reaching unapproved generative-AI domains per week (should trend down).
- DLP blocks and alerts on generative-AI destinations per week.
- Unsanctioned AI tools discovered vs. tools in the approved inventory.
- % of staff who completed AI acceptable-use training.

**Framework references:** AI RMF: GOVERN 1.6, MAP 4.1; ISO 42001: A.2.2, A.9.2; CSF 2.0: PR.DS-02, PR.DS-10, PR.AT-01, ID.AM-02; SP 800-161r1: SR-3; Law: EU AI Act Art. 4; GDPR Art. 28; OWASP LLM: LLM02

Source IDs like [S6] refer to the [sources list](../../sources.md).

---
[Back to project README](../../README.md) | [Risk register](../risk-register.md)
