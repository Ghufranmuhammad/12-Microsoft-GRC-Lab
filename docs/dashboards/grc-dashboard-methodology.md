# GRC Dashboard Methodology

## 1. Risk Scoring Methodology

DesertTech Solutions uses a simple 5x5 risk scoring model.

### Likelihood

Likelihood measures how probable it is that a risk will occur.

| Score | Rating | Description |
|---|---|---|
| 1 | Rare | Very unlikely to occur |
| 2 | Unlikely | Could occur but not expected |
| 3 | Possible | Could reasonably occur |
| 4 | Likely | Expected to occur |
| 5 | Almost Certain | Expected to occur frequently |

### Impact

Impact measures the potential business consequence if the risk occurs.

| Score | Rating | Description |
|---|---|---|
| 1 | Insignificant | Minimal business effect |
| 2 | Minor | Limited disruption or loss |
| 3 | Moderate | Noticeable business impact |
| 4 | Major | Significant operational, financial or compliance impact |
| 5 | Severe | Major business disruption, serious data exposure or regulatory consequences |

### Risk Score

Risk Score = Likelihood × Impact

Example:

Likelihood = 4  
Impact = 5

Risk Score = 4 × 5 = 20

---

## 2. Risk Rating

| Score | Rating |
|---:|---|
| 1–4 | Low |
| 5–9 | Medium |
| 10–16 | High |
| 17–25 | Critical |

### Example

A risk with:

Likelihood = 4  
Impact = 5

Score = 20

Rating = Critical

Critical and High risks should receive priority treatment and management attention.

---

# 3. KRI Thresholds

Key Risk Indicators (KRIs) provide early warning when risk conditions are changing.

The dashboard uses:

| Status | Meaning |
|---|---|
| Green | Within acceptable threshold |
| Amber | Warning level; management attention required |
| Red | Threshold exceeded; immediate action required |

### Example — Critical Vulnerabilities

| KRI | Green | Amber | Red |
|---|---:|---:|---:|
| Critical vulnerabilities overdue | 0–2 | 3–5 | >5 |
| Privileged accounts without MFA | 0 | 1 | >1 |
| Overdue security training | <5% | 5–10% | >10% |
| High-risk vendors without assessment | 0–1 | 2–3 | >3 |
| Failed backup tests | 0 | 1 | >1 |

Thresholds should be reviewed periodically based on organizational risk appetite.

---

# 4. Control Effectiveness

Controls are assessed according to their design, implementation and operating effectiveness.

## Effective

A control is:

- Properly designed
- Implemented
- Operating consistently
- Supported by appropriate evidence
- Producing the expected result

Example:

100% of privileged accounts have MFA and configuration evidence confirms enforcement.

## Partially Effective

A control exists but has weaknesses.

Examples:

- Some users are covered but others are not.
- Reviews are performed but evidence is incomplete.
- A control works but not consistently.

Example:

95% of privileged accounts have MFA while several accounts remain outside the control without documented exceptions.

## Ineffective

A control is absent, poorly designed, not implemented, or consistently failing.

Example:

The organization has a backup policy but has never tested whether critical systems can actually be restored.

---

# 5. Audit Finding Status

## Open

The finding has been identified but corrective action has not yet started.

## In Progress

Management has accepted the finding and remediation activities are underway.

## Overdue

The agreed target date has passed and the finding remains unresolved.

## Closed

Corrective action has been completed and sufficient evidence has been provided.

Where appropriate, GRC should verify the effectiveness of the corrective action before final closure.

---

# 6. Dashboard Governance

The GRC Analyst should:

1. Collect current risk and control information.
2. Validate evidence.
3. Update dashboard metrics.
4. Investigate significant changes.
5. Escalate Red KRIs.
6. Track overdue remediation.
7. Report material changes to management.
8. Maintain an evidence trail for reported metrics.

The dashboard should support decision-making rather than simply display numbers.

---

# GRC Principle

A good dashboard answers five questions:

**What is the risk?**

**How serious is it?**

**Are controls working?**

**What requires management attention?**

**What should we do next?**
