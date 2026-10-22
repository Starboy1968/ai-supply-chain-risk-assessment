# Third-party AI vendor due diligence questionnaire

Send to any vendor whose product uses AI on company data or in a critical process. Ask for evidence, not just yes/no.

| # | Question | What a good answer looks like | Risk(s) |
|---|---|---|---|
| 1 | Which AI features in your product are enabled for us, and can each be turned off without losing core functions? | A list of features, default state, and an admin switch | R03 |
| 2 | Which third-party model providers (fourth parties) power those features, and in which regions are our data processed? | Named providers and regions; sub-processor list | R03, R05 |
| 3 | Is any of our data (inputs, outputs, files, metadata) used to train or improve any model? Is that written in the contract? | No, by contract, including for your providers | R02, R09 |
| 4 | How long do you and your providers retain prompts, files and outputs, and can you certify deletion? | Defined retention (days, not "as needed"); deletion certificate on request | R02, R09 |
| 5 | How much notice do you give before changing or retiring the underlying model, and how do you test changes? | 90+ days for material changes; regression testing evidence | R03, R06 |
| 6 | What is the SLA for AI features, and what happens to our process when the AI is unavailable? | SLA covers AI; documented degraded mode | R03 |
| 7 | How do you protect against prompt injection and limit what AI agents can do in our environment? | Least privilege, human approval options, testing evidence | R04 |
| 8 | How do you verify the integrity and provenance of models, datasets and packages you use? | Signed artifacts, hash pinning, AI-BOM or equivalent | R08 |
| 9 | How do you monitor accuracy and drift, and will you share performance metrics with us? | Defined metrics, monitoring cadence, customer reporting | R06, R07 |
| 10 | Can you explain how an output or score was produced, and keep logs we can audit? | Explanation features; logs retained and exportable | R07 |
| 11 | Who owns inputs and outputs, and do you offer IP indemnity for outputs? | Customer owns inputs/outputs; indemnity terms | R09 |
| 12 | What AI governance certifications or attestations do you hold (for example ISO/IEC 42001, SOC 2 scope covering AI), and how do you assess your own EU AI Act obligations? | Current certificate or roadmap; AI in audit scope; named owner for AI Act | R05 |
| 13 | How fast will you notify us of an AI-related incident (data exposure, harmful output, model compromise)? | Defined notification window in the contract | R02, R04, R08 |


---
[Back to project README](../README.md)
