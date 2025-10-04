---
description: >-
  This guide provides policy templates, enforcement procedures, and training
  frameworks for how MSPs and clients should define, document, and disclose AI
  use responsibly.
---

# Governance & Acceptable Use

### **Introduction**

Documented guardrails reduce shadow IT, clarify responsibilities, and prevent unsafe expectations. These core rules apply whether AI is used by staff, embedded in services, or adopted by clients.

***

#### **Internal and Client-Facing Policies**

* **Reality:** Without documented policies, staff or clients may adopt AI tools unsafely, leading to shadow IT and unmanaged risk.
* **Guardrails:**
  * Create separate internal (staff) and client-facing (service) policies
  * Define roles, responsibilities, and escalation points for AI use

#### Defining Augmentation vs Automation

* **Reality:** Not all AI tasks are equal. Some augment human work, others attempt full automation. Misclassification can create unsafe expectations.
* **Guardrails:**
  * Classify each AI use case
  * Require human-in-the-loop (HITL) for automation
  * State explicitly which functions AI may suggest vs execute

#### Training Staff and Clients

* **Reality:** Staff and clients may lack awareness of AI risks, making them vulnerable to misuse or overtrusting outputs.
* **Guardrails:**
  * Deliver regular training on responsible AI use
  * Include safe prompting, data handling, and error recognition
  * Use simulations (e.g., phishing with AI-generated lures)

#### Policy Enforcement

* **Reality:** Policies are only effective if enforced consistently.
* **Guardrails:**
  * Define consequences for policy violations (HR action, service restriction)
  * Audit compliance with client AI agreements
  * Provide clear reporting channels for violations

***

### Internal AI Acceptable Use Policy Template

Internal usage needs a defined baseline, or staff will improvise with AI tools in inconsistent ways.

<table><thead><tr><th width="192.9140625">Policy Area</th><th>Requirement</th><th>Decision Criteria</th></tr></thead><tbody><tr><td><strong>Data Confidentiality</strong></td><td>Treat all customer and company information as highly confidential</td><td>Prohibit disclosing PII, confidential, or sensitive data to public AI platforms</td></tr><tr><td><strong>Accountability</strong></td><td>Users retain full responsibility for all AI-generated outputs</td><td>AI assists human judgment; never replaces critical thinking</td></tr><tr><td><strong>Transparency</strong></td><td>AI-generated content must be acknowledged where it materially contributes</td><td>Outputs used in client documentation require review and attribution</td></tr><tr><td><strong>Secure Usage</strong></td><td>All AI interactions occur over secure, authenticated systems</td><td>Only use approved enterprise AI systems for processing sensitive data</td></tr></tbody></table>

**Internal AI AUP Checklist**

* [x] All AI usage requires Infosec Committee approval
* [x] Vendors reviewed under Vendor Risk Management policy
* [x] Staff trained on data privacy and AI bias recognition
* [x] Monitoring mechanisms for AI interactions established

***

### Client AI Disclosure Framework

#### **DPA Negotiation Summary**

MSPs should require vendors to ban training on client data, guarantee data residency, and disclose subprocessors with audit rights. These terms set the baseline for compliant AI adoption.

<table><thead><tr><th width="167.359375">Clause Type</th><th>Required Language</th><th>Risk Mitigation</th></tr></thead><tbody><tr><td><strong>Data Usage</strong></td><td>"MSP and client data SHALL NOT be used for vendor model training"</td><td>IP exposure and privacy violations</td></tr><tr><td><strong>Data Residency</strong></td><td>Specify exact jurisdictions for data storage and processing</td><td>GDPR/CCPA compliance violations</td></tr><tr><td><strong>Subprocessors</strong></td><td>Full disclosure of all subcontractors and processing chains</td><td>Unauthorized data exposure</td></tr><tr><td><strong>Audit Rights</strong></td><td>Right to examine algorithmic decision-making and adherence</td><td>Limited control over AI vendor ecosystem</td></tr></tbody></table>

#### **Client Communication Protocol**

Clients often experiment with AI without understanding the risks. Give practical guardrails for AI use, covering policy, data handling, and safe tool selection by:

* Helping clients establish their own AI acceptable use policies
* Advising against inputting confidential information into public AI platforms
* Running AI tools through the same due diligence as other SaaS apps
* Using solutions with no-training / data localization features



**Key terms:** _policy enforcement_, _compliance audit_, _risk acceptance,_ AI governance, acceptable use policy (AUP), risk ownership, _responsible AI_, _prompt hygiene_, _AI-enhanced phishing, augmentation_, _automation_, _HITL (human-in-the-loop)_.

***

### **Bottom Line**

Strong AI governance gives MSPs control over how AI enters their environment. Clear policies, consistent enforcement, and client communication reduce shadow IT and align AI adoption with security standards.

***
