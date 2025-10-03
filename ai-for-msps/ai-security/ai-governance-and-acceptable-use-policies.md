---
description: >-
  Complete AI governance framework including policy templates, shadow IT detection, staff training, and enforcement procedures for MSP environments.
---

# AI Governance & Acceptable Use Policies

MSPs need structured AI governance covering internal usage, client services, and shadow IT prevention. This guide provides policy templates, enforcement procedures, and training frameworks for responsible AI adoption.

### **Internal AI Acceptable Use Policy Template**

**Core Principles:**

| Policy Area              | Requirement                                                               | Decision Criteria                                                               |
| ------------------------ | ------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Data Confidentiality** | Treat all customer and company information as highly confidential         | Prohibit disclosing PII, confidential, or sensitive data to public AI platforms |
| **Accountability**       | Users retain full responsibility for all AI-generated outputs             | AI assists human judgment; never replaces critical thinking                     |
| **Transparency**         | AI-generated content must be acknowledged where it materially contributes | Outputs used in client documentation require review and attribution             |
| **Secure Usage**         | All AI interactions occur over secure, authenticated systems              | Only use approved enterprise AI systems for processing sensitive data           |

**Implementation Checklist:**

- [ ] All AI usage requires Infosec Committee approval
- [ ] Vendors reviewed according to Vendor Risk Management policy
- [ ] Staff training on data privacy and AI bias recognition completed
- [ ] Monitoring mechanisms for AI platform interactions established

### **Client AI Disclosure Framework**

**DPA Negotiation Requirements:**

| Clause Type        | Required Language                                                 | Risk Mitigation                          |
| ------------------ | ----------------------------------------------------------------- | ---------------------------------------- |
| **Data Usage**     | "MSP and client data SHALL NOT be used for vendor model training" | IP exposure and privacy violations       |
| **Data Residency** | Specify exact jurisdictions for data storage and processing       | GDPR/CCPA compliance violations          |
| **Subprocessors**  | Full disclosure of all subcontractors and processing chains       | Unauthorized data exposure               |
| **Audit Rights**   | Right to examine algorithmic decision-making and adherence        | Limited control over AI vendor ecosystem |

**Client Communication Protocol:**

- Help clients establish AI acceptable use policies
- Advise against inputting confidential information into public AI platforms
- Run AI tools through same due diligence as other SaaS applications
- Use enterprise-grade solutions with zero training/data localization features

---

### Internal and Client-Facing Policies

Without documented policies, staff or clients may adopt AI tools unsafely, leading to shadow IT and unmanaged risk.

- **Guardrails:** Create separate internal (staff) and client-facing (service) policies. Define roles, responsibilities, and escalation points for AI use.
- **Key terms:** _AI governance_, _acceptable use policy (AUP)_, _risk ownership_.

### Shadow AI Detection and Enforcement

**Detection Procedures:**

| Method                     | Tool/Technology                 | Enforcement Target                                  |
| -------------------------- | ------------------------------- | --------------------------------------------------- |
| **API/Domain Monitoring**  | DNS and web proxy monitoring    | Detect hits against known AI API/domain lists       |
| **SaaS Inventory**         | Auvik SaaS Management, Augmentt | Identify unauthorized shadow AI apps and plugins    |
| **Data Loss Prevention**   | DLP tools across endpoints      | Prevent sensitive data sharing via AI prompts       |
| **User Activity Tracking** | User behavior monitoring        | Pinpoint employees initiating unauthorized AI usage |

**Enforcement Actions:**

- [ ] Establish clear AI Acceptable Use Policies defining approved tools
- [ ] Provide secure, enterprise-grade AI alternatives to minimize shadow usage
- [ ] Implement least privilege access to restrict proprietary data exposure
- [ ] Define disciplinary consequences for policy violations

### Staff Training Framework

**AI Fundamentals and Governance:**

| Training Area   | Key Topics                                                           | Risk Mitigation Focus                                |
| --------------- | -------------------------------------------------------------------- | ---------------------------------------------------- |
| **AI Basics**   | Differentiate AI, ML, and automation; understand AI system lifecycle | Address myths about AI development and capabilities  |
| **Ethical Use** | Data privacy, security practices, AI bias recognition                | Ensure adherence to internal acceptable use policies |
| **Compliance**  | GDPR, HIPAA, and industry-specific AI requirements                   | Meet compliance when integrating AI into workflows   |

**Operational Training:**

| Area                     | Focus                                                   | MSP Application                                                  |
| ------------------------ | ------------------------------------------------------- | ---------------------------------------------------------------- |
| **Human-AI Loop**        | AI augments expertise, never replaces critical judgment | Humans must review AI triage results before high-impact actions  |
| **Prompt Engineering**   | Contextualizing inquiries and output refinement         | Train staff to elicit specific, accurate responses from AI tools |
| **Output Validation**    | Identifying hallucinations and validating results       | Staff must detect vague or overgeneralized AI responses          |
| **Client Communication** | Explaining AI benefits and insights to clients          | Effective communication during Quarterly Business Reviews        |

### Defining Augmentation vs Automation

Not all AI tasks are equal. Some augment human work, others attempt full automation. Misclassification can create unsafe expectations.

- **Guardrails:** Classify each AI use case. Require human-in-the-loop for automation. State explicitly which functions AI may _suggest_ vs _execute_.
- **Key terms:** _augmentation_, _automation_, _HITL (human-in-the-loop)_.

### Training Staff and Clients

Staff and clients may lack awareness of AI risks, making them vulnerable to misuse or overtrusting outputs.

- **Guardrails:** Deliver regular training on responsible AI use, including safe prompting, data handling, and recognition of AI errors. Use simulations (e.g., phishing with AI-generated lures).
- **Key terms:** _responsible AI_, _prompt hygiene_, _AI-enhanced phishing_.

### Policy Enforcement

Policies are only effective if enforced consistently.

- **Guardrails:** Define consequences for policy violations (HR action, service restriction). Use audits to verify compliance with client AI agreements. Provide clear reporting channels for violations.
- **Key terms:** _policy enforcement_, _compliance audit_, _risk acceptance_.

---

### **Bottom Line**

Strong AI governance policies give MSPs control over how AI enters their environment. By defining boundaries, enforcing app approvals, training users, and auditing compliance, MSPs can reduce shadow IT and align AI adoption with security standards.

---
