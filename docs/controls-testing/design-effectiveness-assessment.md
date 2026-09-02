# Enterprise GRC Control Design Effectiveness Assessment

**Document ID:** `DEA-001`  
**Version:** v2.0  
**Effective Date:** August 2026  
**Classification:** Confidential  
**Framework Alignment:** ISO/IEC 27001:2022, NIST SP 800-53 Rev. 5, UAE PDPL  

---

## 1. Executive Summary
This document provides a formal design effectiveness assessment for five core controls within the enterprise governance framework. Each control is evaluated against its targeted risk, control objective, architectural design, identified design weaknesses, formal assessment rating, and strategic remediation recommendations.

---

## 2. Detailed Design Effectiveness Assessments

### Control 1: Quarterly Privileged Access Review
* **Control ID:** `CTRL-003`
* **Control:** Quarterly privileged-access review workflow in Entra ID / Identity Governance.
* **Risk Addressed:** Inappropriate or orphaned privileged access leading to unauthorized administrative escalation, data exfiltration, or credential compromise.
* **Control Objective:** Ensure all administrative and privileged accounts are formally reviewed and recertified on a quarterly basis by designated asset owners, automatically revoking unverified permissions.
* **Control Design:** Automated quarterly workflow generates attestation tasks for privileged role assignees. Resource owners review access rosters and sign off; accounts lacking recertification within 14 days are disabled automatically.
* **Design Weakness:** The workflow previously omitted non-human service accounts (API keys/app registrations) from the automated reviewer queue, creating a blind spot for privileged machine identities.
* **Assessment:** **Partially Effective** (Design is sound for human accounts but exhibits a scope gap regarding non-human service identities).
* **Recommendation:** Expand the automated recertification scope to include non-human service accounts and API client secrets, requiring service owner attestation.

---

### Control 2: Multi-Factor Authentication (MFA) Enforcement
* **Control ID:** `CTRL-001`
* **Control:** Mandatory phishing-resistant Multi-Factor Authentication (MFA) for all user and administrative logins.
* **Risk Addressed:** Credential stuffing, brute-force attacks, and unauthorized account takeover resulting from compromised passwords.
* **Control Objective:** Prevent unauthorized access by enforcing cryptographic, phishing-resistant MFA (FIDO2 keys or authenticator push notifications with number matching) across 100% of enterprise authentication requests.
* **Control Design:** Conditional Access Policies enforced centrally via Microsoft Entra ID. Legacy authentication protocols (IMAP, POP3, SMTP basic auth) are globally blocked. Authentication requests failing MFA challenge are denied.
* **Design Weakness:** Emergency break-glass accounts were initially configured with standard TOTP app authenticator apps rather than isolated hardware FIDO2 keys and dedicated physical monitoring alerts.
* **Assessment:** **Effective** (The core architectural design successfully blocks credential-based threats, with break-glass configurations now remediated).
* **Recommendation:** Maintain continuous monitoring of Conditional Access policy exclusion lists and ensure break-glass FIDO2 keys are stored in a secure physical vault with real-time audit alerts.

---

### Control 3: Automated Offboarding & Account Deactivation
* **Control ID:** `CTRL-004`
* **Control:** Automated Joiner-Mover-Leaver (JML) provisioning integrated between HRIS and Active Directory.
* **Risk Addressed:** Retention of active access credentials by terminated employees or contractors, leading to insider threat or malicious data access.
* **Control Objective:** Immediately revoke all system access, disable user accounts, and revoke session tokens within 1 hour of formal HR offboarding submission.
* **Control Design:** HRIS webhook triggers an automated PowerShell script in Entra ID / Active Directory upon status change to 'Terminated', instantly revoking sessions and moving user objects to disabled OUs.
* **Design Weakness:** Manual exception processing existed for external third-party contractors whose terminations were logged via spreadsheets rather than direct HRIS feeds.
* **Assessment:** **Partially Effective** (Core HR automation is robust, but contractor offboarding relies on delayed manual intervention).
* **Recommendation:** Integrate contractor vendor management systems directly into the HRIS provisioning gateway to automate third-party lifecycle events.

---

### Control 4: Vendor Security Risk Assessment
* **Control ID:** `CTRL-011`
* **Control:** Pre-engagement and annual third-party risk assessment using standardized questionnaires (SIG/CAIQ).
* **Risk Addressed:** Supply chain compromise, data leakage, and regulatory non-compliance stemming from third-party vendor security deficiencies.
* **Control Objective:** Evaluate and verify that all third-party vendors handling enterprise data maintain adequate information security controls aligned with ISO 27001 standards.
* **Control Design:** Vendor Risk Manager distributes SIG Lite questionnaires, reviews SOC 2 Type II reports, and issues risk scoring prior to contract execution.
* **Design Weakness:** The assessment workflow lacked an automated tracking mechanism for recurring annual re-assessments, relying on manual calendar reminders which resulted in overdue reviews.
* **Assessment:** **Ineffective** (Lack of automated scheduling and enforcement renders the ongoing monitoring design unreliable).
* **Recommendation:** Implement an automated GRC vendor risk portal with automated re-assessment triggers, continuous risk scoring, and mandatory SLA gating.

---

### Control 5: Automated Backup & Integrity Verification
* **Control ID:** `CTRL-009`
* **Control:** Daily automated server backups with weekly immutability locks and monthly test restores.
* **Risk Addressed:** Data loss, ransomware encryption, and catastrophic system failure preventing business operations.
* **Control Objective:** Ensure all critical databases, virtual machines, and document repositories are securely backed up with verified recoverability in the event of a security incident.
* **Control Design:** Veeam backup jobs execute nightly to offsite immutable cloud storage, followed by automated verification checks and monthly isolated test restores.
* **Design Weakness:** Backup completion alerts were routed to a general IT alias rather than a dedicated 24/7 SOC paging queue, delaying response to failed backup jobs.
* **Assessment:** **Effective** (The technical backup architecture and immutability controls are robustly engineered).
* **Recommendation:** Route backup failure alerts directly into the SIEM and PagerDuty incident management pipeline with a 2-hour acknowledgement SLA.

