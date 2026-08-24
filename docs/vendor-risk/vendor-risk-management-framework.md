# Vendor Risk Management Framework

## Overview
This document outlines the enterprise Vendor Risk Management (VRM) framework. It establishes a repeatable, multi-stage lifecycle process for identifying, assessing, mitigating, and monitoring third-party risk across all supplier and cloud vendor relationships.

---

## 1. Vendor Identification
* **Objective:** Discover and catalog all third-party vendors and SaaS providers requesting access to corporate networks, systems, or sensitive data.
* **Key Considerations:** 
  * What services does the vendor provide?
  * What systems, APIs, or cloud tenants will the vendor access?
  * Who is the internal business sponsor or owner?

## 2. Inherent Risk Assessment
* **Objective:** Evaluate the baseline risk profile of the vendor before factoring in their security controls or mitigations.
* **Key Considerations:**
  * What risk exists before considering controls?
  * Data classification handled (e.g., PII, financial records, intellectual property, unclassified public data).
  * Scope of integration and network connectivity.

## 3. Due Diligence
* **Objective:** Collect documentation, compliance posture reports, and legal attestations to verify the vendor's reliability.
* **Key Considerations:**
  * What security/privacy information should you request?
  * Third-party certifications (e.g., ISO/IEC 27001, SOC 2 Type II, PCI-DSS).
  * Business continuity plans, incident response policies, and insurance coverage.

## 4. Control Assessment
* **Objective:** Examine the specific technical, physical, and administrative safeguards implemented by the vendor.
* **Key Considerations:**
  * What controls does the vendor have?
  * Access management, encryption standards (at rest and in transit), and multi-factor authentication (MFA) enforcement.
  * Vulnerability management and software patching cadence.

## 5. Evidence Review
* **Objective:** Validate vendor claims against actual artifacts and testing results.
* **Key Considerations:**
  * What documentation proves those controls?
  * Recent penetration test summaries, SOC 2 audit reports (with bridging letters if needed), and configuration review outputs.

## 6. Risk Rating
* **Objective:** Quantify and categorize the residual risk level based on the evaluation findings.
* **Scale:**
  * **Low:** Minor operational impact; no access to sensitive or regulated data.
  * **Medium:** Limited access to internal networks or non-critical data; robust compensating controls exist.
  * **High:** Direct access to core systems or customer PII; moderate security gaps identified.
  * **Critical:** Unrestricted access to production environments or critical infrastructure with unverified security controls.

## 7. Treatment
* **Objective:** Determine the operational strategy for handling identified risks.
* **Options:**
  * **Accept:** Acknowledge risk when within corporate risk appetite without further mitigation.
  * **Mitigate:** Require the vendor to remediate security gaps before contract signing or service activation.
  * **Transfer:** Shift financial or legal liability via cyber insurance, indemnification, or contractual guarantees.
  * **Avoid:** Terminate the vendor relationship if risks exceed acceptable governance thresholds.

## 8. Approval
* **Objective:** Establish clear accountability and sign-off authority for onboarding third parties.
* **Key Considerations:**
  * Who accepts the residual risk?
  * Formal sign-off required from the internal business owner, Information Security / CISO, and Legal / Compliance.

## 9. Contractual Requirements
* **Objective:** Embed enforceable security and compliance covenants into legal agreements.
* **Key Considerations:**
  * Security/privacy requirements in the contract.
  * Mandatory data breach notification timeframes (e.g., within 24–48 hours).
  * Data deletion/return clauses upon contract termination and compliance with applicable data residency laws.

## 10. Continuous Monitoring
* **Objective:** Maintain ongoing oversight throughout the vendor lifecycle.
* **Key Considerations:**
  * How often should the vendor be reassessed?
  * Annual reviews for Critical/High-risk vendors; biennial reviews for Medium/Low-risk vendors.
  * Continuous automated posture tracking and periodic review of incident history.

