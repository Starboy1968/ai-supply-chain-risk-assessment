# Background

## Why AI in the supply chain creates new risk now

Supply chain risk used to be about physical flows and the IT vendors behind them. AI changes the picture in four ways.

**1. AI arrives inside software you already bought.** ERP, TMS, WMS and procurement platforms ship AI features that call outside model providers. The company may have a contract with the SaaS vendor but none with the model provider underneath - a fourth party it cannot see or audit.

**2. Every employee now has a powerful external tool one browser tab away.** Contracts, BOMs and pricing can leave the company in a copy-paste, with no file transfer for traditional controls to catch. Samsung's 2023 restriction on generative AI after engineers uploaded source code to ChatGPT shows how quickly this happens inside a sophisticated company [S7][S8].

**3. AI agents read untrusted content and take actions.** An agent that reads supplier emails can be steered by instructions hidden in those emails. OWASP ranks prompt injection as the top risk for LLM applications in 2025 [S6].

**4. Attackers use AI too.** Deepfake voice and video undermine "call to confirm" habits. In the 2024 Arup case, an employee transferred HK$200 million after a video call with a deepfaked CFO [S9][S10][S11].

Older lessons still apply. SolarWinds showed that a trusted update channel can deliver malicious code [S14]. The 2024 CrowdStrike outage showed how one vendor's faulty change can disrupt millions of devices across many organizations at once [S12][S13]. Neither was an AI event, but AI model providers and model hubs create the same patterns: concentration, trusted updates, and limited visibility.

## Why regulators and customers care

- The **EU AI Act** applies in stages: AI literacy and prohibited practices from 2 February 2025, general-purpose AI model rules from 2 August 2025, national enforcement from 2 August 2026, and - after the 2026 "AI Omnibus" amendments - Annex III high-risk rules from 2 December 2027 and Annex I product rules from 2 August 2028 [S3][S4][S5].
- **NIST CSF 2.0** made supply chain risk management a Govern-level category (GV.SC) [S2], and the **NIST AI RMF** has a category specifically for third-party AI risk (GOVERN 6, MANAGE 3) [S1].
- Customers increasingly ask suppliers about AI use in security questionnaires; having a register and a mapping ready shortens those reviews.


Source IDs like [S6] refer to the [sources list](../sources.md).

---
[Back to project README](../README.md)
