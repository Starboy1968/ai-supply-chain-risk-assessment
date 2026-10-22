# Recommendations

## Prioritized recommendations

Recommendations are ordered by the risk they treat, highest first. Each names a specific control, not a general practice.

| Priority | Recommendation | Treats | Why first |
|---|---|---|---|
| 1 | **Harden supplier payment changes**: callback to the number on file, dual approval, first-payment hold, portal-only changes with MFA | R01 | Cheapest control against the highest-impact risk; no technology purchase needed |
| 2 | **Give staff a safe AI tool, then block the unsafe ones**: approved enterprise AI with no-training/retention terms; CASB block and DLP on generative-AI domains | R02, R09 | Leakage is near-certain today; blocking without an alternative drives workarounds |
| 3 | **Know your AI dependencies, including fourth parties**: inventory plus concentration flag in third-party tiering | R03 | You cannot plan fallback for a dependency you do not know about |
| 4 | **Put AI terms in critical contracts**: change/deprecation notice, AI-feature SLA, fallback right, no-training, retention limit, deletion certification, IP ownership | R03, R09 | Contracts are the main lever over vendors; renewals are the window |
| 5 | **Design AI agents for least privilege**: no payment-field writes, human approval on writes/sends, allow-lists, logging, kill switch, red-team before go-live | R04 | Cheaper to design in during the pilot than to retrofit |
| 6 | **AI use-case intake with legal screening** (privacy, AI Act class, export control, customer contracts) and AI-literacy records | R05 | Creates the evidence regulators and customers ask for |
| 7 | **Keep a human and a baseline in the loop for planning**: secondary forecast, accuracy tolerance alerts, override runbook, drills | R06 | Protects working capital and keeps expertise alive |
| 8 | **Advisory-only AI in sourcing**: human rationale, source links, sanctions checks against official lists, sample audits, bias tests | R07 | Makes decisions defensible to auditors and suppliers |
| 9 | **Secure the AI build pipeline**: approved sources, hash pinning, signed artifacts, safe formats, AI-BOM, golden test set | R08 | Low likelihood today, but cheap to set before in-house AI grows |

See the [30/60/90-day action plan](action-plan-30-60-90.md).

---
[Back to project README](../README.md)
