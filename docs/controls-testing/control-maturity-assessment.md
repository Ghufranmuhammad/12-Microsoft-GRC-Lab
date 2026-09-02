# Enterprise GRC Control Maturity Assessment Register

**Document ID:** `CMA-001`  
**Version:** v2.0  
**Effective Date:** August 2026  
**Classification:** Confidential  
**Framework Alignment:** CMMI Maturity Model, ISO/IEC 27001:2022, NIST SP 800-53 Rev. 5  

---

## 1. Executive Summary
This document establishes the baseline maturity ratings, supporting test evidence, qualitative justification rationales, target maturity levels, and strategic improvement paths for ten core enterprise controls across the governance, risk, and compliance framework. Maturity levels are rated on a standard 1-to-5 scale:
1. **Initial** (Ad-hoc, manual, reactive)
2. **Developing** (Partially documented, inconsistent execution)
3. **Defined** (Standardized, documented, and consistently executed)
4. **Managed** (Quantitatively measured, monitored, and integrated)
5. **Optimized** (Automated, continuously improving, adaptive)

---

## 2. Control Maturity Assessments

### Control 1: Multi-Factor Authentication (MFA) Enforcement (`CTRL-001`)
* **Current Level:** 4 — Managed
* **Evidence:** Entra ID Conditional Access policy configurations, block logs for legacy protocols, and 100% active user sign-in verification reports.
* **Reason:** MFA enforcement is centrally automated and monitored across all user accounts with zero legacy protocol bypasses, though minor gaps existed in break-glass account hardware token provisioning.
* **Target Level:** 5 — Optimized
* **Improvement:** Transition 100% of emergency break-glass and administrative accounts to continuous device-trust validation and automated risk-based adaptive step-up authentication.

---

### Control 2: Privileged Access Management & Session Vault (`CTRL-002`)
* **Current Level:** 3 — Defined
* **Evidence:** CyberArk/Entra ID privileged session recording logs, vault check-out registers, and role-based access control (RBAC) definitions.
* **Reason:** Privileged access is restricted and recorded through standardized vault procedures, but session auditing relies on periodic manual sampling rather than real-time AI anomaly detection.
* **Target Level:** 4 — Managed
* **Improvement:** Integrate real-time behavioral analytics and automated session termination triggers for anomalous privileged command execution.

---

### Control 3: Quarterly Privileged Access Review (`CTRL-003`)
* **Current Level:** 2 — Developing
* **Evidence:** Q1 and Q2 Entra ID Identity Governance campaign exports and attestation sign-off logs showing service account omission exceptions.
* **Reason:** While human privileged accounts are reviewed quarterly, the workflow failed to include non-human service principals in the attestation scope, reflecting an incomplete population design.
* **Target Level:** 4 — Managed
* **Improvement:** Expand automated identity governance campaigns to dynamically include all service principals, API keys, and machine identities with mandatory automated revocation.

---

### Control 4: Automated Joiner-Mover-Leaver (JML) Provisioning (`CTRL-004`)
* **Current Level:** 3 — Defined
* **Evidence:** HRIS webhook configuration logs, Active Directory provisioning scripts, and automated disable timestamp records.
* **Reason:** Core employee provisioning and deactivation are fully automated via HRIS integration, but third-party contractor offboarding still relies on manual spreadsheet exception handling.
* **Target Level:** 4 — Managed
* **Improvement:** Fully automate contractor lifecycle integration by connecting third-party vendor management portals directly to the HRIS provisioning gateway.

---

### Control 5: Vulnerability Management & Patching Cadence (`CTRL-006`)
* **Current Level:** 3 — Defined
* **Evidence:** Monthly vulnerability scanner reports (Defender for Endpoint / Tenable), patching schedules, and remediation ticket logs.
* **Reason:** Vulnerability scans run regularly and patches are applied according to defined SLAs, but patching verification is tracked via periodic reports rather than automated pipeline gating.
* **Target Level:** 4 — Managed
* **Improvement:** Implement continuous vulnerability scoring tied directly to automated patch deployment validation gates in staging and production environments.

---

### Control 6: Daily Automated Server Backups & Immutability (`CTRL-009`)
* **Current Level:** 4 — Managed
* **Evidence:** Veeam backup job success logs, immutability lock verification reports, and monthly isolated test restore validation certificates.
* **Reason:** Backups execute nightly with immutable storage protections and verified restoration capabilities, though alerting routes to general email distribution lists instead of SOC paging queues.
* **Target Level:** 5 — Optimized
* **Improvement:** Integrate backup failure and anomaly alerts directly into the PagerDuty 24/7 SOC incident management matrix with automated sandbox recovery testing.

---

### Control 7: Third-Party Vendor Security Risk Assessment (`CTRL-011`)
* **Current Level:** 2 — Developing
* **Evidence:** Vendor Risk Register, SIG Lite questionnaire files, and manual spreadsheet review schedules.
* **Reason:** Pre-engagement vendor assessments are performed, but ongoing annual re-assessments lack automated tracking and enforcement, resulting in overdue review lapses.
* **Target Level:** 4 — Managed
* **Improvement:** Deploy an automated GRC vendor risk portal featuring automated annual re-assessment triggers, continuous risk rating feeds, and mandatory procurement gating.

---

### Control 8: Network Firewall Change Management (`CTRL-014`)
* **Current Level:** 3 — Defined
* **Evidence:** Firewall change tickets, change advisory board (CAB) approval sign-offs, and rule review logs.
* **Reason:** Firewall modifications follow a formal CAB approval and documentation workflow, but rule review periodicity is audited manually rather than enforced via automated firewall rule analyzers.
* **Target Level:** 4 — Managed
* **Improvement:** Implement automated firewall rule lifecycle management tools to flag redundant, overly permissive, or stale firewall rules automatically.

---

### Control 9: Cloud Storage Asset Tagging & Classification (`CTRL-018`)
* **Current Level:** 2 — Developing
* **Evidence:** Cloud Security Posture Management (CSPM) compliance reports and storage bucket metadata inventories.
* **Reason:** Production cloud buckets maintain proper data classification tags, but development and sandbox environments frequently bypass asset tagging guidelines during rapid provisioning.
* **Target Level:** 4 — Managed
* **Improvement:** Enforce mandatory Infrastructure-as-Code (IaC) linting and CI/CD pipeline blocking policies to prevent untagged resource deployment.

---

### Control 10: Information Security Policy Governance & Annual Review (`CTRL-022`)
* **Current Level:** 3 — Defined
* **Evidence:** Enterprise policy repository, version control logs, and CISO approval sign-off documentation.
* **Reason:** Core security policies are formally documented and approved, but the annual review tracking mechanism experienced administrative oversight during intranet repository migration.
* **Target Level:** 4 — Managed
* **Improvement:** Implement an automated policy lifecycle management platform with automated review reminders, version tracking, and mandatory employee attestation tracking.
