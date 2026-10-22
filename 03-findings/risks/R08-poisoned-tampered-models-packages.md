# R08 - Poisoned or tampered models, data and AI packages

**Score: 10 (High)** - Likelihood 2 x Impact 5 | **Owner:** IT Security / Engineering Lead | **Stages:** Make, Plan, Enable

**Scenario.** An engineer downloads an open-source model from a public model hub for an in-house parts-classification or visual quality-inspection tool, plus several Python packages. The model file uses an unsafe serialization format that runs code when loaded, or a typosquatted package steals credentials. In another variant, the defect-detection training images are poisoned so a specific defect passes inspection. Or a vendor's own update channel is compromised upstream.

**Why it matters.** Code execution inside the network, or silent quality failures that reach customers. Real-world analog (not AI): in the SolarWinds Orion compromise, a trusted vendor update channel delivered malicious code, and CISA ordered federal agencies to disconnect affected versions (Emergency Directive 21-01) [S14].

**Rating rationale.**

- Likelihood 2: Requires in-house model building or open-source model use, which is limited in a typical mid-size manufacturer today.
- Impact 5: Network compromise or defective product shipped to customers.

**Preventive controls**

- Approved sources only for models and packages, via a private package mirror.
- Model/package hash pinning and signed artifacts; verify at build and deploy.
- Prefer safe model formats (for example safetensors) over formats that can execute code on load; scan models and packages before use.
- AI bill of materials (AI-BOM) for every in-house AI system: model, version, source, training data sources.
- Access control and provenance records on training data.

**Detective controls**

- Integrity check of model artifacts at every deploy.
- Run each new model version against a held-back 'golden' test set, including known defect cases, before release.
- Dependency vulnerability alerts on AI code repositories.

**Corrective controls**

- Roll back to last known-good signed model; rebuild from trusted sources; incident response.

**Key risk indicators (KRIs)**

- % of in-house AI systems with a current AI-BOM.
- % of model artifacts verified by hash/signature at deploy (target: 100%).
- Packages pulled from unapproved sources.
- Golden-test-set pass rate per model release.

**Framework references:** AI RMF: MANAGE 3.2, MEASURE 2.7; ISO 42001: A.7.5, A.4.4, A.6.2.4; CSF 2.0: ID.RA-09, PR.PS-06, ID.AM-08; SP 800-161r1: SR-3, SR-4, SR-11, CM-14; OWASP LLM: LLM03, LLM04

Source IDs like [S6] refer to the [sources list](../../sources.md).

---
[Back to project README](../../README.md) | [Risk register](../risk-register.md)
