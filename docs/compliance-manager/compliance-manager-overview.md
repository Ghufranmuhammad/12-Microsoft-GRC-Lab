# Microsoft Compliance Manager & Purview Overview

## 1. What is Microsoft Purview?
Microsoft Purview is a data governance, risk, and compliance solution family that helps organizations govern, protect, and manage their data estate across on-premises, multi-cloud, and Software-as-a-Service (SaaS) environments.

## 2. What is Compliance Manager?
Microsoft Compliance Manager is a feature in the Microsoft Purview compliance portal that helps simplify compliance and reduce risk. It helps you manage regulatory compliance requirements by building, evaluating, and monitoring control implementations.

## 3. What is an Assessment?
An assessment is a grouping of controls from a specific regulation, standard, or internal policy (e.g., ISO 27001, NIST CSF, GDPR) managed within Compliance Manager. It tracks how well an organization implements the requirements of that standard.

## 4. What is an Improvement Action?
An improvement action is a recommended technical or non-technical task managed within Compliance Manager that helps improve an organization's compliance score by addressing specific control requirements.

## 5. What is Evidence?
Documentation, logs, screenshots, or configuration exports attached to an improvement action to prove to an auditor that a control requirement has been successfully implemented and tested.

## 6. What is a Compliance Score?
A quantitative measurement calculated by Compliance Manager that reflects your organization's progress in completing improvement actions that address recommended controls. 

## 7. Microsoft-managed vs. Organization-managed Actions
* **Microsoft-managed Actions:** Security and compliance controls that Microsoft is entirely responsible for implementing and maintaining in the cloud infrastructure (e.g., physical data center security).
* **Organization-managed Actions:** Controls that the customer (your organization) is responsible for configuring, managing, and evidencing (e.g., user password policies, MFA enforcement).

## 8. Technical vs. Non-Technical Actions
* **Technical Actions:** Controls tested or implemented directly through IT configurations and platform settings (e.g., enabling Conditional Access policies).
* **Non-Technical Actions:** Controls dependent on human processes, policies, physical security, or administrative oversight (e.g., annual employee background checks, written information security policies).

## 9. Preventive vs. Detective vs. Corrective Actions
* **Preventive Actions:** Stop security or compliance failures before they occur (e.g., blocking legacy authentication).
* **Detective Actions:** Identify unwanted events or anomalies after they occur (e.g., reviewing audit log alerts for unauthorized privilege escalation).
* **Corrective Actions:** Fix issues and prevent recurrence after a control failure or security incident has been identified (e.g., patching a vulnerability discovered during a scan).

## 10. Why a GRC Analyst would use Compliance Manager
A GRC analyst uses Compliance Manager to bridge the gap between technical IT configurations and regulatory frameworks. It centralizes control tracking, automates testing of technical controls where possible, streamlines evidence collection for external audits, and provides real-time visibility into risk posture for executive management.

