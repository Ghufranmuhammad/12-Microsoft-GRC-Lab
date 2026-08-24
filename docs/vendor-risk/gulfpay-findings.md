# Vendor Assessment Findings: GulfPay Services

This document details the specific compliance, security, and governance findings identified during the third-party risk assessment of GulfPay Services. Each finding outlines the control deficiency, regulatory or policy requirement, observed evidence, associated risk, severity, recommended remediation action, vendor response, and target completion date.

---

## Finding 1: Outdated Penetration Test Report
* **Finding:** The vendor's most recent third-party penetration test report is 18 months old, violating the requirement for annual independent security testing.
* **Requirement:** Vendors handling critical financial data and Emirates ID information must undergo and provide a comprehensive third-party penetration test report at least annually.
* **Evidence:** Penetration test report dated February 2025 (current assessment date: August 2026).
* **Risk:** Unidentified vulnerabilities in application code, APIs, or cloud infrastructure may be exploited by malicious actors, leading to data exfiltration or unauthorized system access.
* **Severity:** **High**
* **Recommendation:** Require GulfPay Services to complete an immediate, independent third-party penetration test covering all payroll APIs and cloud environments, and supply the full executive summary and remediation status.
* **Vendor Response:** Acknowledged. Remediation test currently scheduled with an external cybersecurity auditing firm.
* **Target Date:** September 30, 2026

---

## Finding 2: Lapsed Business Continuity and Disaster Recovery (BCP/DR) Testing
* **Finding:** GulfPay Services has not performed or documented a BCP/DR failover test in the last 14 months.
* **Requirement:** Critical payroll service providers must conduct and document annual BCP/DR failover tests to guarantee service availability and meet RTO/RPO commitments.
* **Evidence:** Last documented BCP/DR test report dated June 2025.
* **Risk:** Inability to restore operations or recover payroll databases within required recovery windows during a major outage or ransomware event, leading to severe business disruption for clients.
* **Severity:** **High**
* **Recommendation:** Request a formal plan and timeline for conducting the upcoming full-scale BCP/DR failover simulation, including documented RTO and RPO validation metrics.
* **Vendor Response:** Agreed. BCP simulation exercise is scheduled for the upcoming quarter.
* **Target Date:** October 15, 2026

---

## Finding 3: Unvetted Sub-Processors and Third-Party Dependencies
* **Finding:** The vendor utilizes two external subcontractors for infrastructure and data processing support whose security postures and compliance certifications have not been independently reviewed or provided.
* **Requirement:** All fourth-party sub-processors must be formally identified, risk-assessed, and bound by equivalent security and data protection obligations.
* **Evidence:** Sub-processor inventory list showing two unassessed external entities with access to processing environments.
* **Risk:** Exposure to supply chain attacks or downstream data breaches originating from inadequately secured subcontractor infrastructure.
* **Severity:** **Medium**
* **Recommendation:** Obtain complete SOC 2 Type II reports or security assessment packages for both sub-processors, alongside copies of signed Data Processing Agreements (DPAs).
* **Vendor Response:** Will compile and provide subcontractor security documentation and compliance attestations.
* **Target Date:** September 15, 2026

---

## Finding 4: Undefined Data Breach Notification Timeframe
* **Finding:** GulfPay's incident response procedure and contractual terms do not specify a mandatory customer notification timeframe (such as 24 to 48 hours) in the event of a security breach.
* **Requirement:** Vendors must contractually commit to notifying corporate clients of any confirmed or suspected security incident affecting PII or financial data within 24 to 48 hours of discovery.
* **Evidence:** Review of GulfPay's standard Master Services Agreement (MSA) and incident response SLA documentation.
* **Risk:** Delayed notification inhibits the organization's ability to meet regulatory reporting mandates (e.g., UAE Data Protection Law) and take timely defensive actions.
* **Severity:** **High**
* **Recommendation:** Execute a contractual addendum establishing a strict 24-hour mandatory incident and data breach notification SLA.
* **Vendor Response:** Legal team reviewing contract amendment language for integration into current terms.
* **Target Date:** September 10, 2026

---

## Finding 5: Lack of Evidence for Privileged Access Reviews
* **Finding:** GulfPay Services failed to provide audit logs or documentation proving the execution of periodic privileged-access reviews.
* **Requirement:** Privileged accounts and administrative access rights must be formally reviewed at least quarterly to ensure adherence to the principle of least privilege.
* **Evidence:** Absence of periodic access review sign-off sheets or Identity and Access Management (IAM) review logs for Q1 and Q2 2026.
* **Risk:** Orphaned accounts or excessive administrative permissions could be leveraged by malicious insiders or compromised credentials to execute unauthorized system changes.
* **Severity:** **Medium**
* **Recommendation:** Require GulfPay to produce their most recent quarterly privileged access review report and establish a recurring calendar schedule for future reviews.
* **Vendor Response:** Will generate and provide the current privileged access audit logs from the IAM system.
* **Target Date:** September 5, 2026

