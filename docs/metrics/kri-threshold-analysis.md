# Key Risk Indicator (KRI) Threshold Analysis & Action Framework

**Classification:** Confidential / Enterprise GRC Governance  
**Version:** 3.2  
**Owner:** Enterprise Risk Management & Quantitative Analytics Team  

---

## 1. Overview of KRI Threshold Methodology
Key Risk Indicators (KRIs) serve as forward-looking telemetry measuring emerging risk exposure across the enterprise. Each KRI is governed by a strict threshold framework structured around three operational bands:
* **Green (Optimal / Normal Operating Band):** Risk exposure is within established corporate risk appetite and tolerance levels. Normal operational monitoring applies.
* **Amber (Elevated Risk / Warning Band):** Risk exposure is trending outside optimal parameters, signaling potential control degradation or external market pressure. Requires enhanced monitoring and tactical review.
* **Red (Critical Risk / Breach Band):** Risk exposure has exceeded maximum acceptable risk thresholds, posing an immediate threat to operational integrity, financial stability, or compliance mandates. Requires mandatory escalation and immediate executive remediation.
* **Trigger:** The specific quantitative metric value or operational event that forces a status transition from Green to Amber, or Amber to Red.
* **Management Action:** The mandatory governance, engineering, or administrative workflow executed by assigned owners upon threshold breach.

---

## 2. Enterprise KRI Threshold Register

### KRI-01: High & Critical Vulnerabilities Past Remediation SLA
* **Domain:** Vulnerability Management
* **Green Threshold:** 0 to 5 open vulnerabilities past SLA
* **Amber Threshold:** 6 to 15 open vulnerabilities past SLA
* **Red Threshold:** > 15 open vulnerabilities past SLA
* **Trigger:** Daily automated vulnerability scanner ticket count exceeding 15 items aged beyond 30 days.
* **Management Action:** Mandatory engineering sprint reallocation, freeze on non-security feature deployments, and weekly status reporting to the Chief Information Security Officer (CISO).

### KRI-02: Failed Employee Phishing Simulation Rate
* **Domain:** Workforce Security Awareness
* **Green Threshold:** < 3.0% failure rate
* **Amber Threshold:** 3.0% to 7.0% failure rate
* **Red Threshold:** > 7.0% failure rate
* **Trigger:** Monthly phishing simulation metrics reporting a departmental or enterprise click-through rate above 7%.
* **Management Action:** Mandatory remedial interactive security training assigned to failing business units within 48 hours; increased simulation frequency.

### KRI-03: Multi-Factor Authentication (MFA) Bypass Events
* **Domain:** Identity & Access Management (IAM)
* **Green Threshold:** 0 unauthorized bypass events
* **Amber Threshold:** 1 to 2 temporary emergency bypasses without post-review
* **Red Threshold:** > 2 unauthorized bypass events or any unreviewed admin override
* **Trigger:** SIEM alert detecting an administrative account authentication session established without FIDO2 hardware token verification.
* **Management Action:** Immediate revocation of session tokens, freezing of compromised administrative credentials, and initiation of an internal security investigation.

### KRI-04: Third-Party Vendor Risk Assessment Backlog
* **Domain:** Vendor & Supply Chain Risk
* **Green Threshold:** < 5% of active onboarding vendors awaiting assessment
* **Amber Threshold:** 5% to 15% pending assessment
* **Red Threshold:** > 15% pending assessment or onboarding active without security review
* **Trigger:** Procurement pipeline showing more than 15% of active third-party suppliers operating without a completed security questionnaire and risk score.
* **Management Action:** Halt vendor contract execution until GRC sign-off is completed; audit procurement workflows to enforce mandatory security gating.

### KRI-05: Data Subject Access Request (DSAR) Breach of Statutory SLA
* **Domain:** Privacy & Regulatory Compliance
* **Green Threshold:** 100% of requests fulfilled within 30 days (< 1% backlog)
* **Amber Threshold:** 1% to 5% of requests approaching or exceeding statutory 30-day limit
* **Red Threshold:** > 5% of requests overdue past regulatory deadline
* **Trigger:** Privacy team ticketing queue registering overdue consumer data deletion or export requests past the legal 30-day window.
* **Management Action:** Reallocate privacy operations personnel to queue triage; legal risk review initiated for potential regulatory notification requirements.

### KRI-06: Centralized SIEM Log Ingestion Pipeline Delay
* **Domain:** Security Monitoring & Logging
* **Green Threshold:** Log ingestion lag < 5 minutes
* **Amber Threshold:** Log ingestion lag between 5 to 30 minutes
* **Red Threshold:** Log ingestion lag > 30 minutes or complete pipeline outage
* **Trigger:** Infrastructure monitoring alerting that SIEM log collection buffers are delayed beyond 30 minutes, impairing real-time threat detection.
* **Management Action:** DevOps and SOC infrastructure leads paged immediately; failover to secondary ingestion pipeline executed; incident logged for root-cause analysis.

### KRI-07: Unpatched Critical Third-Party Software Dependencies (SBOM)
* **Domain:** Secure Software Development
* **Green Threshold:** 0 critical or high CVEs in active production SBOM
* **Amber Threshold:** 1 to 3 critical CVEs unpatched past 7 days
* **Red Threshold:** > 3 critical CVEs unpatched past 7 days or active exploit in the wild
* **Trigger:** CI/CD software composition analysis (SCA) pipeline identifying unpatched library vulnerabilities exceeding acceptable severity windows.
* **Management Action:** Immediate emergency dependency patching sprint; if patch unavailable, enforce emergency web application firewall (WAF) virtual patching rules.

### KRI-08: Backup Restoration Test Failure Rate
* **Domain:** Business Continuity & Disaster Recovery
* **Green Threshold:** 100% successful quarterly restoration drill pass rate
* **Amber Threshold:** Single non-critical database or file store restoration failure requiring script tweak
* **Red Threshold:** Core mission-critical database restoration failure during scheduled drill
* **Trigger:** Quarterly disaster recovery test resulting in inability to restore Tier 1 core ledger data within the RTO window.
* **Management Action:** Immediate escalation to Infrastructure Reliability Lead; freeze database architecture changes until backup integrity is re-validated through a fresh drill.

### KRI-09: Unresolved High-Severity Internal Audit Findings
* **Domain:** Internal Audit & Governance
* **Green Threshold:** 0 overdue high-severity audit findings past agreed remediation date
* **Amber Threshold:** 1 to 2 overdue audit findings past deadline by < 30 days
* **Red Threshold:** > 2 overdue audit findings past deadline by > 30 days
* **Trigger:** GRC audit tracking system flagging management action items that have missed agreed remediation milestones by more than 30 days.
* **Management Action:** Formal notification sent to executive committee and business unit owner; mandatory status defense presentation required at the next Audit Committee meeting.

### KRI-10: Monthly Cloud Infrastructure Cost & Resource Anomalies
* **Domain:** Financial & Operational Risk
* **Green Threshold:** Monthly spend variance within +/- 5% of forecasted budget
* **Amber Threshold:** Monthly spend variance between 5% to 20% above forecast
* **Red Threshold:** Monthly spend variance > 20% above forecast or sudden unexplained compute spike
* **Trigger:** Cloud billing anomaly detector signaling unexpected resource provisioning spikes that could indicate compromised compute assets (e.g., unauthorized crypto mining).
* **Management Action:** FinOps and cloud security teams review AWS/Azure resource allocation logs; shutdown unapproved compute instances and audit IAM roles.

