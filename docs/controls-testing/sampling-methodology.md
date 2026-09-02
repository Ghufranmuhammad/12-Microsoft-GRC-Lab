# Enterprise GRC Control Testing Sampling Methodology

**Document ID:** `SMP-001`  
**Version:** v2.0  
**Effective Date:** August 2026  
**Classification:** Confidential  
**Framework Alignment:** ISO/IEC 27001:2022, NIST SP 800-53 Rev. 5, AICPA Audit Standards  

---

## 1. Purpose & Scope
This document defines the statistical and judgmental sampling methodology utilized by internal audit and GRC teams when testing internal controls. Because testing 100% of operational transactions is frequently impractical or impossible, sampling allows auditors to evaluate a representative subset of a population to draw valid conclusions regarding control operating effectiveness. *Note: Audit sampling provides reasonable assurance but does not prove absolute compliance or guarantee that zero operational exceptions exist across the unexamined population.*

---

## 2. Core Sampling Concepts & Terminology

### 2.1 Population
* **Definition:** The entire set of data items, transactions, user accounts, or control executions from which a sample is drawn and to which the auditor wishes to generalize conclusions.
* **Requirements:** The population must be complete, accurate, and relevant to the control objective being tested.

### 2.2 Sample
* **Definition:** A subset of sampling units selected from the broader population representing a specific audit period.
* **Requirements:** The sample size must be sufficient to support a defensible conclusion regarding control operating effectiveness.

### 2.3 Sampling Period
* **Definition:** The specific timeframe (e.g., Q1–Q4, monthly, annual) covered by the population and sample selection.
* **Requirements:** Must align with the audit scope window and control frequency (e.g., daily controls require larger populations than annual controls).

### 2.4 Sample Selection Techniques
* **Random Sampling:** Every item in the population has an equal and independent chance of being selected (e.g., generated via cryptographic pseudo-random number generators). This eliminates selection bias and supports statistical inference.
* **Judgmental (Risk-Based) Sampling:** The auditor uses professional experience, risk weighting, and qualitative factors (e.g., high-risk accounts, offshore vendors, peak transaction volumes) to select specific items. While not statistically projectable, judgmental sampling targets known vulnerability areas.

### 2.5 Why Sampling is Used
* **Efficiency & Pragmatism:** Evaluating millions of daily log events, user access entries, or firewall modifications across large enterprises is resource-prohibitive.
* **Reasonable Assurance:** Statistical and risk-based sampling provides sufficient, appropriate audit evidence to form a professional opinion on control effectiveness without incurring prohibitive operational delays.

### 2.6 Sampling Limitations
* **Sampling Risk:** The risk that the auditor's conclusion based on a sample differs from the conclusion that would reach the entire population if 100% testing were performed.
* **Non-Absolute Assurance:** Finding zero exceptions in a sample of 25 items indicates high operational reliability, but it does **not** prove absolute 100% compliance across the unexamined population.

---

## 3. Fictional Sampling Examples

### Example 1: User Access Review Population (Random Sampling)
* **Control:** Quarterly user access recertification (`CTRL-003`).
* **Population:** 120 user access review attestation sheets completed across Q1–Q2 2026.
* **Sample Size:** 15 review sheets.
* **Selection Method:** Random sampling utilizing a computerized random number generator.
* **Rationale & Explanation:** Random sampling was selected to ensure unbiased coverage across all departments and system tiers. Evaluating 15 randomly selected reviews provides sufficient evidence to assess whether managers are actively performing recertifications without selection bias. *Result note: This sample supports a finding of operational reliability but does not guarantee that every single unexamined review sheet was executed perfectly.*

### Example 2: Privileged Account Population (Judgmental / Risk-Based Sampling)
* **Control:** Privileged access management and session monitoring (`CTRL-002`).
* **Population:** 50 active privileged administrator and service accounts in the enterprise vault.
* **Sample Size:** 10 accounts.
* **Selection Method:** Judgmental (risk-weighted) sampling focusing on global domain administrators, external contractor admin accounts, and non-expiring service accounts.
* **Rationale & Explanation:** Rather than selecting accounts randomly (which might heavily sample low-risk standard IT admin accounts), judgmental sampling targeted high-privilege, high-risk accounts where the impact of unauthorized compromise is catastrophic. This approach maximizes audit efficiency in uncovering configuration anomalies.

### Example 3: Firewall Change Ticket Population (Stratified Sampling)
* **Control:** Network firewall change management and authorization review (`CTRL-014`).
* **Population:** 300 firewall modification tickets submitted over a 6-month period.
* **Sample Size:** 30 tickets (stratified: 15 standard change tickets, 15 emergency/after-hours change tickets).
* **Selection Method:** Stratified random sampling.
* **Rationale & Explanation:** Emergency and after-hours firewall changes carry significantly higher risk than standard daytime maintenance. Stratifying the population ensures that high-risk emergency changes are adequately represented in the sample, allowing auditors to test whether emergency authorization protocols were strictly followed.

