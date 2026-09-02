# Enterprise Access Control Policy

**Document ID:** `POL-003`  
**Version:** v2.5  
**Effective Date:** March 12, 2025  
**Review Date:** March 12, 2026  
**Classification:** Confidential  
**Status:** Active  
**Policy Owner:** Identity & Access Management (IAM) Lead & CISO  
**Approver:** Chief Information Security Officer & IT Steering Committee  

---

## 1. Purpose
The Access Control Policy defines the mandatory framework for granting, modifying, reviewing, and revoking access to all enterprise information systems, applications, networks, and data repositories. The objective of this policy is to enforce the principle of least privilege, prevent unauthorized access or data exfiltration, protect sensitive enterprise assets, and ensure full compliance with regulatory standards including ISO/IEC 27001, NCA ECC, and UAE PDPL.

---

## 2. Scope
This policy applies universally to all employees, contractors, consultants, third-party vendors, and system administrators who access or manage enterprise information technology resources across on-premises data centers, cloud environments, and remote working locations.

---

## 3. Least Privilege
* **Minimum Access Principle:** User access rights must be restricted to the absolute minimum permissions necessary to perform specific job duties and authorized business functions.
* **Granular Role Assignment:** Permissions must be assigned based on verified job roles rather than blanket departmental access. Functional roles must be reviewed periodically to ensure scope creep does not violate least privilege.

---

## 4. Need-to-Know
* **Information Segregation:** Access to Confidential and Restricted data repositories is strictly governed by the need-to-know principle.
* **Business Justification:** Individuals may only access information assets when required directly by their assigned tasks. Curiosity-driven browsing or unauthorized access to sensitive records is strictly prohibited and subject to disciplinary action.

---

## 5. User Provisioning
* **Formal Approval Workflow:** New user account creation and permission provisioning must be initiated via an authorized ticketing workflow requiring formal sign-off from the employee's manager and the respective resource owner.
* **Identity Verification:** Prior to granting system access, Human Resources and IT must verify the user's identity, employment status, and background screening requirements.
* **Timely Onboarding:** Provisioning must be completed on or before the employee's official start date, ensuring no pre-employment or unauthorized access occurs.

---

## 6. User Deprovisioning
* **Immediate Revocation:** Access credentials for terminating, resigning, or suspended employees must be revoked immediately upon notice of termination (and no later than 2 hours after employment separation).
* **Automated Sync:** HR exit workflows must automatically trigger account disablement across Active Directory, Microsoft 365, VPN gateways, and cloud SaaS applications.
* **Handover of Assets:** Departing personnel must return all corporate hardware, tokens, and storage media to IT during the exit clearance process.

---

## 7. Privileged Accounts
* **Strict Monitoring:** Privileged accounts (e.g., Domain Admins, Root, Cloud Global Admins) possess extensive system control and are subject to enhanced security controls.
* **Separate Credentials:** Administrators must utilize distinct, non-privileged accounts for daily tasks (such as email and web browsing) and switch to dedicated privileged accounts only when performing administrative operations.
* **Session Recording:** All privileged sessions across critical servers and cloud control planes must be recorded, logged, and audited in real time. Shared administrator accounts are strictly prohibited.

---

## 8. Multi-Factor Authentication (MFA)
* **Universal Mandate:** Multi-Factor Authentication (MFA) is mandatory for all user accounts accessing corporate networks, email, VPN gateways, cloud workloads, and administrative portals.
* **Approved Methods:** Authentication must utilize phishing-resistant methods, including approved authenticator applications (e.g., Microsoft Authenticator) or FIDO2 hardware security keys. SMS-based MFA is prohibited for privileged access.

---

## 9. Access Reviews
* **Quarterly Attestation:** Department managers and system owners must conduct formal quarterly access reviews and recertifications for all assigned user permissions and privileged roles.
* **Revocation of Excess Rights:** Any access rights that are no longer required for current job responsibilities must be revoked immediately during the review attestation cycle.
* **Audit Trail:** Review completion logs and sign-off attestations must be retained for a minimum of 365 days to satisfy internal and external audit requirements.

---

## 10. Service & Non-Human Accounts
* **Strict Inventory:** All service accounts, API keys, daemon accounts, and automated scripts must be registered in the enterprise Identity and Access Management (IAM) inventory.
* **Credential Rotation:** Service account passwords and cryptographic secrets must be automatically rotated every 90 days using enterprise secrets management solutions (e.g., Azure Key Vault, HashiCorp Vault).
* **Hardcoded Credentials:** Embedding plaintext passwords or API keys directly within source code repositories or configuration files is strictly prohibited.

---

## 11. Remote Access
* **Secure VPN Gateway:** Remote access to internal enterprise systems must be tunneled exclusively through authorized corporate VPN gateways enforcing device posture checks and MFA.
* **Split Tunneling Prohibition:** Unauthorized split tunneling is prohibited on corporate VPN sessions to ensure all traffic passes through enterprise security filtering and DLP controls.
* **Unsecured Networks:** Accessing corporate systems from public, unencrypted Wi-Fi hotspots without active VPN protection is strictly prohibited.

---

## 12. Dormant & Orphaned Accounts
* **Inactivity Threshold:** User accounts that remain inactive for 45 consecutive days must be automatically disabled by the IAM system.
* **Purging Lifecycle:** Disabled dormant accounts and accounts belonging to former contractors must be permanently deleted or archived after 90 days of inactivity following formal review.
* **Orphaned Account Audits:** Monthly automated scans must be performed to detect and remediate orphaned user accounts or unassigned resource permissions.

---

## 13. Access Exceptions
* **Formal Exception Request:** Any temporary or permanent deviation from this Access Control Policy requires the submission of an Enterprise Policy Exception Request.
* **Risk Assessment & Approval:** Exceptions must include a documented business justification, risk evaluation, and defined compensating controls, requiring formal approval from the CISO and IT Steering Committee.
* **Time-Bound Expiry:** Policy exceptions must have a strict expiry date not exceeding 6 months. Permanent exceptions are prohibited and must be re-evaluated annually.

---

## 14. Document Version History
| Version | Effective Date | Author / Editor | Summary of Changes |
| :--- | :--- | :--- | :--- |
| v1.0 | 2023-03-12 | IAM Team | Initial access control policy implementation. |
| v2.0 | 2024-03-12 | CISO Office | Updated privileged account monitoring and MFA requirements. |
| v2.5 | 2025-03-12 | GRC Team | Annual review and incorporation of service account secret rotation mandates. |

