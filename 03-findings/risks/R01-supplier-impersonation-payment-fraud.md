# R01 - AI-enabled supplier impersonation and payment fraud

**Score: 20 (Critical)** - Likelihood 4 x Impact 5 | **Owner:** Controller / AP Manager (with CISO) | **Stages:** Source, Enable, Return

**Scenario.** An attacker uses a large language model (LLM) to write a flawless email from a known supplier's account manager, sent from a look-alike domain, announcing new bank details. When AP hesitates, a follow-up call uses a cloned voice of the supplier contact, or a video call with a deepfake of our own CFO 'approves' the change. AP updates the vendor master file and the next payment run sends money to the attacker.

**Why it matters.** This is direct and often unrecoverable cash loss, and the real supplier still has to be paid. Generative AI removes the typos and odd phrasing that staff were trained to spot, and voice/video are no longer proof of identity. Real-world analog: in 2024 engineering firm Arup confirmed that an employee in its Hong Kong office transferred HK$200 million (about US$25.6 million) after a video call with a deepfaked CFO and colleagues [S9][S10][S11].

**Rating rationale.**

- Likelihood 4: Supplier bank-change fraud already targets accounts payable routinely; AI makes it cheaper and more convincing, and a firm with ~400 suppliers sees bank changes regularly.
- Impact 5: A single fraudulent payment can be large and recovery is uncertain once funds move; supplier relationships are also damaged.

**Preventive controls**

- Vendor-master change rule: every bank-detail change is verified by a callback to the phone number already on file (never a number in the request), plus dual approval in the ERP.
- Written rule: no payment or bank change is approved on the strength of a voice or video call alone.
- Payment hold (for example 5 business days) on the first payment to any changed bank account.
- Bank-detail changes accepted only through the supplier portal with MFA, not by email.
- DMARC at p=reject on our own domains; look-alike domain monitoring for our brand and top suppliers.

**Detective controls**

- ERP alert when a vendor bank change is followed by a payment within 30 days.
- Bank account-name validation (where the bank offers it) before the first payment.
- Payment-run exception report listing new or recently changed payee accounts.

**Corrective controls**

- Payment-fraud runbook: call the bank's fraud desk for recall immediately, report to law enforcement (in the US, the FBI's IC3), notify the real supplier, preserve evidence.
- Confirm cyber/crime insurance covers social-engineering losses before you need it.

**Key risk indicators (KRIs)**

- % of bank-detail changes verified by callback to the number on file (target: 100%).
- Number of bank-change requests received by email instead of the portal.
- Look-alike domains detected per month.
- Payments released to accounts changed in the last 30 days.
- Phishing-simulation failure rate for AP and procurement staff.

**Framework references:** CSF 2.0: PR.AT-02, PR.AA-03, DE.AE-02, GV.SC-05; SP 800-161r1: SR-6, AT-3

Source IDs like [S6] refer to the [sources list](../../sources.md).

---
[Back to project README](../../README.md) | [Risk register](../risk-register.md)
