# Approach and scoring method

## Method

1. **Set context.** Defined the illustrative organization, its supply chain stages and its current AI uses (embedded, sanctioned, informal, and attacker-side).
2. **Identify risks.** Walked each stage and asked "what AI touches this, what data flows to it, who else is involved, what happens if it is wrong, down, or hostile?" Used the OWASP Top 10 for LLM Applications 2025 [S6], NIST AI RMF and its Generative AI Profile (NIST AI 600-1) [S1][S19], and NIST SP 800-161r1 [S15] as prompts.
3. **Merge and cut.** Combined overlapping risks (for example shadow AI into data leakage; over-automation into forecast drift) and dropped weak ones, leaving nine distinct, actionable risks.
4. **Score.** Rated likelihood and impact (1-5) with a one-line rationale for each, assuming **current state with no AI-specific controls** (inherent risk).
5. **Design controls.** For each risk: preventive, detective and corrective controls, a named owner role, and KRIs.
6. **Map to frameworks.** Mapped each risk to framework IDs only (no restated framework text). References were checked against the source documents listed in the Sources section.
7. **Prioritize.** Ordered by score (ties broken by higher impact) and built a 30/60/90-day plan.

## Rating scale

**Ratings are analyst judgment for a typical mid-size manufacturer/distributor using AI tools, not measured data.**

| Score | Likelihood (next 12 months) | Impact (worst credible outcome) |
|---|---|---|
| 1 | Rare - would need unusual circumstances | Minimal - absorbed in normal operations, no external effect |
| 2 | Unlikely - could happen, no signs it is | Minor - limited cost or delay, internal only |
| 3 | Possible - plausible; similar events seen in the industry | Moderate - noticeable cost, delay or customer impact; recoverable within weeks |
| 4 | Likely - expected to happen at least once without new controls | Major - significant financial loss, regulatory attention, or disruption of a key process for days |
| 5 | Almost certain - already happening or will happen | Severe - large or unrecoverable loss, enforcement action, loss of key customers, or extended shutdown |

**Risk score = Likelihood x Impact** (range 1-25).

| Band | Score | Expected response |
|---|---|---|
| Critical | 20-25 | Executive attention; treatment plan started within 30 days |
| High | 10-16 | Named owner; treatment within 90 days |
| Medium | 5-9 | Treat within normal planning cycle; monitor KRIs |
| Low | 1-4 | Accept and monitor |

## Supply chain stages used throughout

| Code | Stage | What it covers |
|---|---|---|
| PLAN | Plan | Demand forecasting, inventory and production planning |
| SOURCE | Source | Procurement, supplier selection, contracts, supplier management |
| MAKE | Make | Manufacturing, engineering, quality |
| DELIVER | Deliver | Logistics, transportation (TMS), warehousing (WMS) |
| RETURN | Return | Returns (RMA), warranty, after-sales service |
| ENABLE | Enable | Finance/accounts payable, legal and compliance, IT |

## Sources and frameworks

| Framework | Used for |
|---|---|
| NIST AI RMF 1.0 (AI 100-1) [S1] | AI risk functions: Govern, Map, Measure, Manage |
| ISO/IEC 42001:2023 [S16][S17] | AI management system controls (Annex A) |
| NIST CSF 2.0 [S2] | Cybersecurity outcomes, especially GV.SC supply chain risk management |
| NIST SP 800-161r1-upd1 [S15] | Cybersecurity supply chain risk management (C-SCRM) controls |
| EU AI Act [S3][S4][S18] | Legal obligations and timeline |
| OWASP Top 10 for LLM Applications 2025 [S6] | LLM-specific threats (prompt injection, poisoning, etc.) |


---
[Back to project README](../README.md)
