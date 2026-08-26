# Internal Audit Working Papers: Information Security Mock Audit

## Overview
This document contains the working papers and test results for the Information Security Internal Audit conducted across the fictional UAE organization. A total of 15 control tests were executed across various domains using sample-based inspection, policy walkthroughs, and technical configuration reviews.

---

## Audit Test Register

### Test 1: Information Security Policy Approval
* **Test ID:** TST-001
* **Control:** Information Security Governance Policy
* **Requirement:** Information security policies must be formally documented, approved by executive management, and reviewed annually.
* **Evidence:** Master Information Security Policy document v3.2 with digital board sign-off.
* **Testing Procedure:** Inspected policy document metadata, approval signatures, and compared the annual review date against organizational change logs.
* **Sample:** Master Policy Document (POL-SEC-01)
* **Result:** Pass
* **Auditor Observation:** Policy was reviewed and approved by the CISO and Executive Board within the last 12 months.
* **Conclusion:** Control is operating effectively.

### Test 2: Risk Assessment Execution
* **Test ID:** TST-002
* **Control:** Enterprise Risk Assessment
* **Requirement:** Comprehensive risk assessments must be conducted at least annually to identify and evaluate asset vulnerabilities and threats.
* **Evidence:** Enterprise Risk Register and Annual Risk Assessment Report 2025/2026.
* **Testing Procedure:** Reviewed risk register entries, methodology documentation, and verified scoring consistency across business units.
* **Sample:** Risk Register (Sample of 20 identified operational risks)
* **Result:** Pass
* **Auditor Observation:** Risk register is actively maintained, though linkage to lower-level technical remediation tickets could be more explicit.
* **Conclusion:** Control is operating effectively with minor opportunities for process refinement.

### Test 3: Multi-Factor Authentication (MFA) Enforcement
* **Test ID:** TST-003
* **Control:** Access Control & MFA
* **Requirement:** Multi-factor authentication must be enforced for all administrative and remote user access to corporate resources.
* **Evidence:** Microsoft Entra ID Conditional Access Policy configuration export.
* **Testing Procedure:** Verified conditional access rules requiring MFA for all user roles without exception policies.
* **Sample:** Active Directory Tenant Policy Configuration & 15 user account samples.
* **Result:** Pass
* **Auditor Observation:** MFA enforcement is active tenant-wide via Conditional Access policies.
* **Conclusion:** Control is operating effectively.

### Test 4: Privileged Access Reviews
* **Test ID:** TST-004
* **Control:** Privileged Account Governance
* **Requirement:** Privileged access rights and administrative accounts must be formally reviewed on a quarterly basis.
* **Evidence:** Q1 and Q2 2026 Privileged Access Review logs.
* **Testing Procedure:** Inspected review sign-off sheets and checked for removal or recertification of terminated employee admin accounts.
* **Sample:** Q1/Q2 Access Review Logs (Sample of 10 privileged accounts)
* **Result:** Partial
* **Auditor Observation:** Q1 review was conducted on time, but Q2 review lacked formal sign-off documentation for cloud infrastructure administrators.
* **Conclusion:** Control deficiency noted; requires remediation.

### Test 5: Data Classification Implementation
* **Test ID:** TST-005
* **Control:** Data Classification Scheme
* **Requirement:** Data must be classified into defined tiers (e.g., Public, Internal, Confidential, Restricted) and labeled accordingly.
* **Evidence:** Data Classification Policy and Microsoft Purview sensitivity label configuration.
* **Testing Procedure:** Inspected Purview sensitivity label rules and sampled files across departmental shared drives.
* **Sample:** 25 files sampled across SharePoint and OneDrive repositories.
* **Result:** Partial
* **Auditor Observation:** Automated labeling works for emails, but unstructured files on shared drives frequently lack mandatory classification tags.
* **Conclusion:** Control operating partially; user adherence requires reinforcement.

### Test 6: Incident Response Plan Testing
* **Test ID:** TST-006
* **Control:** Incident Management & Testing
* **Requirement:** The Incident Response Plan (IRP) must be formally documented and tested via tabletop simulations at least annually.
* **Evidence:** Incident Response Plan v2.0 and Tabletop Exercise After-Action Report (June 2025).
* **Testing Procedure:** Inspected IRP document date and reviewed tabletop exercise simulation transcripts and attendance logs.
* **Sample:** IRP document and annual simulation report.
* **Result:** Pass
* **Auditor Observation:** Comprehensive IRP is in place and annual tabletop simulation was duly executed.
* **Conclusion:** Control is operating effectively.

### Test 7: Breach Notification Timeframe SLA
* **Test ID:** TST-007
* **Control:** Breach Notification Procedures
* **Requirement:** Incident response procedures must mandate customer and regulatory data breach notification within 24 to 48 hours.
* **Evidence:** Standard Operating Procedure (SOP) for Security Incidents.
* **Testing Procedure:** Reviewed incident escalation SOP text for explicit customer notification timeline clauses.
* **Sample:** SOP-IR-04 Section 5 (Notification SLAs)
* **Result:** Fail
* **Auditor Observation:** The current incident response procedure outlines internal escalation steps but lacks a defined, mandatory 24-48 hour external customer notification timeframe.
* **Conclusion:** Control failure; requires immediate policy update.

### Test 8: Business Impact Analysis (BIA) Completeness
* **Test ID:** TST-008
* **Control:** Business Continuity Planning - BIA
* **Requirement:** Critical business processes must undergo a documented Business Impact Analysis (BIA) to determine RTO and RPO requirements.
* **Evidence:** Enterprise BIA Register and Criticality Scoring Matrix.
* **Testing Procedure:** Inspected BIA documentation for core business units and verified scoring calculations.
* **Sample:** 5 critical business processes evaluated in BIA.
* **Result:** Pass
* **Auditor Observation:** BIA register is thoroughly documented with clear RTO/RPO targets established.
* **Conclusion:** Control is operating effectively.

### Test 9: Annual Disaster Recovery (DR) Testing
* **Test ID:** TST-009
* **Control:** Disaster Recovery Failover Testing
* **Requirement:** Full-scale disaster recovery failover tests must be conducted and documented annually.
* **Evidence:** Last DR test execution report.
* **Testing Procedure:** Inspected date of last documented DR simulation report against current system date.
* **Sample:** Annual DR test documentation for primary cloud environment.
* **Result:** Fail
* **Auditor Observation:** Last full-scale BCP/DR failover test was conducted 14 months ago, exceeding the annual testing mandate.
* **Conclusion:** Control failure; testing schedule lapsed.

### Test 10: Vendor Due Diligence & Security Questionnaires
* **Test ID:** TST-010
* **Control:** Vendor Risk Management Onboarding
* **Requirement:** All third-party vendors must complete a security questionnaire and undergo due diligence prior to contract execution.
* **Evidence:** Completed vendor security questionnaires and scoring sheets.
* **Testing Procedure:** Inspected onboarding records for a sample of 5 recently contracted vendors.
* **Sample:** 5 active vendor onboarding files.
* **Result:** Pass
* **Auditor Observation:** All sampled vendors completed security questionnaires and scoring matrices prior to onboarding.
* **Conclusion:** Control is operating effectively.

### Test 11: Fourth-Party / Sub-Processor Vetting
* **Test ID:** TST-011
* **Control:** Sub-Processor Risk Management
* **Requirement:** Third-party vendors utilizing external sub-processors must provide documented security assessments and compliance attestations for those sub-processors.
* **Evidence:** Sub-processor inventory and review documentation for GulfPay Services.
* **Testing Procedure:** Checked vendor file for sub-processor disclosures and independent security evaluation records.
* **Sample:** GulfPay Services vendor assessment file.
* **Result:** Fail
* **Auditor Observation:** Vendor uses two external sub-processors whose security postures have not been independently reviewed or documented.
* **Conclusion:** Control failure; supply chain visibility gap identified.

### Test 12: Security Awareness Training Completion
* **Test ID:** TST-012
* **Control:** Security Awareness & Training
* **Requirement:** All employees must complete security awareness training upon hire and annually thereafter.
* **Evidence:** Learning Management System (LMS) completion tracking logs for 2026.
* **Testing Procedure:** Queried LMS database for completion rates and checked overdue training lists.
* **Sample:** LMS compliance report (Sample of 50 active employees).
* **Result:** Pass
* **Auditor Observation:** 96% completion rate achieved across organization; automated reminders active for outstanding users.
* **Conclusion:** Control is operating effectively.

### Test 13: Phishing Simulation Exercises
* **Test ID:** TST-013
* **Control:** Phishing Testing & Culture
* **Requirement:** Periodic simulated phishing campaigns must be conducted at least bi-annually to test employee awareness.
* **Evidence:** Phishing campaign reports from Q1 and Q2 2026.
* **Testing Procedure:** Reviewed campaign statistics, click-through rates, and mandatory remedial training assignments for repeat clickers.
* **Sample:** Q1 and Q2 Phishing Campaign Execution Reports.
* **Result:** Pass
* **Auditor Observation:** Campaigns executed bi-annually with appropriate follow-up training for employees who failed simulations.
* **Conclusion:** Control is operating effectively.

### Test 14: Vulnerability Scanning Cadence
* **Test ID:** TST-014
* **Control:** Vulnerability Management
* **Requirement:** Automated vulnerability scans of cloud infrastructure and web applications must be performed at least monthly.
* **Evidence:** Automated vulnerability scanner (Defender for Cloud / Tenable) monthly schedule and scan logs.
* **Testing Procedure:** Inspected scan schedules and sample report timestamps for the past 6 months.
* **Sample:** Monthly vulnerability scan logs (Feb 2026 – Jul 2026).
* **Result:** Pass
* **Auditor Observation:** Monthly scans execute automatically per policy; vulnerability remediation SLAs are tracked.
* **Conclusion:** Control is operating effectively.

### Test 15: Penetration Testing Recertification
* **Test ID:** TST-015
* **Control:** Third-Party Penetration Testing
* **Requirement:** External third-party penetration testing of core applications and APIs must be conducted at least annually.
* **Evidence:** Third-party penetration test reports.
* **Testing Procedure:** Inspected report publication date and scope of testing against current architecture.
* **Sample:** Penetration test report on file.
* **Result:** Fail
* **Auditor Observation:** The most recent penetration test report on file is 18 months old, violating the annual recertification requirement.
* **Conclusion:** Control failure; requires immediate scheduling of an external penetration test.
