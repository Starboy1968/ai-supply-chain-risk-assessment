# R07 - Hallucinated, biased or unexplainable outputs in supplier selection

**Score: 12 (High)** - Likelihood 4 x Impact 3 | **Owner:** Director of Procurement | **Stages:** Source, Enable

**Scenario.** Procurement uses an AI tool to summarize supplier risk (financial health, news, sanctions) and to score bids. The tool invents a news story about a supplier's bankruptcy, misses a sanctions listing, or consistently scores new and small suppliers lower because its inputs favor incumbents. When a losing bidder disputes the result, nobody can explain why it scored 62 versus 71.

**Why it matters.** Wrong sourcing decisions, sanctions exposure, unfair treatment of suppliers, and failed audits because decisions are not explainable. OWASP lists misinformation (confident but false output) as LLM09 in its 2025 Top 10 [S6].

**Rating rationale.**

- Likelihood 4: False or unsupported statements are a known property of LLM output, and supplier research is a common early AI use case.
- Impact 3: Awards are usually reviewed before signing, limiting impact; a missed sanctions hit would be higher, which is why sanctions checks are pulled out as a hard control.

**Preventive controls**

- AI output is advisory only: every supplier award has a documented human decision and rationale.
- Every factual claim from the tool must carry a source link; sanctions and financial checks run against authoritative sources (official sanctions lists, credit reports), never the LLM.
- Scoring criteria and weights set by humans; the AI only gathers evidence.
- Twice-yearly bias test comparing scores across supplier segments (size, tenure, region).

**Detective controls**

- Monthly sample audit (for example 10%) of AI-assisted supplier assessments for factual errors.
- Track supplier disputes that cite scoring.

**Corrective controls**

- Correct and re-score; notify affected suppliers where a decision changed; suspend the tool if the audited error rate exceeds tolerance.

**Key risk indicators (KRIs)**

- Factual-error rate in sample audits.
- % of awards with documented human rationale (target: 100%).
- Average score gap between supplier segments.
- Supplier disputes citing AI-assisted scoring.

**Framework references:** AI RMF: MEASURE 2.9, MEASURE 2.11, MAP 3.5; ISO 42001: A.6.2.4, A.9.4; CSF 2.0: GV.SC-06, ID.RA-10; SP 800-161r1: SR-6; OWASP LLM: LLM09, LLM05

Source IDs like [S6] refer to the [sources list](../../sources.md).

---
[Back to project README](../../README.md) | [Risk register](../risk-register.md)
