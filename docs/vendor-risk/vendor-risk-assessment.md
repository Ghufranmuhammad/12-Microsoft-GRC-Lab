# Vendor Risk Assessment Report

## Vendor Profile
- **Vendor ID:** VEN-001
- **Service Name:** NexusCloud Financial ERP
- **Data Handled:** Restricted (Financial records, corporate tax data, employee banking PII)
- **Business Criticality:** Critical
- **Assessment Date:** January 15, 2026

## 1. Inherent Risk
- **Inherent Risk Level:** High
- **Justification:** The vendor processes mission-critical financial data and stores restricted PII and financial ledger information, exposing the organization to heavy regulatory compliance burdens and financial loss if compromised.

## 2. Security Controls Evaluated
- SOC 2 Type II certification verified and valid for the current review period.
- Data encrypted at rest (AES-256) and in transit (TLS 1.3).
- Mandatory hardware-token based MFA enforced for all system administrator logins.
- Role-based access controls mapped to operational job descriptions.

## 3. Identified Gaps & Weaknesses
- **Gap 1:** Vendor backup restoration testing results are documented via summary tables only, lacking raw verification logs.
- **Gap 2:** The vendor's standard sub-processor notification policy offers only 14 days' notice for infrastructure changes, which is below our internal 30-day requirement.

## 4. Residual Risk
- **Residual Risk Level:** Medium
- **Justification:** While core cryptographic and access controls are mature, the sub-processor notification timeline and lack of raw backup validation evidence leave minor operational gaps.

## 5. Recommendation & Decision
- **Recommendation:** **Approve with Conditions**
- **Action Items:** Execute a customized contract addendum extending sub-processor notification terms to 30 days, and require annual submission of signed backup restoration test certificates.

