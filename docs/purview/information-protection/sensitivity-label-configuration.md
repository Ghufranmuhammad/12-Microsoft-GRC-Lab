# Sensitivity Label Configuration Workpaper

## Label Configurations

### Label 1 — Public
* **Scope:** Files, Emails, and Meetings
* **Users:** All internal users and external public
* **Protection:** None (Standard container behaviors)
* **Sharing:** Unrestricted external and internal sharing allowed
* **Business Justification:** Zero friction for external outbound material and public-facing marketing assets.

### Label 2 — Internal
* **Scope:** Files, Emails, and SharePoint Sites
* **Users:** All authenticated employees and contractors
* **Protection:** Standard visual markings (Footer / Header)
* **Sharing:** Internal tenant only; external sharing blocked by default
* **Business Justification:** Prevents baseline accidental oversharing of internal day-to-day operational material.

### Label 3 — Confidential
* **Scope:** Files, Emails, and Container Sites
* **Users:** Authorized business units and management groups
* **Protection:** AES-256 Encryption, RMS access control rights enforcement
* **Sharing:** Restricted/Domain-locked; external sharing requires explicit approval
* **Business Justification:** Protects corporate intellectual property, legal documents, and financial viability.

### Label 4 — Highly Confidential
* **Scope:** Strict File and Email scope
* **Users:** Compartmentalized roles (C-Suite, HR Payroll, Lead Engineering)
* **Protection:** Enforced encryption, view-only or restricted export/print controls
* **Sharing:** Fully blocked externally; strict internal compartmentalization
* **Business Justification:** Mitigates severe data exfiltration risks regarding critical PII, credentials, and source code.

## Deployment Strategy
We deploy using a phased approach (**Pilot → Test → Tune → Deploy**) rather than immediately applying restrictive controls to everyone. Immediate enterprise enforcement without tuning risks blocking vital business processes and generating high user friction. Piloting with a designated GRC team allows compliance analysts to evaluate false-positive friction, adjust encryption conditions, and verify policy propagation safely before enterprise-wide activation.

