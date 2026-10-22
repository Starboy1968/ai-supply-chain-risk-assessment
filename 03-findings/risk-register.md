# Risk register

*Ratings are analyst judgment for an illustrative mid-size manufacturer/distributor, not measured data. Sources checked October 2026.*

Ordered by score, highest first (ties broken by higher impact). Scores are inherent risk (before AI-specific controls). Detail sheets: [`risks/`](risks/). CSV: [`risk-register.csv`](risk-register.csv).

## Summary

| Rank | ID | Risk | Stages | L | I | Score | Rating | Owner |
|---|---|---|---|---|---|---|---|---|
| 1 | R01 | AI-enabled supplier impersonation and payment fraud | Source, Enable, Return | 4 | 5 | 20 | **Critical** | Controller / AP Manager (with CISO) |
| 2 | R02 | Sensitive data leakage through generative AI tools (incl. shadow AI) | Source, Make, Plan, Enable | 5 | 4 | 20 | **Critical** | CISO (with Procurement and Engineering leads) |
| 3 | R03 | Third-party AI vendor dependency and concentration (fourth-party risk) | Plan, Deliver, Source, Enable | 4 | 4 | 16 | **High** | Third-Party Risk Manager (with IT Vendor Management) |
| 4 | R04 | Prompt injection against AI agents that read supplier content | Source, Enable, Deliver, Return | 3 | 5 | 15 | **High** | Application Owner (AP Automation) with Security Architecture |
| 5 | R05 | Regulatory, privacy and contractual non-compliance | Enable, Source, Return, Make | 3 | 4 | 12 | **High** | General Counsel / Privacy Officer (with Trade Compliance) |
| 6 | R06 | Forecast model drift and over-automation in planning | Plan, Source, Make, Deliver | 4 | 3 | 12 | **High** | Director of Supply Chain Planning |
| 7 | R07 | Hallucinated, biased or unexplainable outputs in supplier selection | Source, Enable | 4 | 3 | 12 | **High** | Director of Procurement |
| 8 | R08 | Poisoned or tampered models, data and AI packages | Make, Plan, Enable | 2 | 5 | 10 | **High** | IT Security / Engineering Lead |
| 9 | R09 | Intellectual property exposure through AI vendor terms | Make, Source, Enable | 3 | 3 | 9 | **Medium** | General Counsel (with Engineering) |

## Full register

| ID | Risk | Description / scenario | Affected stages | L | I | Score | Rating | Key controls / mitigations | Owner (role) | Framework references |
|---|---|---|---|---|---|---|---|---|---|---|
| R01 | AI-enabled supplier impersonation and payment fraud | Deepfake / AI-written impersonation leads AP to pay a fraudster | Source, Enable, Return | 4 | 5 | 20 | Critical | Callback to number on file + dual approval for bank changes; first-payment hold; portal-only changes with MFA; DMARC p=reject | Controller / AP Manager (with CISO) | CSF 2.0: PR.AT-02, PR.AA-03, DE.AE-02, GV.SC-05; SP 800-161r1: SR-6, AT-3 |
| R02 | Sensitive data leakage through generative AI tools (incl. shadow AI) | Staff paste contracts, pricing, BOMs into unapproved AI tools | Source, Make, Plan, Enable | 5 | 4 | 20 | Critical | Approved enterprise AI tool (no-training, retention limit); CASB block of unapproved genAI domains; DLP on paste/upload; extension allow-list | CISO (with Procurement and Engineering leads) | AI RMF: GOVERN 1.6, MAP 4.1; ISO 42001: A.2.2, A.9.2; CSF 2.0: PR.DS-02, PR.DS-10, PR.AT-01, ID.AM-02; SP 800-161r1: SR-3; Law: EU AI Act Art. 4; GDPR Art. 28; OWASP LLM: LLM02 |
| R03 | Third-party AI vendor dependency and concentration (fourth-party risk) | Critical SaaS features depend on a few upstream model providers | Plan, Deliver, Source, Enable | 4 | 4 | 16 | High | AI dependency inventory incl. fourth parties; change/deprecation notice + AI-feature SLA in contracts; concentration flag; tested manual-mode runbooks | Third-Party Risk Manager (with IT Vendor Management) | AI RMF: GOVERN 6.2, MANAGE 3.1, MAP 4.1; ISO 42001: A.10.2, A.10.3; CSF 2.0: GV.SC-04, GV.SC-07, GV.SC-08, GV.SC-10, DE.CM-06, PR.IR-03; SP 800-161r1: SR-8, SR-13, SA-9, CP-2; OWASP LLM: LLM03 |
| R04 | Prompt injection against AI agents that read supplier content | Hidden instructions in supplier emails/documents hijack an AI agent | Source, Enable, Deliver, Return | 3 | 5 | 15 | High | Read-only agent, no payment-field writes; human approval on every write/send; hidden-text stripping; tool/recipient allow-list; red-team before go-live; kill switch | Application Owner (AP Automation) with Security Architecture | AI RMF: MEASURE 2.7, MANAGE 2.4, MAP 3.5; ISO 42001: A.6.2.4, A.6.2.8; CSF 2.0: PR.AA-03, DE.CM-09, ID.RA-09; SP 800-161r1: SA-4; OWASP LLM: LLM01, LLM05, LLM06 |
| R05 | Regulatory, privacy and contractual non-compliance | AI use breaches GDPR/CCPA, EU AI Act duties, export controls or customer contracts | Enable, Source, Return, Make | 3 | 4 | 12 | High | AI use-case intake with legal/privacy/export screening; Art. 28 DPA + transfer terms; DLP on export-controlled data; AI-literacy training records | General Counsel / Privacy Officer (with Trade Compliance) | AI RMF: GOVERN 1.1, MAP 4.1; ISO 42001: A.5.2, A.5.4; CSF 2.0: GV.OC-03, GV.SC-05; SP 800-161r1: SR-5; Law: EU AI Act Arts. 4, 26, 50; GDPR Arts. 28, 33, 35; CCPA; export controls |
| R06 | Forecast model drift and over-automation in planning | AI forecasts degrade quietly; planners no longer check; auto-POs follow | Plan, Source, Make, Deliver | 4 | 3 | 12 | High | Secondary forecast fallback + manual override runbook; accuracy tolerance with alerts; human review of large/abnormal auto-POs; planning drills | Director of Supply Chain Planning | AI RMF: MEASURE 2.4, MANAGE 4.1, MAP 3.5, GOVERN 3.2; ISO 42001: A.6.2.6, A.4.6; CSF 2.0: PR.IR-03, ID.IM-04; SP 800-161r1: SA-9 |
| R07 | Hallucinated, biased or unexplainable outputs in supplier selection | AI supplier summaries/scores contain errors or bias and cannot be explained | Source, Enable | 4 | 3 | 12 | High | Advisory-only AI with documented human rationale; source links required; sanctions checks against official lists; sample audits and bias tests | Director of Procurement | AI RMF: MEASURE 2.9, MEASURE 2.11, MAP 3.5; ISO 42001: A.6.2.4, A.9.4; CSF 2.0: GV.SC-06, ID.RA-10; SP 800-161r1: SR-6; OWASP LLM: LLM09, LLM05 |
| R08 | Poisoned or tampered models, data and AI packages | Malicious open-source model/package or poisoned training data enters the pipeline | Make, Plan, Enable | 2 | 5 | 10 | High | Model/package hash pinning and signed artifacts; private mirror; safe model formats + scanning; AI-BOM; golden test set before release | IT Security / Engineering Lead | AI RMF: MANAGE 3.2, MEASURE 2.7; ISO 42001: A.7.5, A.4.4, A.6.2.4; CSF 2.0: ID.RA-09, PR.PS-06, ID.AM-08; SP 800-161r1: SR-3, SR-4, SR-11, CM-14; OWASP LLM: LLM03, LLM04 |
| R09 | Intellectual property exposure through AI vendor terms | Approved AI vendors may train on or retain designs/terms; output ownership unclear | Make, Source, Enable | 3 | 3 | 9 | Medium | No-training clause + retention limit + deletion certification in AI vendor DPA; input/output IP ownership clause; crown-jewel data only in tenant-isolated AI | General Counsel (with Engineering) | AI RMF: GOVERN 6.1; ISO 42001: A.10.2, A.10.3; CSF 2.0: GV.SC-05, GV.SC-06; SP 800-161r1: SR-5; Law: Trade-secret law; customer contracts; OWASP LLM: LLM02 |

## Risk detail sheets

- [R01 - AI-enabled supplier impersonation and payment fraud](risks/R01-supplier-impersonation-payment-fraud.md)
- [R02 - Sensitive data leakage through generative AI tools (incl. shadow AI)](risks/R02-data-leakage-genai-shadow-ai.md)
- [R03 - Third-party AI vendor dependency and concentration (fourth-party risk)](risks/R03-ai-vendor-concentration-fourth-party.md)
- [R04 - Prompt injection against AI agents that read supplier content](risks/R04-prompt-injection-ai-agents.md)
- [R05 - Regulatory, privacy and contractual non-compliance](risks/R05-regulatory-privacy-contract-compliance.md)
- [R06 - Forecast model drift and over-automation in planning](risks/R06-forecast-model-drift-over-automation.md)
- [R07 - Hallucinated, biased or unexplainable outputs in supplier selection](risks/R07-hallucinated-biased-supplier-decisions.md)
- [R08 - Poisoned or tampered models, data and AI packages](risks/R08-poisoned-tampered-models-packages.md)
- [R09 - Intellectual property exposure through AI vendor terms](risks/R09-ip-exposure-ai-vendor-terms.md)

---
[Back to project README](../README.md)
