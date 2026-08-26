# Internal Audit Findings & Corrective Action Plan

## Overview
This document outlines the formal audit findings identified during the Information Security Internal Audit. Each finding details the control deficiency, regulatory or policy requirement, observed condition, supporting evidence, associated risk, root cause, severity rating, recommended corrective action, management response, designated owner, and target due date.

---

## Finding Summary
* **High Severity (2):** Lapsed Annual Penetration Testing; Outdated Business Continuity / Disaster Recovery (BCP/DR) Failover Testing.
* **Medium Severity (3):** Lack of Mandatory Customer Breach Notification Timeframes; Incomplete Privileged Access Reviews; Unvetted Sub-Processors.
* **Low Severity (2):** Unstructured Data Classification Lables; Inconsistent Risk Register Ticket Linkages.

---

## Detailed Audit Findings

### Finding 1 (High): Lapsed Annual Penetration Testing
* **Finding ID:** AUD-FIN-001
* **Title:** Lapsed Annual Third-Party Penetration Testing
* **Requirement:** ISO/IEC 27001:2022 Control A.12.6.1 and internal policies require external third-party penetration testing of core applications and APIs to be conducted at least annually.
* **Condition:** The organization's most recent third-party penetration test report is 18 months old.
* **Evidence:** Penetration test report dated February 2025 (Audit inspection conducted in August 2026).
* **Risk:** Unidentified vulnerabilities in cloud infrastructure, web applications, or APIs may be exploited by external threat actors, leading to unauthorized system access or data compromise.
* **Root Cause:** Over-reliance on internal vulnerability scanners without an automated tracking mechanism or budget pre-approval for annual external testing engagements.
* **Severity:** **High**
* **Recommendation:** Immediately engage an accredited third-party cybersecurity firm to perform a comprehensive penetration test of all production environments and establish an automated calendar reminder for annual recertification.
* **Management Response:** Accepted. Budget has been approved, and scheduling with an external auditing vendor is underway.
* **Owner:** Lead Information Security Engineer
* **Target Date:** September 30, 2026

---

### Finding 2 (High): Lapsed BCP/DR Failover Testing
* **Finding ID:** AUD-FIN-002
* **Title:** Failure to Execute Annual Disaster Recovery Failover Testing
* **Requirement:** ISO/IEC 27001:2022 Control A.17.1.3 and organizational BCP standards mandate full-scale disaster recovery failover simulations at least annually.
* **Condition:** No full-scale BCP/DR failover test has been performed or documented in the last 14 months.
* **Evidence:** Last documented BCP/DR failover test report dated June 2025.
* **Risk:** Inability to restore critical cloud infrastructure or meet RTO/RPO objectives during a major regional outage or ransomware incident, resulting in severe operational disruption.
* **Root Cause:** Competing operational project priorities delayed the scheduling of the annual disaster recovery simulation window.
* **Severity:** **High**
* **Recommendation:** Authorize an immediate full-scale technical disaster recovery failover test for all Tier-1 critical applications and update the compliance calendar to enforce mandatory annual execution.
* **Management Response:** Agreed. A comprehensive failover simulation is scheduled for the upcoming quarter.
* **Owner:** Chief Information Security Officer (CISO) & IT Infrastructure Lead
* **Target Date:** October 15, 2026

---

### Finding 3 (Medium): Lack of Mandatory Customer Breach Notification Timeframe
* **Finding ID:** AUD-FIN-003
* **Title:** Undefined Data Breach Notification SLA in Incident Procedures
* **Requirement:** Internal incident management policy and UAE data protection regulatory mandates require clear, time-bound customer and regulatory notification SLAs in the event of a security breach.
* **Condition:** The current Incident Response Plan (IRP) and standard operating procedures lack a defined, mandatory 24–48 hour customer breach notification timeframe.
* **Evidence:** Review of Incident Response Standard Operating Procedure (SOP-IR-04).
* **Risk:** Delayed notification to affected clients and regulatory authorities inhibits timely defensive actions and violates statutory reporting compliance obligations.
* **Root Cause:** Policy drafting oversight during the transition to the updated incident response framework.
* **Severity:** **Medium**
* **Recommendation:** Update the Incident Response Plan and standard operating procedures to include an explicit 24 to 48-hour mandatory customer and regulatory notification clause.
* **Management Response:** Accepted. Policy revision is currently under legal review for immediate integration.
* **Owner:** Head of Legal & Compliance
* **Target Date:** September 10, 2026

---

### Finding 4 (Medium): Incomplete Privileged Access Reviews
* **Finding ID:** AUD-FIN-004
* **Title:** Absence of Formal Sign-Off for Cloud Administrator Access Reviews
* **Requirement:** Access Control policy mandates quarterly formal reviews and recertification of all privileged and administrative accounts.
* **Condition:** While Q1 access reviews were completed on time, Q2 privileged access review logs lacked formal sign-off documentation for cloud infrastructure administrators.
* **Evidence:** Q1 and Q2 2026 Identity and Access Management (IAM) review logs.
* **Risk:** Orphaned administrative accounts or excessive user permissions could be exploited by malicious insiders or compromised credentials to execute unauthorized system changes.
* **Root Cause:** Lack of automated sign-off tracking within the cloud identity management dashboard.
* **Severity:** **Medium**
* **Recommendation:** Generate and archive the missing Q2 privileged access review sign-off sheets and implement automated quarterly review reminders within Microsoft Entra ID.
* **Owner:** Identity Access Management Administrator
* **Target Date:** September 15, 2026
* **Management Response:** Acknowledged. Access logs will be updated and automated review workflows configured.

---

### Finding 5 (Medium): Unvetted Sub-Processors in Supply Chain
* **Finding ID:** AUD-FIN-005
* **Title:** Lack of Independent Security Assessments for Sub-Processors
* **Requirement:** Vendor Risk Management framework requires all fourth-party sub-processors utilized by key vendors to be formally risk-assessed and bound by equivalent security obligations.
* **Condition:** Key vendor GulfPay Services utilizes two external subcontractors whose security postures and compliance certifications have not been independently reviewed.
* **Evidence:** Vendor assessment review file and sub-processor inventory list for GulfPay Services.
* **Risk:** Exposure to supply chain attacks or downstream data breaches originating from inadequately secured third-party subcontractor infrastructure.
* **Root Cause:** Historical vendor onboarding processes focused primarily on primary suppliers without mandating full sub-processor transparency.
* **Severity:** **Medium**
* **Recommendation:** Request and review complete SOC 2 Type II reports or security assessment packages for both sub-processors, alongside signed Data Processing Agreements (DPAs).
* **Management Response:** Agreed. Vendor management has reached out to GulfPay Services to collect the required subcontractor documentation.
* **Owner:** Director of Procurement & Vendor Management
* **Target Date:** September 30, 2026

---

### Finding 6 (Low): Unstructured Data Classification Lables
* **Finding ID:** AUD-FIN-006
* **Title:** Inconsistent Implementation of Sensitivity Labels on Unstructured Files
* **Requirement:** Data Classification policy requires all files stored on corporate shared drives to be tagged with appropriate sensitivity labels (e.g., Internal, Confidential).
* **Condition:** Automated labeling is active for emails, but unstructured files on departmental shared drives frequently lack mandatory classification tags.
* **Evidence:** Sample audit inspection of 25 files across SharePoint and OneDrive repositories.
* **Risk:** Misclassification or improper handling of sensitive corporate files by employees, increasing the likelihood of accidental data exposure.
* **Root Cause:** Relying solely on manual user application of sensitivity labels without strict automated blocking rules.
* **Severity:** **Low**
* **Recommendation:** Enable default mandatory sensitivity labeling rules within Microsoft Purview for all new documents created on shared corporate repositories.
* **Management Response:** Accepted. Purview default labeling policies will be deployed in phased rollout.
* **Owner:** Cloud Collaboration Administrator
* **Target Date:** October 30, 2026

---

### Finding 7 (Low): Inconsistent Risk Register Ticket Linkages
* **Finding ID:** AUD-FIN-007
* **Title:** Lack of Explicit Tracking Links Between Enterprise Risks and Technical Tickets
* **Requirement:** Enterprise Risk Management framework requires identified high-level risks to maintain explicit traceability links to operational remediation tickets.
* **Condition:** The enterprise risk register is actively maintained, but linkage to lower-level technical remediation tickets in Jira/GitHub is maintained manually rather than automatically.
* **Evidence:** Inspection of Enterprise Risk Register and sample tracking entries.
* **Risk:** Potential disconnect between high-level risk oversight and actual technical task execution, leading to delayed remediation tracking.
* **Root Cause:** Decoupled tooling between corporate GRC registers and engineering ticketing systems.
* **Severity:** **Low**
* **Recommendation:** Implement a unified API or standard labeling convention linking risk register IDs directly to GitHub and Jira remediation issues.
* **Management Response:** Acknowledged. Will evaluate integration options during the next GRC tool review cycle.
* **Owner:** GRC Compliance Analyst
* **Target Date:** November 15, 2026

