# R05 - Regulatory, privacy and contractual non-compliance

**Score: 12 (High)** - Likelihood 3 x Impact 4 | **Owner:** General Counsel / Privacy Officer (with Trade Compliance) | **Stages:** Enable, Source, Return, Make

**Scenario.** The company sells into the EU and holds personal data on supplier contacts and customers who return goods. AI tools are adopted without checking whether the vendor has a GDPR Article 28 processor agreement and a lawful transfer mechanism; whether any use is high-risk under the EU AI Act (for example an AI tool used to screen warehouse job applicants, an Annex III employment use); whether staff AI-literacy measures exist (Article 4); whether export-controlled drawings are being sent to an AI service hosted abroad; or whether customer contracts forbid sharing their data with new sub-processors.

**Why it matters.** Fines, contract breaches and lost customer approvals. EU AI Act timing matters: AI literacy has applied since 2 February 2025 and national enforcement began 2 August 2026; after the 2026 'AI Omnibus' amendments, Annex III high-risk rules apply from 2 December 2027 [S3][S4][S5].

**Rating rationale.**

- Likelihood 3: The obligations are real, but most supply chain AI uses are not 'high-risk' under the AI Act; exposure concentrates in personal data, export control and contract terms.
- Impact 4: Regulatory penalties, mandatory notifications and possible loss of key customers or certifications.

**Preventive controls**

- AI use-case intake form with Legal/Privacy screening: DPIA trigger (GDPR Art. 35), AI Act classification, export-control flag, customer-contract check.
- AI vendor DPA with Art. 28 terms, sub-processor list, data residency and transfer mechanism.
- Export-controlled data labeled and blocked from external AI services by DLP.
- AI-literacy training with completion records for staff who use or oversee AI (EU AI Act Art. 4).

**Detective controls**

- Annual compliance review of the AI use-case register; quarterly check for new AI features switched on in existing SaaS.

**Corrective controls**

- Suspend a non-compliant use case; follow the breach-notification procedure (GDPR Art. 33: 72 hours to the authority where required).

**Key risk indicators (KRIs)**

- % of AI use cases with completed Legal/Privacy screening.
- AI vendors processing personal data without a signed DPA.
- Export-controlled files detected in AI-bound traffic.
- % of in-scope staff with AI-literacy training recorded.

**Framework references:** AI RMF: GOVERN 1.1, MAP 4.1; ISO 42001: A.5.2, A.5.4; CSF 2.0: GV.OC-03, GV.SC-05; SP 800-161r1: SR-5; Law: EU AI Act Arts. 4, 26, 50; GDPR Arts. 28, 33, 35; CCPA; export controls

Source IDs like [S6] refer to the [sources list](../../sources.md).

---
[Back to project README](../../README.md) | [Risk register](../risk-register.md)
