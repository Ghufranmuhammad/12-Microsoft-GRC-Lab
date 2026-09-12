# Incident Analysis: Accidental Confidential Document Disclosure

## Detection
* **Discovery Mechanism:** The incident was identified via an automated Data Loss Prevention (DLP) email intercept rule that flagged outbound external sharing of a file containing restricted internal classifications.
* **Secondary Alert:** The external recipient proactively contacted the helpdesk to report receipt of misdirected sensitive material, accelerating time-to-detection.

## Triage
* **Initial Assessment:** The Security Operations Center (SOC) immediately verified the validity of the DLP alert within 15 minutes of transmission, confirming the exact recipient address and file metadata.
* **Scope Determination:** The analysis confirmed that a single internal user attached the wrong draft strategy document to an external email thread, transmitting it to one distinct external recipient domain.

## Severity
* **Classification Level:** Categorized as **Medium Severity** (Data Leakage / Unauthorized External Disclosure).
* **Impact Evaluation:** Evaluated based on data sensitivity (proprietary financial projections and internal product roadmaps) versus blast radius (confined to one external recipient who is an established non-disclosure agreement (NDA) partner).

## Containment
* **Immediate Technical Actions:** The Security Engineer immediately revoked active cloud link-sharing permissions and initiated an automated remote recall request through the email gateway.
* **External Outreach:** Sent a formal secure retraction notice to the external recipient demanding immediate deletion and written attestation of non-retention.

## Evidence
* **Artifact Preservation:** Captured full message headers, SMTP delivery logs, DLP rule match logs, and cloud storage audit trails.
* **Chain of Custody:** Stored all digital logs securely in the SIEM forensic repository with restricted access to support potential legal or regulatory reviews.

## Stakeholders
* **Internal Leadership:** Notified the Chief Information Security Officer (CISO) and the Department Head of the affected business unit within 1 hour of triage verification.
* **External / Legal Partners:** Briefed Corporate Legal Counsel and the Data Protection Officer (DPO) to evaluate contractual and regulatory notification thresholds.

## Privacy Considerations
* **PII Assessment:** Verified that the leaked document contained strictly corporate financial and operational data, with **no** Personally Identifiable Information (PII) or sensitive personal records concerning employees or customers.
* **Regulatory Trigger:** Concluded that mandatory data protection authority notification (e.g., GDPR/CCPA) was not triggered due to the absence of exposed PII.

## Root Cause
* **Primary Factor:** Human error driven by email client auto-complete selecting an incorrect external contact with a similar display name to an internal colleague.
* **Contributing Factor:** Inadequate warning banners or friction in the email client when attaching sensitive classification tags to external domains.

## Corrective Action
* **Immediate Remediation:** Received written confirmation of secure file deletion and non-dissemination from the external recipient within 4 hours.
* **Technical Enforcement:** Updated email gateway policy rules to enforce mandatory manual verification pop-ups whenever a file labeled "Confidential" is addressed to external domains.

## Lessons Learned
* **Training Gaps:** Highlighted the need for reinforced employee awareness regarding email client auto-complete risks and external recipient verification.
* **Process Enhancement:** Recommended accelerating the deployment of cloud-native Information Rights Management (IRM) controls to auto-encrypt sensitive documents by default, neutralizing risk even if misdirected.

