---
description: >-
  AI brings efficiency but has hard limits that create operational and legal
  risks. Misuse or overconfidence can damage client trust, reduce staff
  capability, and increase liability.
---

# What It Cant Do Yet

### Introduction

AI features in MSP tools are marketed as powerful, but their limits are real. These systems generate patterns, not certainty, and they lack context about individual client environments. Without safeguards, AI creates new risks: false confidence, broken processes, and legal exposure. This section outlines where AI fails today and how MSPs can mitigate those gaps.

***

### Technical Limitations

* **Hallucination (Confident Wrong Answers):** AI can generate plausible but incorrect guidance.\
  &#xNAN;_**Example:**_ Suggests PowerShell commands that don’t exist.\
  &#xNAN;_**Risk:**_ Techs may copy errors into production without verification.
* **Context Boundaries:** Generic models lack awareness of client-specific environments.\
  &#xNAN;_**Example:**_ Suggests a generic “Outlook fix” that conflicts with a client’s M365 setup.\
  &#xNAN;_**Risk:**_ Misaligned advice drives ticket volume higher.

***

### Client Impact

* **False Confidence in Security**\
  AI-based detection may over-alert or under-alert. While techs chase false positives, real threats can slip through.
* **Expectation Gap**\
  Clients may believe AI “fixes” issues automatically. In reality, it only suggests. Overselling creates liability when AI misses something.
* **Compliance Mismatch**\
  Some AI tools cannot provide legally required explanations for automated actions. Outputs may be valid technically but unacceptable contractually.

***

### Operational Risks

<table><thead><tr><th width="213.42578125">Risk</th><th width="250.1328125">Impact on MSP</th><th>Safeguard</th></tr></thead><tbody><tr><td><strong>Skill erosion</strong></td><td>Techs rely on AI instead of learning troubleshooting</td><td>Maintain manual training labs</td></tr><tr><td><strong>Over-automation</strong></td><td>AI runs unchecked, compounding errors</td><td>Keep human-in-the-loop checkpoints</td></tr><tr><td><strong>Vendor lock-in</strong></td><td>Proprietary AI becomes dependency</td><td>Negotiate portability rights</td></tr><tr><td><strong>Audit gaps</strong></td><td>AI decisions not logged</td><td>Require exportable audit trails</td></tr></tbody></table>

***

### Safety Checklist Before Enabling AI

* [x] Review the Data Processing Agreement (look for **no-training** guarantees)
* [x] Confirm liability limits in the contract — who pays if AI fails?
* [x] Identify which client data will be processed and where (data residency)
* [x] Establish rollback steps if AI guidance is wrong
* [x] Train staff to verify outputs and document misses
* [x] Maintain manual fallback workflows for critical services

**Key terms**: _hallucination_, _liability squeeze_, _data processing agreement_, _human-in-the-loop_, _false positive_.

***

#### Bottom Line

AI can augment MSP operations, but it cannot replace human oversight or compliance guardrails. The risks are operational as much as technical: hallucinations, blind spots, and expectation gaps must be managed deliberately.

👉 See [**Where We’re Going**](where-were-going/) for how these risks are evolving into regulatory and contract requirements.
