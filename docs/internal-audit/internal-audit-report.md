# Internal Audit Report: Information Security Management System (ISMS)
**Organization:** Fictional UAE Company  
**Audit Period:** August 2025 – August 2026 | **Report Date:** August 2026  

---

## Executive Summary
This internal audit report provides an independent evaluation of the information security governance, risk management, and operational control environment of the organization. Over the review period of August 2025 to August 2026, testing was conducted across fifteen core control domains in alignment with ISO/IEC 27001:2022 benchmarks, internal policies, and applicable UAE regulatory mandates. 

The evaluation revealed robust foundational strengths, particularly in access control enforcement via multi-factor authentication (MFA), vulnerability management lifecycles, and high employee participation in security awareness training. However, critical operational gaps were identified regarding lapsed annual penetration testing, overdue disaster recovery failover simulations, and third-party sub-processor transparency. Furthermore, procedural deficiencies were noted concerning customer breach notification SLAs and privileged access review logging. 

**Overall Conclusion:** **Partially Effective**  
While foundational technical security controls are operating effectively, significant compliance and assurance lapses in periodic testing and third-party risk governance prevent an "Effective" rating. Management has acknowledged these findings and committed to a structured corrective action plan to remediate all identified vulnerabilities within the established target dates.

---

## 1. Audit Objective
To independently and objectively evaluate the design, operating effectiveness, and maturity of the organization's ISMS, ensuring adequate asset protection, risk mitigation, and compliance with internal policies and regional regulatory standards.

## 2. Audit Scope
Encompasses all operational units, cloud infrastructure environments, physical facilities, and administrative processes, specifically focusing on governance, risk management, access control, data classification, incident management, business continuity, vendor risk, and security awareness.

## 3. Audit Criteria
* ISO/IEC 27001:2022 (Information Security Management Systems)
* Organization's internal security policies and standard operating procedures
* Applicable UAE data protection and cybersecurity regulatory requirements

## 4. Methodology
Risk-based internal audit methodology aligned with professional standards, including preliminary planning, document inspection, sample-based control testing, stakeholder walkthrough interviews, and root-cause analysis.

## 5. Overall Conclusion
**Partially Effective** — Core technical controls are strong, but critical testing lapses and supply-chain oversight gaps require immediate remediation.

## 6. Key Strengths
1. **Robust Access Control:** Tenant-wide Multi-Factor Authentication (MFA) enforcement via Microsoft Entra ID conditional access policies.
2. **Effective Vulnerability Management:** Automated monthly vulnerability scanning of cloud infrastructure and systematic remediation tracking.
3. **Strong Security Culture:** High employee engagement (96% completion rate) in annual security awareness training and bi-annual phishing simulations.

## 7. Findings Summary
* **Critical / High (2):** 
  * AUD-FIN-001: Lapsed Annual Third-Party Penetration Testing
  * AUD-FIN-002: Lapsed Disaster Recovery Failover Testing
* **Medium (3):** 
  * AUD-FIN-003: Undefined Data Breach Notification SLAs
  * AUD-FIN-004: Incomplete Privileged Access Review Sign-Offs
  * AUD-FIN-005: Unvetted Sub-Processors in Supply Chain
* **Low (2):** 
  * AUD-FIN-006: Inconsistent Unstructured Data Classification Labels
  * AUD-FIN-007: Decoupled Risk Register and Remediation Ticket Linkages

---

## 8. Detailed Findings Summary
* **AUD-FIN-001 (High):** The organization's latest third-party penetration test report is 18 months old, violating annual testing mandates.
* **AUD-FIN-002 (High):** No full-scale BCP/DR failover simulation has been executed or documented in the last 14 months.
* **AUD-FIN-003 (Medium):** Incident response procedures lack explicit 24–48 hour customer breach notification SLAs.
* **AUD-FIN-004 (Medium):** Q2 privileged access review logs lacked formal sign-off documentation for cloud administrators.
* **AUD-FIN-005 (Medium):** Key vendor GulfPay Services utilizes two unvetted external sub-processors.
* **AUD-FIN-006 (Low):** Unstructured files on shared corporate drives frequently lack mandatory sensitivity labels.
* **AUD-FIN-007 (Low):** Enterprise risk register items maintain manual rather than automated traceability links to Jira/GitHub tickets.

---

## 9. Corrective Action & Management Recommendations
Management has accepted all audit findings and initiated a comprehensive remediation roadmap. Key actions include:
* Engaging an accredited external firm to perform an immediate network and application penetration test.
* Scheduling and executing a full-scale cloud disaster recovery failover simulation.
* Updating incident response standard operating procedures to mandate 24-hour customer breach notifications.
* Archiving missing privileged access sign-offs and collecting SOC 2 reports for all vendor sub-processors.

---

## 10. Follow-up
The Internal Audit team will conduct a formal follow-up review on **November 15, 2026**, to verify the implementation status of all corrective action plans and evaluate the closure of open findings.

