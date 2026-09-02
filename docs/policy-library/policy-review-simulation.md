# GRC Policy Review Simulation: Access Control Policy

**Document ID Under Review:** `POL-001` (Access Control Policy)  
**Reviewer:** Senior GRC Auditor & Lead Risk Analyst  
**Review Date:** August 26, 2026  
**Target Standard:** ISO/IEC 27001:2022 (A.9 / A.5), NIST SP 800-53 (AC Family), & UAE Data Protection Law (PDPL)  

---

## 1. Executive Summary & Review Verdict
**Verdict:** **Approve with Changes**

### Explanation of Verdict
The Access Control Policy (`POL-001`) establishes a solid foundational framework for identity governance, multi-factor authentication, and privilege management. However, our rigorous policy review identified eight (8) critical observations ranging from obsolete password rotation mandates (conflicting with modern NIST SP 800-63B standards) to missing automated access provisioning workflows for cloud workloads and vague third-party vendor access controls. 

Because the foundational principles and scope are robust, outright rejection is unnecessary. Instead, approving the policy conditional upon the mandatory implementation of the eight corrective recommendations will ensure full alignment with ISO/IEC 27001, NCA ECC, and UAE PDPL mandates before the final executive sign-off.

---

## 2. Review Observations & Action Matrix

### Observation 1: Outdated Password Rotation Mandates
* **Observation:** Section 4.2 mandates compulsory 90-day password expiration for all internal user accounts. This contradicts current NIST SP 800-63B guidance, which discourages periodic forced password rotation in favor of breach-detection screening and multi-factor authentication.
* **Risk:** Forces users to adopt predictable, weak password recycling patterns or write credentials down physically, increasing credential compromise susceptibility.
* **Recommendation:** Revise Section 4.2 to eliminate mandatory periodic expiration for standard passwords unless compromise is suspected, and mandate breached-credential monitoring and MFA enforcement instead.
* **Owner:** Identity and Access Management (IAM) Team Lead
* **Priority:** High
* **Required Evidence:** Updated policy draft reflecting NIST SP 800-63B alignment; Active Directory / Entra ID password policy configuration screenshot.

### Observation 2: Undefined Privileged Access Review Frequencies
* **Observation:** Section 6.1 requires "periodic review" of privileged accounts but fails to define a concrete calendar frequency (e.g., monthly vs. quarterly).
* **Risk:** Accumulation of orphan privileged accounts and excessive access creep over time, violating the principle of least privilege under ISO/IEC 27001 (A.9.2.5).
* **Recommendation:** Explicitly mandate monthly recertification for Domain Admins and Cloud Root credentials, and quarterly recertification for standard elevated system administrative rights.
* **Owner:** Information Security Governance Lead
* **Priority:** High
* **Required Evidence:** Updated Section 6.1 text with explicit recurrence schedules; signed quarterly access review attestation reports.

### Observation 3: Lack of Automated Provisioning / Deprovisioning SLAs for Contractors
* **Observation:** The policy lacks explicit time-bound Service Level Agreements (SLAs) for revoking physical and logical access upon the termination or contract expiration of third-party vendors.
* **Risk:** Delayed deprovisioning windows leave orphaned contractor accounts active post-termination, creating high-probability insider threat and unauthorized data access vectors.
* **Recommendation:** Enforce a strict SLA requiring immediate logical and physical access revocation within 2 hours of contract termination or employee departure.
* **Owner:** Human Resources & IT Service Desk Manager
* **Priority:** Critical
* **Required Evidence:** Updated HR-IT offboarding workflow runbook; automated identity management audit logs demonstrating 2-hour deprovisioning compliance.

### Observation 4: Absence of Break-Glass Account Monitoring Protocols
* **Observation:** While emergency "break-glass" administrative accounts are mentioned in Section 5.4, the policy omits mandatory real-time alerting and post-use auditing requirements.
* **Risk:** Unmonitored emergency accounts can be abused by threat actors or rogue insiders to bypass security controls without immediate detection or attribution.
* **Recommendation:** Mandate that all break-glass account activations trigger immediate automated SIEM paging to the SOC and require a mandatory post-incident audit review within 24 hours.
* **Owner:** Security Operations Center (SOC) Manager
* **Priority:** Critical
* **Required Evidence:** SIEM alerting rule configuration export; post-incident review ticket template for break-glass usage.

### Observation 5: Ambiguous Multi-Factor Authentication (MFA) Scope for Remote Work
* **Observation:** Section 3.3 mandates MFA for remote connections but does not explicitly specify phishing-resistant authentication methods (e.g., FIDO2 hardware keys or passkeys) for access to critical cloud management planes.
* **Risk:** Vulnerability to modern adversary-in-the-middle (AiTM) phishing kits that easily bypass standard SMS or push-notification OTPs.
* **Recommendation:** Update Section 3.3 to mandate phishing-resistant MFA (FIDO2 / WebAuthn) for all privileged users, sysadmins, and access to production cloud environments.
* **Owner:** Enterprise Architecture & Security Engineering
* **Priority:** Medium
* **Required Evidence:** Updated cloud authentication policy standard; Entra ID / Okta conditional access policy rules enforcing phishing-resistant methods.

### Observation 6: Unaddressed Biometric Data Storage & Privacy Controls
* **Observation:** Section 7 references physical access control via biometric readers (fingerprint and facial recognition) but fails to reference compliance with UAE PDPL regarding biometric data collection, encryption, and consent.
* **Risk:** Regulatory non-compliance penalties under the UAE Personal Data Protection Law (PDPL) regarding sensitive biometric data processing.
* **Recommendation:** Incorporate explicit reference to UAE PDPL requirements, mandating that biometric templates be stored strictly in hashed or encrypted mathematical vector formats rather than raw images.
* **Owner:** Data Protection Officer (DPO) & Physical Security Lead
* **Priority:** High
* **Required Evidence:** Biometric system architecture data flow diagram; DPO compliance assessment sign-off.

### Observation 7: Missing Service Account Hardening and Rotation Standards
* **Observation:** The policy provides comprehensive guidance for human user credentials but contains no specific controls or lifecycle management rules for non-human service accounts and API tokens.
* **Risk:** Hardcoded credentials and unrotated service account secrets embedded in application configuration files can be compromised and exploited for persistent lateral movement.
* **Recommendation:** Add a dedicated subsection (Section 8) governing service accounts, mandating automatic secret rotation every 90 days via enterprise secrets management vaults (e.g., Azure Key Vault / HashiCorp Vault).
* **Owner:** DevOps & Application Engineering Lead
* **Priority:** High
* **Required Evidence:** Secrets management vault integration audit report; automated credential rotation schedule logs.

### Observation 8: Incomplete Penalty and Disciplinary Enforcement Clause
* **Observation:** Section 10 outlines general policy governance but lacks an explicit statement regarding disciplinary consequences for intentional, unauthorized sharing of credentials or access bypass.
* **Risk:** Low deterrence against employee negligence or intentional policy violations due to the absence of clear administrative consequences.
* **Recommendation:** Insert a clear enforcement clause stating that deliberate or negligent violations of the Access Control Policy will result in formal disciplinary action up to and including termination of employment and legal prosecution where applicable.
* **Owner:** Chief Human Resources Officer & Legal Counsel
* **Priority:** Medium
* **Required Evidence:** Updated policy section with HR and Legal sign-off; employee handbook cross-reference link.

