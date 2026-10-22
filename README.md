# AI Supply Chain Risk Assessment

**A completed GRC portfolio project: how AI tools change supply chain and third-party risk, and what to do about it in the first 90 days.**

For hiring managers and teams in GRC, third-party risk (TPRM) and supply chain risk.

## Summary

This project assesses the new risks that AI introduces across the supply chain of an illustrative mid-size manufacturer and distributor - from AI built into ERP and logistics software, to staff using public chatbots, to attackers using deepfakes. It identifies nine risks, scores each on likelihood and impact, assigns owners, designs specific controls and key risk indicators, maps everything to recognized frameworks, and ends with a 30/60/90-day plan and an AI vendor questionnaire.

> Ratings are analyst judgment for an illustrative mid-size manufacturer, not measured data.

## Objective

Find the AI-related supply chain risks a risk team should act on first, and turn them into owned, specific controls.

## Approach

- **Scope and stages:** walked six supply chain stages (plan, source, make, deliver, return, enabling functions) and the AI touching each one, including vendors' hidden model providers.
- **Scoring:** 1-5 likelihood x 1-5 impact with a written rationale for every rating; bands Low / Medium / High / Critical.
- **Controls and mapping:** preventive, detective and corrective controls plus KRIs per risk, mapped to NIST AI RMF, ISO/IEC 42001, NIST CSF 2.0, NIST SP 800-161r1, the EU AI Act and OWASP Top 10 for LLM Applications.

## Top findings

| ID | Risk | Score | Rating |
|---|---|---|---|
| R01 | AI-enabled supplier impersonation and payment fraud | 4 x 5 = **20** | Critical |
| R02 | Sensitive data leakage through generative AI tools (incl. shadow AI) | 5 x 4 = **20** | Critical |
| R03 | Third-party AI vendor dependency and concentration (fourth-party risk) | 4 x 4 = **16** | High |

All nine risks: [risk register](03-findings/risk-register.md) | [heat map](03-findings/heat-map.md)

## Key recommendations

1. **Verify every supplier bank-detail change** by calling the number already on file, with dual approval and a hold on the first payment.
2. **Give staff an approved AI tool** with no-training terms, then block unapproved AI sites and pasting of confidential data (DLP/CASB).
3. **Inventory AI dependencies, including vendors' model providers**, and add AI clauses to critical contracts: change notice, no-training, data-retention limits, fallback rights.

Full list: [recommendations](04-recommendations/recommendations.md) | [30/60/90-day plan](04-recommendations/action-plan-30-60-90.md)

## Skills demonstrated

- Risk identification across a supply chain, including fourth-party risk
- Likelihood/impact scoring with documented rationale
- Control design (preventive, detective, corrective) and key risk indicators
- Third-party risk: vendor due diligence questions and contract clauses
- Framework mapping: NIST AI RMF, ISO/IEC 42001, NIST CSF 2.0 (GV.SC), NIST SP 800-161r1, EU AI Act, OWASP LLM Top 10
- Writing for decision-makers: executive summary, heat map, prioritized plan

## Repo map

| Folder | What's inside |
|---|---|
| [01-project-brief](01-project-brief/project-brief.md) | Objective, questions, scope, organization profile, deliverables |
| [02-background-and-approach](02-background-and-approach/) | [Why this matters now](02-background-and-approach/background.md); [method and rating scale](02-background-and-approach/approach-and-scoring-method.md) |
| [03-findings](03-findings/) | [Risk register](03-findings/risk-register.md) ([CSV](03-findings/risk-register.csv)), [heat map](03-findings/heat-map.md), [one sheet per risk](03-findings/risks/) |
| [04-recommendations](04-recommendations/) | [Recommendations](04-recommendations/recommendations.md), [30/60/90 plan](04-recommendations/action-plan-30-60-90.md), [vendor questionnaire](04-recommendations/vendor-due-diligence-questionnaire.md), [framework mapping](04-recommendations/control-framework-mapping.md) |
| [05-deliverables](05-deliverables/) | Full report as Word and PDF |
| [glossary.md](glossary.md) / [sources.md](sources.md) | Plain-language terms; every source cited |

## Related projects

- [AI-Assisted Risk Analysis](https://github.com/Starboy1968/ai-assisted-risk-analysis): a reusable risk-analysis prompt and a worked example where an AI first draft is checked and corrected by a human reviewer.
- [Reading the Room: Power and Behavior Risk Indicators](https://github.com/Starboy1968/power-behavior-risk-indicators): observable signs of how power, incentives and group behavior shape risk decisions, and how to turn them into solid findings.
- [Behavioral Supply Chain Risk: Human Factors, AI, and Audit](https://github.com/Starboy1968/behavioral-supply-chain-risk-audit-ai): how bias and pressure create supply chain risk, and how AI triage, audit evidence and human review help catch it.
- [Playing the Risk Game: Game Theory for Supply Chain Risk and AI Governance](https://github.com/Starboy1968/supply-chain-ai-governance-strategy): plain-language game theory that explains why supply chain and AI risks persist, and which incentives to change.
- [AI in Supply Chain Operations: A Strategist's Field Guide](https://github.com/Starboy1968/ai-in-supply-chain-operations): how a supply chain manager can use AI in six everyday jobs, and what to check before trusting it.
- [Healthcare Cyber Risk Program: An OSINT Case Study](https://github.com/Starboy1968/healthcare-cyber-risk-osint-case-study): a cyber risk program for a fictional regional health system, built only from public sources.

## Author

Rashon Alsberry, supply chain and third-party risk analyst - [starboy1968.github.io](https://starboy1968.github.io)
