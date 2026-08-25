# Enterprise Business Continuity Plan (BCP)
**Organization:** Apex Financial Services (UAE Operations)  
**Version:** 2.4 | **Status:** Active & Approved  

---

## 1. Purpose
This Business Continuity Plan (BCP) establishes the operational procedures, communication protocols, and recovery strategies required to maintain or rapidly resume critical business functions following a severe disruption, disaster, or cyber incident affecting UAE operations.

## 2. Scope
This plan applies to all operational units, cloud infrastructure, local offices, employees, and contracted third-party suppliers supporting Apex Financial Services within the United Arab Emirates.

## 3. Critical Services
The organization has identified four core operations requiring immediate continuity prioritization:
1. **Core Payment & Payroll Disbursement Processing (WPS)** (RTO: 1 Hour | RPO: 15 Mins)
2. **Customer Identity & Access Management (CIAM)** (RTO: 30 Mins | RPO: 0 Mins)
3. **Enterprise Customer Support & Ticketing Hub** (RTO: 2 Hours | RPO: 1 Hour)
4. **Regulatory Compliance & Audit Reporting Engine** (RTO: 4 Hours | RPO: 24 Hours)

## 4. Activation Criteria
The BCP is officially activated when any of the following triggers occur:
* A catastrophic cloud tenant or regional data center outage exceeding 30 minutes.
* A confirmed ransomware attack locking critical production databases.
* A physical or facility disaster rendering the primary corporate office uninhabitable.
* Direct mandate from executive leadership or regulatory authorities (e.g., UAE Central Bank / Data Protection Office).

## 5. Crisis Management Team (CMT)
The CMT directs all recovery operations during an emergency:
* **Crisis Director (CEO):** Overall command, strategic decision-making, and regulatory liaison.
* **Incident Commander (CISO):** Technical containment, security assessment, and IT recovery direction.
* **Operations Lead (COO):** Business process resumption and alternate workflow management.
* **Communications Lead (Head of PR/HR):** Internal staff welfare and external stakeholder messaging.

## 6. Roles & Responsibilities
* **Crisis Director:** Declares disaster status, authorizes budget allocations, and approves external public notifications.
* **Incident Commander:** Coordinates IT disaster recovery (DRP) teams and liaises with cloud hosting providers.
* **Operations Lead:** Manages department-level business continuity liaisons and resource allocation.
* **Communications Lead:** Dispatches emergency alerts via SMS/email and handles media inquiries.

## 7. Communication Protocols
* **Internal Alerting:** Immediate automated broadcast via Microsoft Teams emergency channel and SMS blast to all staff.
* **Status Updates:** Mandatory 30-minute briefings held by the CMT during active crisis response.
* **External Stakeholders:** Regulators and key corporate clients notified within 24 hours in accordance with contractual SLAs and UAE compliance mandates.

## 8. Recovery Priorities
* **Phase 1 (0–1 Hour):** Life safety verification, containment of threats, and activation of critical IT database replicas.
* **Phase 2 (1–4 Hours):** Resumption of payment processing and core customer authentication channels.
* **Phase 3 (4–24 Hours):** Restoration of customer support desks, secondary business applications, and reporting tools.

## 9. Alternate Work Arrangements
* **Remote Work Transition:** All staff equipped with company-managed laptops, encrypted VPN clients, and multi-factor authentication can transition immediately to 100% remote operations within 1 hour of notice.
* **Secondary Office Hub:** Designated warm-site fallback facility located in Dubai Internet City for executive and critical finance operations if primary Abu Dhabi headquarters is compromised.

## 10. Supplier Dependencies
* **Cloud Infrastructure Provider (Microsoft Azure):** Relies on automated geo-replication and regional failover zones.
* **Primary Clearing Bank:** Direct communication channels established for emergency WPS payroll file submissions.
* **Telecommunications Carrier:** Redundant fiber and cellular backup links active for customer support centers.

## 11. Recovery Procedures
1. **Assess & Declare:** Incident Commander verifies disruption severity and briefs Crisis Director.
2. **Invoke Technical DRP:** Database Administrators promote secondary warm-standby database replicas.
3. **Validate Data Integrity:** Run automated validation scripts to check for zero data corruption.
4. **Open Operations:** Route traffic through secondary load balancers and notify departmental leads.

## 12. Testing
* **Frequency:** The BCP is tested at least annually via a combination of tabletop simulations (quarterly) and full technical failover drills (annually).
* **Documentation:** All test results, execution timestamps, and identified gaps are logged in the Business Continuity Register.

## 13. Review & Maintenance
* This BCP is formally reviewed and updated annually by the CISO and Compliance Officer, or immediately following any major security incident, organizational restructuring, or significant technology change.

