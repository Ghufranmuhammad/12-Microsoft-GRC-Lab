# Enterprise GRC Internal Audit Control Findings Register

**Document ID:** `FIND-REG-001`  
**Version:** v2.0  
**Effective Date:** August 2026  
**Classification:** Confidential  
**Framework Alignment:** ISO/IEC 27001:2022, NIST SP 800-53 Rev. 5, UAE PDPL  

---

## 1. Executive Summary
This document records formal internal control deficiencies, audit findings, root cause analyses, risk impact assessments, management remediation responses, accountable owners, and target due dates identified during the Q2–Q3 2026 internal controls testing cycle.

---

## 2. Detailed Findings Register

### Finding 1: Privileged Service Accounts Omitted from Quarterly Access Review Scope
* **Finding ID:** `FIND-2026-001`
* **Control:** Quarterly privileged-access review workflow (`CTRL-003`)
* **Criteria:** ISO/IEC 27001:2022 Control 9.2.5 (Review of Information Security Access Rights) mandates that all administrative and privileged access rights (including human and machine identities) must be periodically reviewed.
* **Condition:** During the Q2 2026 privileged access review cycle, 2 non-human service accounts (API app registrations with Global Administrator privileges) were omitted from the Entra ID reviewer attestation queue.
* **Evidence:** Entra ID Identity Governance campaign configuration exports and Q2 sign-off logs showing 23 of 25 active privileged accounts reviewed.
* **Cause:** Configuration gap in the identity governance automation script which filtered attestation targets exclusively by user object type (`UserPrincipalName`), excluding service principals (`ServicePrincipal`).
* **Risk:** Unmonitored or orphaned non-human privileged credentials could be exploited by malicious actors for persistent, undetected administrative access and data exfiltration.
* **Severity:** **High**
* **Recommendation:** Update the Entra ID Identity Governance dynamic group query and workflow scope to explicitly include all non-human service accounts and API client secrets, requiring formal sign-off by service owners.
* **Management Response:** Management agrees with the finding. The identity governance workflow script has been updated to include service principal objects effective immediately.
* **Owner:** Identity & Access Management (IAM) Lead
* **Due Date:** September 30, 2026

---

### Finding 2: Manual Contractor Offboarding Delays Exceeding SLA
* **Finding ID:** `FIND-2026-002`
* **Control:** Automated Joiner-Mover-Leaver (JML) provisioning (`CTRL-004`)
* **Criteria:** Enterprise Security Policy SEC-POL-04 requires all terminated employee and contractor access credentials to be disabled and session tokens revoked within 1 hour of formal offboarding notification.
* **Condition:** Testing of 15 recent terminations revealed that 2 external contractor terminations processed via manual spreadsheet logs experienced a 48-hour delay before account deactivation.
* **Evidence:** HRIS termination tickets matched against Active Directory disable timestamp logs and session token revocation records.
* **Cause:** Reliance on manual spreadsheet communication channels between vendor management and IT service desks for third-party contractor terminations, bypassing the automated HRIS webhook gateway.
* **Risk:** Retained access privileges by terminated contractors create an insider threat vulnerability, potentially allowing unauthorized access to internal repositories and sensitive data.
* **Severity:** **High**
* **Recommendation:** Onboard third-party contractor management systems directly into the centralized HRIS provisioning API to eliminate manual spreadsheet tracking and enforce automated JML triggers.
* **Management Response:** Management accepts the finding. Integration of contractor lifecycle management into the HRIS gateway is currently underway.
* **Owner:** Human Resources Operations Manager / IT Systems Administrator
* **Due Date:** October 15, 2026

---

### Finding 3: Expired Annual Security Re-Assessments for Legacy Vendors
* **Finding ID:** `FIND-2026-003`
* **Control:** Pre-engagement and annual third-party risk assessment (`CTRL-011`)
* **Criteria:** Enterprise Third-Party Risk Management Standard TPRM-02 requires annual security re-assessments and questionnaire updates for all active tier-1 and tier-2 vendors.
* **Condition:** Out of 10 sampled active vendors, 4 long-term vendors lacked documentation for their recurring annual security re-assessments, with review dates overdue by 6 to 9 months.
* **Evidence:** Vendor Risk Register database records and completed SIG Lite questionnaire timestamp logs.
* **Cause:** Absence of automated notification triggers in the legacy vendor tracking tool, leading reliance on manual calendar reminders which lapsed during personnel turnover.
* **Risk:** Unidentified security posture degradation or compliance failures at third-party vendors could lead to supply chain compromise or regulatory data breaches.
* **Severity:** **Medium**
* **Recommendation:** Deploy an automated GRC vendor risk module that automatically generates annual re-assessment tasks and sends escalation alerts to vendor managers 30 days prior to due dates.
* **Management Response:** Management concurs. Implementation of the automated GRC vendor portal is scheduled for completion next quarter.
* **Owner:** Vendor Risk Manager
* **Due Date:** November 30, 2026

---

### Finding 4: Emergency Break-Glass Accounts Configured with Standard App TOTP
* **Finding ID:** `FIND-2026-004`
* **Control:** Mandatory phishing-resistant Multi-Factor Authentication (`CTRL-001`)
* **Criteria:** Enterprise Authentication Standard AUTH-03 requires all emergency break-glass administrative accounts to utilize hardware-based phishing-resistant FIDO2 security keys rather than software-based TOTP applications.
* **Condition:** Emergency global administrator break-glass accounts were found to be provisioned with standard smartphone authenticator app TOTP tokens rather than isolated hardware security keys.
* **Evidence:** Entra ID Authentication Methods policy export for break-glass accounts `admin-emergency@enterprise.internal`.
* **Cause:** Initial deployment oversight during tenant creation where standard authentication defaults were applied to emergency accounts without subsequent hardening verification.
* **Risk:** Software-based TOTP tokens are susceptible to advanced adversary-in-the-middle (AitM) phishing attacks, potentially compromising emergency root administrative access.
* **Severity:** **Medium**
* **Recommendation:** Immediately provision hardware FIDO2 security keys for all break-glass accounts, store them securely in a physical biometric vault, and demote software TOTP methods.
* **Management Response:** Management agrees. FIDO2 security keys have been procured, configured, and placed in the executive physical safe.
* **Owner:** Enterprise Security Architect
* **Due Date:** September 15, 2026

---

### Finding 5: Backup Completion Alerts Routed to General IT Alias Without SLA Monitoring
* **Finding ID:** `FIND-2026-005`
* **Control:** Daily automated server backups and integrity verification (`CTRL-009`)
* **Criteria:** Enterprise Disaster Recovery Standard DR-01 requires backup failure alerts to be routed directly to a 24/7 Security Operations Center (SOC) incident queue with a mandatory 2-hour acknowledgement SLA.
* **Condition:** Backup job completion and failure notifications were configured to route to a general IT distribution list (`it-support@enterprise.internal`) rather than the PagerDuty / SIEM SOC queue.
* **Evidence:** Veeam Backup & Replication notification rules configuration export and email alias routing tables.
* **Cause:** Historical alert configuration carried over from legacy infrastructure setup without integration into modern enterprise incident response pipelines.
* **Risk:** Delayed identification of failed backup jobs could result in undetected data protection gaps, lengthening recovery time objectives (RTO) during a ransomware or system failure event.
* **Severity:** **Medium**
* **Recommendation:** Reconfigure Veeam notification settings to feed directly into the SIEM webhook and PagerDuty alerting matrix with automated paging escalations.
* **Management Response:** Management accepts the finding. Alert routing rules will be integrated into the PagerDuty SOC rotation.
* **Owner:** Infrastructure & Backup Operations Lead
* **Due Date:** October 01, 2026

---

### Finding 6: Incomplete Asset Tagging on Development Cloud Storage Buckets
* **Finding ID:** `FIND-2026-006`
* **Control:** Cloud Asset Inventory & Classification (`CTRL-018`)
* **Criteria:** Cloud Security Governance Policy CSP-02 mandates that all cloud storage buckets and virtual disks must be tagged with accurate data classification labels (Public, Internal, Confidential, Restricted) and owner metadata upon creation.
* **Condition:** An audit of cloud storage infrastructure identified 8 out of 45 development cloud storage buckets lacking mandatory data classification and ownership metadata tags.
* **Evidence:** Cloud Native Infrastructure audit reports generated via Cloud Security Posture Management (CSPM) tool.
* **Cause:** Developers bypassed infrastructure-as-code (IaC) linting checks when rapidly provisioning temporary testing environments in the sandbox subscription.
* **Risk:** Untagged and unclassified storage buckets increase the risk of shadow data accumulation, accidental public exposure, and non-compliance with data privacy regulations.
* **Severity:** **Low**
* **Recommendation:** Enforce automated CI/CD pipeline guardrails (Checkov/TFSec) that block the deployment of cloud storage resources lacking mandatory classification tags.
* **Management Response:** Management agrees. CI/CD pipeline blocking policies will be enforced across all cloud environments.
* **Owner:** Cloud Security Engineer
* **Due Date:** November 15, 2026

---

### Finding 7: Lack of Formal Documented Annual Review for IT Acceptable Use Policy
* **Finding ID:** `FIND-2026-007`
* **Control:** Information Security Policy Governance & Review (`CTRL-022`)
* **Criteria:** ISO/IEC 27001:2022 Control 5.15 (Access Control) and Enterprise Policy Governance Framework require all core security policies to be formally reviewed, updated, and approved by management on an annual basis.
* **Condition:** The enterprise IT Acceptable Use Policy (AUP-v1.4) had not undergone a formal documented annual review and re-approval sign-off for 14 months, exceeding the annual review window.
* **Evidence:** Policy document version history logs and Management Review Committee meeting minutes from 2025 and 2026.
* **Cause:** Oversight by the policy administrator during annual document repository archiving and migration to the new intranet portal.
* **Risk:** Outdated policy terms may fail to address emerging remote work, AI tool usage, or regulatory requirements, weakening legal enforceability of employee behavioral standards.
* **Severity:** **Low**
* **Recommendation:** Conduct an expedited annual review of the Acceptable Use Policy, incorporate updated remote work and generative AI guidelines, and obtain formal sign-off from the CISO.
* **Management Response:** Management concurs. The AUP review is currently in progress and will be finalized before the deadline.
* **Owner:** Governance, Risk, and Compliance (GRC) Analyst
* **Due Date:** December 15, 2026

