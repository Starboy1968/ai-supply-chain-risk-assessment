# R06 - Forecast model drift and over-automation in planning

**Score: 12 (High)** - Likelihood 4 x Impact 3 | **Owner:** Director of Supply Chain Planning | **Stages:** Plan, Source, Make, Deliver

**Scenario.** The AI demand-forecasting module learned pre-change demand patterns. A major customer changes ordering behavior, a tariff shifts demand, or the vendor silently updates the model. Forecast error grows for weeks. Planners stopped reviewing forecasts because 'the system is usually right', and auto-replenishment keeps issuing purchase orders on the bad forecast. Result: stockouts on fast movers and excess stock on slow movers. Skills to plan manually have faded, so the fallback is weak.

**Why it matters.** Inventory is cash. Forecast errors amplify upstream to suppliers (the bullwhip effect), and loss of human expertise means the organization cannot step in when the model is wrong.

**Rating rationale.**

- Likelihood 4: Drift is expected for any forecasting model when conditions change; most organizations do not benchmark AI forecasts against a simple baseline.
- Impact 3: Margin, working-capital and service-level impact that is usually recoverable within weeks to a quarter.

**Preventive controls**

- Documented accuracy tolerance (for example forecast error and bias by product family) agreed with the business.
- Secondary forecast fallback: keep a simple statistical baseline running in parallel as benchmark and backup.
- Human review required for auto-generated POs above a value threshold or deviating more than X% from the prior period.
- Quarterly manual-planning drill so planners keep the skill.

**Detective controls**

- Weekly accuracy dashboard: AI forecast vs. baseline; alert when the AI underperforms the baseline for 3 consecutive weeks.
- Contract requirement for the vendor to notify model updates; compare accuracy before/after.

**Corrective controls**

- Manual override runbook: switch affected families to the baseline forecast, freeze auto-POs, recalibrate with the vendor.

**Key risk indicators (KRIs)**

- Forecast error and bias vs. baseline, by product family.
- % of auto-POs changed by planners (near 0% suggests rubber-stamping; very high suggests the model is not trusted).
- Stockout rate and excess-inventory value trend.
- Days since last manual-planning drill.

**Framework references:** AI RMF: MEASURE 2.4, MANAGE 4.1, MAP 3.5, GOVERN 3.2; ISO 42001: A.6.2.6, A.4.6; CSF 2.0: PR.IR-03, ID.IM-04; SP 800-161r1: SA-9

Source IDs like [S6] refer to the [sources list](../../sources.md).

---
[Back to project README](../../README.md) | [Risk register](../risk-register.md)
