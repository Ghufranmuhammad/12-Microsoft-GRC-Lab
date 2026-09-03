# Vendor Risk Management (VRM) Methodology

## 1. Vendor Identification
All third-party vendors, suppliers, and service providers must be identified and cataloged in the Central Vendor Risk Register prior to contract execution or data access provisioning. Business unit owners are responsible for notifying the Governance, Risk, and Compliance (GRC) team during the procurement intake process.

## 2. Inherent Risk Evaluation
Inherent risk is evaluated prior to assessing existing controls. It is determined by crossing the **Data Sensitivity Classification** (Public, Internal, Confidential, Restricted) with the **Service Criticality** (Operational, Business-Critical, Mission-Critical). 
- **Factors evaluated:** Volume of records accessed, regulatory scope (GDPR, HIPAA, etc.), network connectivity, and physical access.

## 3. Due Diligence
Vendors must complete baseline security evaluations relative to their inherent risk tier. Due diligence collection mechanisms include:
- Security questionnaires (Standardized Information Gathering - SIG Lite/Full or proprietary templates).
- Independent third-party audit reports (SOC 2 Type II, ISO 27001 certificates, PCI-DSS Attestation of Compliance).
- Public breach history and financial viability checks.

## 4. Risk Scoring
Risk is quantified using a standard $5 \times 5$ Risk Matrix:
$$\text{Risk Score} = \text{Impact} \times \text{Likelihood}$$
- **Low:** 1 to 6
- **Medium:** 8 to 12
- **High:** 15 to 20
- **Critical:** 21 to 25

## 5. Contract & Security Requirements
Contractual agreements must incorporate baseline security riders covering:
- Mandatory data protection and privacy clauses (Data Processing Addendums).
- Breach notification SLAs (notification within 46 hours of confirmation).
- Right-to-audit clauses and compliance with regulatory frameworks.
- Data deletion and return protocols upon contract termination.

## 6. Ongoing Monitoring
Vendors are continuously tracked throughout their lifecycle via automated and manual triggers:
- Annual security posture re-assessments.
- Periodic review of compliance certificates (SOC 2 renewals).
- Incident monitoring and security news alerts.
- Performance SLA reviews conducted quarterly.

## 7. Offboarding
Upon contract termination, offboarding procedures are enforced:
- Revocation of all system credentials, API tokens, and network access within 24 hours.
- Certification of data destruction or secure return of organization assets.
- Archiving of historical vendor risk documentation for compliance retention periods.
