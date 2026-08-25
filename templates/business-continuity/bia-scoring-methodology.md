# Business Impact Analysis (BIA) Criticality Scoring Methodology

## 1. Overview
This document defines the quantitative and qualitative scoring methodology used to evaluate and classify the criticality of business processes, supporting systems, and operational functions during a Business Impact Analysis (BIA). The objective is to establish an objective standard for prioritizing resources, recovery strategies, and disaster recovery planning.

---

## 2. Impact Evaluation Factors
Each business process is assessed against five core impact dimensions. Every factor is scored on a standardized scale from **1 (Negligible)** to **5 (Catastrophic)** based on the potential consequences of a prolonged operational disruption:

1. **Financial Impact:** Direct monetary loss, revenue interruption, recovery expenses, and contractual penalties.
2. **Customer Impact:** Number of customers affected, severity of service degradation, and potential customer churn.
3. **Regulatory Impact:** Breach of statutory laws, contractual compliance failures, regulatory fines, and legal liabilities.
4. **Operational Impact:** Degree of internal workflow disruption, inability to deliver core products/services, and reliance on manual workarounds.
5. **Reputation Impact:** Negative public perception, brand erosion, media scrutiny, and loss of market trust.

---

## 3. Scoring Scale and Tier Classification
The aggregate BIA criticality score is calculated by evaluating the severity across the impact dimensions, yielding an overall tier classification that determines the Recovery Time Objective (RTO) and Recovery Point Objective (RPO) requirements.

* **Low (Score: 5 – 9)**
  * *Characteristics:* Minor operational inconvenience; negligible financial or customer impact; easily absorbed backlogs.
  * *Recovery Target:* RTO $\le$ 72 Hours | RPO $\le$ 24 Hours.

* **Medium (Score: 10 – 16)**
  * *Characteristics:* Noticeable disruption to secondary internal functions; moderate financial impact; temporary workarounds effective.
  * *Recovery Target:* RTO $\le$ 24 Hours | RPO $\le$ 12 Hours.

* **High (Score: 17 – 24)**
  * *Characteristics:* Significant impact on revenue generation or customer service delivery; potential regulatory visibility; operational strain.
  * *Recovery Target:* RTO $\le$ 4 Hours | RPO $\le$ 2 Hours.

* **Critical (Score: 25 – 25)**
  * *Characteristics:* Severe catastrophic consequences; immediate regulatory breach, immense financial loss, complete halt of primary business operations, or major reputational harm.
  * *Recovery Target:* RTO $\le$ 1 Hour | RPO $\le$ 15 Minutes (Near-Zero Downtime).

---

## 4. Scoring Methodology & Calculation
For each business function evaluated during the BIA workshop:
* Assign a score ($1-5$) to each of the 5 impact factors.
* Compute the **Total Criticality Score** as the sum of all factor ratings.
* Map the final aggregate score directly to the corresponding tier (Low, Medium, High, or Critical) to govern recovery tiering and disaster recovery resource allocation.

