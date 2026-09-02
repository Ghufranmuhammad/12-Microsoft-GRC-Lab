# Enterprise GRC Control Operating Effectiveness Testing Register

**Document ID:** `OET-001`  
**Version:** v2.0  
**Effective Date:** August 2026  
**Classification:** Confidential  
**Framework Alignment:** ISO/IEC 27001:2022, NIST SP 800-53 Rev. 5, UAE PDPL  

---

## 1. Executive Summary
This document records the operational testing execution, fictional evidence collection, sample comparisons, and final operational effectiveness conclusions for five core enterprise controls.

---

## 2. Detailed Operating Effectiveness Test Results

### Control 1: Quarterly Privileged Access Review (`CTRL-003`)
* **Control:** Quarterly privileged-access review workflow in Entra ID / Identity Governance.
* **Evidence:** Q1 and Q2 access-review sign-off reports and Entra ID privileged role assignment exports.
* **Test Procedure:** Compare the total active privileged-account population against the reviewer sign-off population across Q1 and Q2 audit cycles.
* **Test Findings:** Testing identified that across the active population of 25 privileged accounts, only 23 accounts were included in the Q2 review scope (2 non-human service accounts were omitted due to manual configuration gaps).
* **Operating Effectiveness Result:** **Ineffective** (Operational failure due to incomplete population coverage during the Q2 attestation cycle).
* **Conclusion Explanation:** Although the quarterly review process operated successfully for human administrators, the omission of privileged service accounts violates the control objective of comprehensive review coverage, resulting in an operational exception and a formal finding (`FIND-001`).

---

### Control 2: Multi-Factor Authentication (MFA) Enforcement (`CTRL-001`)
* **Control:** Mandatory phishing-resistant Multi-Factor Authentication (MFA) for all user and administrative logins.
* **Evidence:** Microsoft Entra ID Conditional Access policy configuration exports and authentication sign-in logs for July–August 2026.
* **Test Procedure:** Sample 100 authentication logs (including admin, standard, and remote user logins) and verify that 100% successfully challenged and enforced phishing-resistant MFA, with zero legacy authentication bypasses.
* **Test Findings:** All 100 sampled authentication attempts enforced MFA successfully. Zero legacy protocol bypasses or unchallengeable sessions were detected.
* **Operating Effectiveness Result:** **Effective** (The control operated consistently and perfectly across all sampled operational instances).
* **Conclusion Explanation:** The technical enforcement mechanism via Entra ID Conditional Access policies operated flawlessly throughout the review period, confirming that authentication controls are fully operational.

---

### Control 3: Automated Offboarding & Account Deactivation (`CTRL-004`)
* **Control:** Automated Joiner-Mover-Leaver (JML) provisioning integrated between HRIS and Active Directory.
* **Evidence:** HRIS termination tickets, Active Directory account deactivation timestamp logs, and session revocation audit records for Q2–Q3 2026.
* **Test Procedure:** Sample 15 recent employee and contractor terminations, comparing the exact timestamp of HRIS termination approval against the AD disable timestamp and token revocation record.
* **Test Findings:** 13 out of 15 sampled terminations executed automated deactivation within 15 minutes. However, 2 external contractor terminations processed manually via spreadsheet logs showed a 48-hour delay before account disablement.
* **Operating Effectiveness Result:** **Partially Effective** (Operating effectively for internal HR employees, but exhibiting operational exceptions for manual contractor offboarding pathways).
* **Conclusion Explanation:** While automated JML workflows function as intended, manual exceptions introduced significant operational lag in revoking third-party contractor access, necessitating corrective action (`FIND-002`).

---

### Control 4: Vendor Security Risk Assessment (`CTRL-011`)
* **Control:** Pre-engagement and annual third-party risk assessment using standardized questionnaires (SIG/CAIQ).
* **Evidence:** Vendor Risk Register, completed SIG Lite questionnaires, and signed contract date logs for active vendors in 2026.
* **Test Procedure:** Sample 10 active third-party vendors onboarded or reviewed in 2026 and inspect files for completed security questionnaires, risk scores, and annual re-assessment sign-offs.
* **Test Findings:** Pre-engagement reviews were present for all 10 vendors, but 4 out of 10 long-term vendors lacked documentation for their recurring annual security re-assessments due to expired manual tracking.
* **Operating Effectiveness Result:** **Ineffective** (Widespread operational failure in executing recurring annual vendor reviews).
* **Conclusion Explanation:** The absence of completed annual re-assessments for 40% of the sample indicates that ongoing operational monitoring of third-party risk is not functioning reliably under manual tracking methods.

---

### Control 5: Automated Backup & Integrity Verification (`CTRL-009`)
* **Control:** Daily automated server backups with weekly immutability locks and monthly test restores.
* **Evidence:** Veeam backup job success logs, immutability status confirmation outputs, and monthly test restore execution minutes for July–August 2026.
* **Test Procedure:** Inspect daily backup job logs for 60 consecutive days, verify immutability flag enforcement on weekly backup points, and review July/August test restore validation reports.
* **Test Findings:** 60 of 60 daily backup jobs completed successfully with zero job failures. Weekly immutability locks were successfully verified, and monthly test restores completed with 100% data recoverability.
* **Operating Effectiveness Result:** **Effective** (The backup and verification control operated without exception across the entire testing window).
* **Conclusion Explanation:** System logs and restore validation reports confirm that the backup schedule, immutability safeguards, and recoverability tests operated reliably and continuously as designed.

