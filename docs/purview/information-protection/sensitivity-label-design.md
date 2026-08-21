# Data Classification Design

## 1. Sensitivity Label Architecture

### Public
* **Purpose:** Governs information intended for unrestricted external distribution and public consumption.
* **Example Data:** Marketing brochures, public-facing press releases, open website content.
* **Who Can Access:** Unrestricted (General Public and all internal employees).
* **Sharing Restrictions:** None; can be freely shared externally without tracking.
* **Encryption Requirement:** None.
* **Retention Consideration:** Retain for 1 year post-publication, then archive or delete.
* **Business Owner:** Marketing / Corporate Communications Director.
* **Example Evidence:** Published PDF product sheets, marketing assets repo.

### Internal
* **Purpose:** Protects general operational day-to-day business data not meant for public release but safe for all staff.
* **Example Data:** Internal company policies, general announcements, office memos, non-sensitive operational procedures.
* **Who Can Access:** All authenticated active employees and verified contractors.
* **Sharing Restrictions:** Internal sharing only; external sharing blocked unless explicitly approved by a manager.
* **Encryption Requirement:** Optional / Standard transport encryption (TLS).
* **Retention Consideration:** Retain for 3 years active, then review.
* **Business Owner:** Internal Operations / Human Resources.
* **Example Evidence:** Employee handbook, standard operating procedures (SOPs) PDF.

### Confidential
* **Purpose:** Restricts access to sensitive business-critical or proprietary information that could cause financial or reputational harm if leaked.
* **Example Data:** Customer contracts, vendor master agreements, financial reports, architectural schematics.
* **Who Can Access:** Authorized business units, specific project groups, and management line-of-sight.
* **Sharing Restrictions:** Restricted sharing; external sharing requires explicit rights management (RMS) and domain restrictions.
* **Encryption Requirement:** Mandatory encryption (AES-256) via Purview Sensitivity Label.
* **Retention Consideration:** Retain for 7 years to meet statutory financial and legal compliance standards.
* **Business Owner:** Legal Counsel / Chief Financial Officer (CFO).
* **Example Evidence:** Executed MSAs, audited financial balance sheets.

### Highly Confidential
* **Purpose:** Imposes maximum containment controls on mission-critical assets whose compromise represents an existential or severe regulatory risk.
* **Example Data:** Employee payroll records, unreleased source code, board meeting minutes, passport/identity data scans, credential databases.
* **Who Can Access:** Strictly compartmentalized "Need-to-Know" basis (e.g., C-Suite, Payroll Administrators, Lead Security Engineers).
* **Sharing Restrictions:** Strict prohibition on external sharing; printing, copying, and forwarding restricted via Rights Management Services (RMS).
* **Encryption Requirement:** Strongest encryption with enforced user authentication checks and revocation capability.
* **Retention Consideration:** Retain permanently or per statutory labor/tax laws (e.g., 10+ years).
* **Business Owner:** Chief Information Security Officer (CISO) / Head of HR.
* **Example Evidence:** Encrypted payroll ledger spreadsheets, privileged access management configuration files.

