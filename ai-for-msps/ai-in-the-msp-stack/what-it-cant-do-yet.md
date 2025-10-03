# What It Cant Do Yet

Critical limitations of AI in MSP environments, including liability risks, data boundaries, and failure modes requiring human oversight.

AI provides efficiency gains but has hard limits that create operational and legal risks. These constraints affect client relationships, staff competency, and business liability.

### **Technical Limitations**

**Hallucination (Confident Wrong Answers)**

* AI generates plausible-sounding but incorrect information
* **Example**: Suggests PowerShell commands that don't exist
* **Risk**: Technicians implement broken solutions without verification

**Context Boundaries**

* Generic models lack knowledge of your specific client environments
* **Example**: Suggests fixes for "Outlook issues" without knowing client's M365 configuration
* **Risk**: Generic advice doesn't match actual setup

### **Legal and Contractual Risks**

**Liability Shift ("The Liability Squeeze")**

* AI tool contracts frequently limit company liability to monthly subscription costs¹
* MSPs remain responsible for AI-caused client damage or data breaches
* **Example**: AI miscategorizes security incident, causing delayed response and client exposure

**Data Processing Exposure**

* 92% of AI companies claim rights to use customer data for training¹
* MSP client data could train competitor-accessible models
* **Risk**: Violates client confidentiality agreements

¹ [_Source: Stanford Law review of AI vendor contracts, 2024_](https://law.stanford.edu/2025/03/21/navigating-ai-vendor-contracts-and-the-future-of-law-a-guide-for-legal-tech-innovators/)

### **Operational Risks**

| Risk Type           | MSP Impact                                 | Mitigation Required                     |
| ------------------- | ------------------------------------------ | --------------------------------------- |
| **Skill Erosion**   | Technicians lose troubleshooting ability   | Maintain manual training programs       |
| **Over-Automation** | Critical tasks run without human review    | Implement human-in-the-loop checkpoints |
| **Vendor Lock-in**  | Proprietary AI becomes business dependency | Negotiate data portability clauses      |
| **Audit Gaps**      | No logging for AI decision making          | Require enterprise-grade audit trails   |

### **Client Impact**

**False Confidence in Security**

* AI threat detection systems generate false positives requiring manual verification
* MSPs may miss real threats while investigating AI-generated alerts
* Client expectations often exceed current AI capabilities

**Compliance Violations**

* AI processing may violate data residency requirements (varies by jurisdiction)
* GDPR Article 22 "right to explanation" may conflict with AI decision opacity
* Client audits increasingly include AI governance requirements

### Safety Checklist Before Enabling AI

* [x] Review the Data Processing Agreement (look for **no-training** guarantees)
* [x] Confirm liability limits in the contract — who pays if AI fails?
* [x] Identify which client data will be processed and where (data residency)
* [x] Establish rollback steps if AI guidance is wrong
* [x] Train staff to verify outputs and document misses
* [x] Maintain manual fallback workflows for critical services

**Key terms**: _hallucination_, _liability squeeze_, _data processing agreement_, _human-in-the-loop_, _false positive_.
