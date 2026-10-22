# Control framework mapping

Mapping is by ID only; see the Sources section for the documents. "-" means no direct mapping was claimed.

| Risk | NIST AI RMF 1.0 | ISO/IEC 42001 Annex A | NIST CSF 2.0 | NIST SP 800-161r1 | EU AI Act / law | OWASP LLM 2025 |
|---|---|---|---|---|---|---|
| R01 AI-enabled supplier impersonation and payment fraud | n/a (the AI is the attacker's tool) | n/a | PR.AT-02, PR.AA-03, DE.AE-02, GV.SC-05 | SR-6, AT-3 | - | - |
| R02 Sensitive data leakage through generative AI tools (incl. shadow AI) | GOVERN 1.6, MAP 4.1 | A.2.2, A.9.2 | PR.DS-02, PR.DS-10, PR.AT-01, ID.AM-02 | SR-3 | EU AI Act Art. 4; GDPR Art. 28 | LLM02 |
| R03 Third-party AI vendor dependency and concentration (fourth-party risk) | GOVERN 6.2, MANAGE 3.1, MAP 4.1 | A.10.2, A.10.3 | GV.SC-04, GV.SC-07, GV.SC-08, GV.SC-10, DE.CM-06, PR.IR-03 | SR-8, SR-13, SA-9, CP-2 | - | LLM03 |
| R04 Prompt injection against AI agents that read supplier content | MEASURE 2.7, MANAGE 2.4, MAP 3.5 | A.6.2.4, A.6.2.8 | PR.AA-03, DE.CM-09, ID.RA-09 | SA-4 | - | LLM01, LLM05, LLM06 |
| R05 Regulatory, privacy and contractual non-compliance | GOVERN 1.1, MAP 4.1 | A.5.2, A.5.4 | GV.OC-03, GV.SC-05 | SR-5 | EU AI Act Arts. 4, 26, 50; GDPR Arts. 28, 33, 35; CCPA; export controls | - |
| R06 Forecast model drift and over-automation in planning | MEASURE 2.4, MANAGE 4.1, MAP 3.5, GOVERN 3.2 | A.6.2.6, A.4.6 | PR.IR-03, ID.IM-04 | SA-9 | - | - |
| R07 Hallucinated, biased or unexplainable outputs in supplier selection | MEASURE 2.9, MEASURE 2.11, MAP 3.5 | A.6.2.4, A.9.4 | GV.SC-06, ID.RA-10 | SR-6 | - | LLM09, LLM05 |
| R08 Poisoned or tampered models, data and AI packages | MANAGE 3.2, MEASURE 2.7 | A.7.5, A.4.4, A.6.2.4 | ID.RA-09, PR.PS-06, ID.AM-08 | SR-3, SR-4, SR-11, CM-14 | - | LLM03, LLM04 |
| R09 Intellectual property exposure through AI vendor terms | GOVERN 6.1 | A.10.2, A.10.3 | GV.SC-05, GV.SC-06 | SR-5 | Trade-secret law; customer contracts | LLM02 |

**How to read the frameworks together**

- **NIST AI RMF** (Govern, Map, Measure, Manage) frames *what* AI risk management should achieve; GOVERN 6 and MANAGE 3 cover third-party AI [S1].
- **ISO/IEC 42001** turns that into a certifiable management system; Annex A.10 (A.10.2 allocating responsibilities, A.10.3 suppliers) is the third-party core [S16][S17].
- **NIST CSF 2.0 GV.SC** (GV.SC-01 to GV.SC-10) is the supply chain backbone: know and tier suppliers, contract requirements, due diligence, monitoring, incident coordination, and exit [S2].
- **NIST SP 800-161r1** supplies the control detail for C-SCRM (for example SR-3 supply chain controls, SR-4 provenance, SR-6 supplier assessments, SR-8 notification agreements, SR-11 component authenticity, SR-13 supplier inventory) [S15].
- **EU AI Act** sets legal duties; for most supply chain uses the live ones are AI literacy (Art. 4) and transparency (Art. 50), with deployer duties (Art. 26) for any high-risk use such as AI in hiring [S3][S18].
- **OWASP Top 10 for LLM Applications 2025** names the technical attack patterns for LLM-based tools and agents [S6].

Source IDs like [S6] refer to the [sources list](../sources.md).

---
[Back to project README](../README.md)
