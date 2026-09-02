# Enterprise Incident Response Policy

**Document ID:** `POL-004`  
**Version:** v3.1  
**Effective Date:** February 20, 2025  
**Review Date:** February 20, 2026  
**Classification:** Confidential  
**Status:** Active  
**Policy Owner:** Chief Information Security Officer (CISO) & Head of SOC  
**Approver:** Chief Risk Officer & Executive Leadership Team  

---

## 1. Purpose
The Incident Response Policy establishes a rigorous, structured, and repeatable framework for detecting, containing, eradicating, and recovering from cybersecurity incidents. The primary objective is to minimize business disruption, protect sensitive enterprise assets, preserve legal and forensic evidence, and fulfill statutory reporting obligations under UAE laws and international cybersecurity frameworks (ISO/IEC 27001, NIST SP 800-63/800-61, and NCA ECC).

---

## 2. Scope
This policy applies universally across all information assets, networks, endpoints, cloud workloads, applications, and business units managed by the enterprise. It governs the actions of all employees, contractors, managed security service providers, and incident response team (IRT) members.

---

## 3. Incident Response Lifecycle
The enterprise adheres to an 8-stage sequential incident response lifecycle:


* **3.1 Preparation:** Maintaining documented runbooks, deploying automated SIEM and EDR detection tools, conducting team training, and executing regular tabletop simulation exercises.
* **3.2 Detection:** Continuous monitoring of security telemetry, firewall logs, user behavior analytics, and endpoint sensors to identify anomalous activity or indicators of compromise (IoCs).
* **3.3 Reporting:** Immediate notification of suspected security events by employees to the Security Operations Center (SOC) via designated emergency channels.
* **3.4 Triage:** Initial analysis and classification of reported events to verify validity, scope out the affected systems, and assign a preliminary severity level.
* **3.5 Containment:** Executing immediate isolation measures (network disconnection, account suspension, IP blocking) to prevent the lateral spread of malware or threat actor access.
* **3.6 Eradication:** Removing root causes, deleting malicious payloads, patching underlying vulnerabilities, and resetting compromised credentials.
* **3.7 Recovery:** Restoring systems to normal operational status from clean, verified backups, conducting integrity checks, and monitoring for secondary threat activity.
* **3.8 Lessons Learned:** Conducting post-incident reviews, documenting root causes, updating security controls, and refining incident response playbooks within 14 days of resolution.

---

## 4. Incident Response Roles & Responsibilities
* **Incident Commander (SOC Lead):** Leads tactical response operations, coordinates technical containment, and oversees forensic evidence collection.
* **Chief Information Security Officer (CISO):** Directs strategic crisis management, coordinates with executive leadership, and authorizes external notifications.
* **Legal Counsel:** Advises on legal liability, regulatory disclosure requirements, and law enforcement liaison.
* **Corporate Communications Lead:** Manages internal messaging, public relations, and stakeholder communications under executive oversight.
* **System Owners & IT Engineers:** Provide technical access, assist with system restoration, and apply emergency patches.

---

## 5. Severity Levels & Categorization
Incidents are categorized into four severity tiers based on business impact and scope:

| Severity Level | Description & Impact Criteria | Response SLA |
| :--- | :--- | :--- |
| **Sev-1 (Critical)** | Active ransomware, widespread data exfiltration of Restricted PII, critical infrastructure outage, or targeted nation-state intrusion. | Immediate (< 15 mins) |
| **Sev-2 (High)** | Compromise of multiple non-critical servers, privileged account takeover without immediate data loss, or significant malware infection. | Within 1 hour |
| **Sev-3 (Medium)** | Isolated phishing success, unauthorized software installation on a single endpoint, or non-disruptive policy scan alert. | Within 4 hours |
| **Sev-4 (Low)** | Blocked malware attempt, low-risk port scan, or minor security anomaly with zero operational impact. | Within 24 hours |

---

## 6. Escalation Matrix
* **Sev-1 & Sev-2 Incidents:** Trigger immediate automated paging to the on-call Incident Commander, CISO, and Executive Leadership Team.
* **Cross-Functional Escalation:** When an incident impacts legal, PR, or regulatory domains, the CISO immediately convenes the Crisis Management Committee.

---

## 7. Evidence Preservation & Chain of Custody
* **Forensic Integrity:** All digital evidence (memory dumps, disk images, firewall logs, packet captures) must be collected in accordance with forensic standards to ensure admissibility in legal proceedings.
* **Chain of Custody:** A strict Chain of Custody log must be maintained for all physical and digital evidence, recording date, time, collector identity, storage location, and transfer details.
* **Tamper-Proof Storage:** Acquired forensic images must be hashed (SHA-256) upon creation and stored in write-once, read-many (WORM) secure repositories.

---

## 8. Communications Protocol
* **Internal Communication:** Managed via out-of-band secure channels (encrypted messaging or dedicated bridge lines) to prevent interception by threat actors.
* **External Communication:** Public statements, media releases, and customer notifications may only be authorized and issued by the Corporate Communications Lead and Legal Counsel. Unauthorized employee commentary on social media or to the press is strictly prohibited.

---

## 9. Regulatory & Statutory Considerations
* **UAE PDPL Compliance:** Data breaches involving personal data of UAE residents must be reported to the UAE Data Office without undue delay and in accordance with statutory deadlines.
* **NCA ECC Mandates:** Critical infrastructure incidents must be reported to the National Cyber Security Center (NCA) operational centers per national cybersecurity guidelines.
* **Law Enforcement Engagement:** Engagement with police cybercrime divisions or international law enforcement must be coordinated strictly through Legal Counsel and executive leadership.

---

## 10. Post-Incident Review & Reporting
* **Root Cause Analysis (RCA):** Within 5 business days following incident closure, the IRT must complete a comprehensive RCA detailing vector analysis, dwell time, and impact assessment.
* **Corrective Action Plan (CAPA):** Preventative controls and remediation tasks identified during the review must be logged in the enterprise GRC register and tracked to completion.

---

## 11. Document Version History
| Version | Effective Date | Author / Editor | Summary of Changes |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-02-20 | SOC Team | Initial incident response framework release. |
| v2.0 | 2024-02-20 | CISO Office | Updated severity triage SLAs and forensic evidence protocols. |
| v3.1 | 2025-02-20 | GRC Team | Annual revision incorporating UAE PDPL breach notification timelines. |
