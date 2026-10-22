# R09 - Intellectual property exposure through AI vendor terms

**Score: 9 (Medium)** - Likelihood 3 x Impact 3 | **Owner:** General Counsel (with Engineering) | **Stages:** Make, Source, Enable

**Scenario.** Engineering uses a sanctioned AI design assistant and uploads CAD files and a proprietary coating formula. The vendor's default terms allow customer inputs to be used to improve its models and do not limit retention. Separately, AI-generated design changes and contract language have unclear ownership, and a customer contract requires us to protect the customer's drawings.

**Why it matters.** Trade secrets lose value once shared without protection; in the US, trade-secret protection generally depends on the owner taking reasonable measures to keep the information secret. Disputes over who owns AI-assisted designs are costly. This differs from R02: here the tool is approved but the contract terms are weak.

**Rating rationale.**

- Likelihood 3: Exposure depends on vendor terms: many enterprise plans exclude training, but defaults vary and terms change.
- Impact 3: Potential loss of exclusivity over specific designs or formulas, and legal cost; rated 3 because approved tools under enterprise terms limit exposure.

**Preventive controls**

- Contractual no-training clause, data-retention limit (for example 30 days or less) and deletion certification in every AI vendor DPA/MSA.
- Contract assigns ownership of inputs and outputs to the company; IP indemnity for outputs where available.
- 'Crown-jewel' data classes (formulas, CAD, customer drawings) allowed only in approved, tenant-isolated AI deployments.

**Detective controls**

- Track AI vendor terms-of-service and policy changes; annual terms review for each AI vendor.

**Corrective controls**

- Invoke contractual deletion rights; Legal assesses trade-secret and customer-contract impact.

**Key risk indicators (KRIs)**

- % of AI vendors with a signed no-training clause (target: 100%).
- AI vendor terms changes reviewed vs. detected.
- Crown-jewel files sent to AI tools outside the approved list.

**Framework references:** AI RMF: GOVERN 6.1; ISO 42001: A.10.2, A.10.3; CSF 2.0: GV.SC-05, GV.SC-06; SP 800-161r1: SR-5; Law: Trade-secret law; customer contracts; OWASP LLM: LLM02

Source IDs like [S6] refer to the [sources list](../../sources.md).

---
[Back to project README](../../README.md) | [Risk register](../risk-register.md)
