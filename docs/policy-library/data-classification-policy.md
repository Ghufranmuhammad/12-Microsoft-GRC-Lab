# Enterprise Data Classification Policy

**Document ID:** `POL-005`  
**Version:** v2.2  
**Effective Date:** April 10, 2025  
**Review Date:** April 10, 2026  
**Classification:** Confidential  
**Status:** Active  
**Policy Owner:** Chief Information Security Officer (CISO) & Data Protection Officer (DPO)  
**Approver:** Executive Leadership Team & IT Steering Committee  

---

## 1. Purpose
The Data Classification Policy establishes a standardized framework for categorizing enterprise information assets based on their sensitivity, business value, and regulatory criticality. Proper classification ensures that appropriate administrative, technical, and physical security controls are applied throughout the information lifecycle to protect against unauthorized disclosure, alteration, or destruction, in full compliance with ISO/IEC 27001 and the UAE Personal Data Protection Law (UAE PDPL).

---

## 2. Scope
This policy applies to all information assets owned, processed, transmitted, or stored by the enterprise, regardless of format (electronic, physical, cloud-hosted, or paper-based) across all business units and operational locations.

---

## 3. Data Classification Tiers
Information assets are categorized into four distinct hierarchical classification levels:

### 3.1 Public
* **Definition:** Information intended for unrestricted public consumption where unauthorized disclosure poses zero risk to enterprise operations, legal standing, or brand reputation.
* **Examples:** Marketing brochures, public press releases, published corporate financial reports, website content, and public job postings.
* **Who Can Access:** Unrestricted access for internal personnel and the general public.
* **Storage Requirements:** Stored on public-facing web servers, public cloud storage buckets, or marketing repositories with standard integrity controls.
* **Transmission Requirements:** Can be transmitted freely over public networks and email without encryption requirements.
* **Disposal Requirements:** Standard deletion or recycling; no special sanitization required.
* **Handling Requirements:** Must maintain brand accuracy and official corporate authorization prior to external release.

---

### 3.2 Internal
* **Definition:** Routine business operational data intended exclusively for internal use by employees and contractors. Unauthorized disclosure could cause minor operational inconvenience but negligible damage.
* **Examples:** Internal employee phone directories, general company policies, office memos, non-sensitive project schedules, and internal training materials.
* **Who Can Access:** All active employees, contractors, and authenticated internal personnel.
* **Storage Requirements:** Stored on enterprise internal file shares, company intranet portals, or approved internal cloud repositories.
* **Transmission Requirements:** Transmitted within secure corporate networks or encrypted internal email channels; external transmission requires basic TLS encryption.
* **Disposal Requirements:** Secure digital deletion or shredding of physical paper drafts when no longer required for business operations.
* **Handling Requirements:** Must not be posted to public websites or shared with external parties without prior managerial approval.

---

### 3.3 Confidential
* **Definition:** Sensitive business, financial, or personal data where unauthorized disclosure, modification, or destruction could cause moderate financial loss, regulatory sanction, or reputational harm.
* **Examples:** Strategic business plans, unreleased financial earnings, internal audit reports, proprietary source code, HR personnel files, standard vendor contracts, and non-restricted customer lists.
* **Who Can Access:** Authorized employees and contractors with a verified business need-to-know, managed via role-based access controls (RBAC).
* **Storage Requirements:** Stored in encrypted enterprise databases, restricted SharePoint repositories, and access-controlled file servers with AES-256 encryption at rest.
* **Transmission Requirements:** Encrypted in transit using TLS 1.3 or IPsec VPN; email transmission requires enterprise Data Loss Prevention (DLP) tagging and encryption.
* **Disposal Requirements:** Digital files must be securely shredded using DoD-compliant wiping utilities; physical paper documents must be placed in locked confidential destruction bins for cross-cut shredding.
* **Handling Requirements:** Must bear explicit "Confidential" visual markings on header/footer banners; copying, printing, or local downloading is restricted.

---

### 3.4 Restricted
* **Definition:** Highly sensitive enterprise assets, cryptographic keys, critical infrastructure configurations, and protected personal data (PII) under UAE PDPL where unauthorized exposure would cause catastrophic financial damage, severe legal penalties, or regulatory intervention.
* **Examples:** Passwords, private cryptographic keys, API secrets, M&A negotiation documents, board meeting minutes, national ID numbers, biometric records, health data, and severe security incident forensic reports.
* **Who Can Access:** Strictly limited to named individuals with explicit executive authorization and business justification, governed by strict multi-factor authentication and least privilege.
* **Storage Requirements:** Stored in dedicated, highly isolated secure vaults (e.g., Azure Key Vault, HSM, encrypted air-gapped databases) with mandatory AES-256 encryption and immutable logging.
* **Transmission Requirements:** Encrypted end-to-end using robust cryptographic tunneling (TLS 1.3 with certificate pinning); transmission across public networks without robust encryption is strictly prohibited.
* **Disposal Requirements:** Storage media must be physically degaussed, shredded, or destroyed in accordance with NIST SP 800-88 guidelines; physical records must be witnessed and certified destroyed.
* **Handling Requirements:** Must be watermarked with user tracking identifiers; screen-capture blocking enforced on endpoints; printing or exporting is strictly prohibited without CISO sign-off.

---

## 4. Document Version History
| Version | Effective Date | Author / Editor | Summary of Changes |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-04-10 | GRC Team | Initial data classification framework release. |
| v2.0 | 2024-04-10 | CISO Office | Added cloud storage security tiers. |
| v2.2 | 2025-04-10 | Data Protection Officer | Annual review and UAE PDPL alignment for Restricted data. |

