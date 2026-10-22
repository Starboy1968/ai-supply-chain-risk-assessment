# R03 - Third-party AI vendor dependency and concentration (fourth-party risk)

**Score: 16 (High)** - Likelihood 4 x Impact 4 | **Owner:** Third-Party Risk Manager (with IT Vendor Management) | **Stages:** Plan, Deliver, Source, Enable

**Scenario.** The transportation management system's (TMS) route optimization and the ERP's AI forecasting both call the same upstream foundation-model provider, a 'fourth party' we have no contract with. That provider has a multi-hour outage during peak season, retires the model version with short notice, or changes model behavior. Load planning and order promising stall. The SaaS contracts cap liability at fees paid and say nothing about AI features.

**Why it matters.** Failures are correlated: several 'different' vendors fail at once because they share one hidden dependency, and we cannot see the fourth party's SLA. Real-world analog (not AI): on July 19, 2024 a faulty CrowdStrike update crashed an estimated 8.5 million Windows devices, showing how one vendor's change can hit many organizations at the same time [S12][S13].

**Rating rationale.**

- Likelihood 4: Supply chain SaaS vendors increasingly embed AI from a small number of model providers; outages, model retirements and behavior changes are a normal part of that market.
- Impact 4: Hours to days of degraded shipping and order processing with revenue and penalty impact; not rated 5 if a manual mode exists.

**Preventive controls**

- AI dependency inventory: business process -> SaaS product -> AI feature -> model provider -> hosting region.
- Contract clauses for critical AI vendors: 90-day notice of model-provider or sub-processor changes and model deprecations, SLA and service credits that cover AI features, right to switch AI features off and fall back to non-AI logic.
- Concentration check in third-party risk tiering: flag when two or more critical processes depend on the same fourth party.

**Detective controls**

- Subscribe to status pages of vendors and their disclosed model providers; route alerts to the IT on-call.
- Synthetic transaction monitoring on AI-dependent workflows (for example a test route plan every 15 minutes).

**Corrective controls**

- Tested manual-mode runbooks (route planning, order promising) exercised at least twice a year.
- Documented exit plan for each critical AI vendor (data export, alternative provider).

**Key risk indicators (KRIs)**

- Number of critical processes depending on a single model provider.
- % of critical AI vendors with a tested fallback.
- AI-feature downtime hours per quarter.
- Unannounced model or version changes by vendors per quarter.

**Framework references:** AI RMF: GOVERN 6.2, MANAGE 3.1, MAP 4.1; ISO 42001: A.10.2, A.10.3; CSF 2.0: GV.SC-04, GV.SC-07, GV.SC-08, GV.SC-10, DE.CM-06, PR.IR-03; SP 800-161r1: SR-8, SR-13, SA-9, CP-2; OWASP LLM: LLM03

Source IDs like [S6] refer to the [sources list](../../sources.md).

---
[Back to project README](../../README.md) | [Risk register](../risk-register.md)
