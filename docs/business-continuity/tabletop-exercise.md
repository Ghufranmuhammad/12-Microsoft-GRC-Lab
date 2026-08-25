# Business Continuity Tabletop Exercise: Major Cloud Outage Scenario

## 1. Exercise Overview & Scenario Timeline
* **Scenario:** Major Cloud-Hosted Platform Outage
* **Location:** UAE Operations (Abu Dhabi / Dubai)
* **Timeline of Events:**
  * **08:30 UAE Time:** The company's primary cloud-hosted customer platform becomes completely unavailable. Automated monitoring alerts trigger in the SIEM.
  * **09:00 UAE Time:** Customers are unable to access their accounts; customer support experiences a surge of complaints; finance cannot process payroll or incoming payments; IT identifies a potential cloud service provider outage; negative social media posts begin to climb.
  * **10:00 UAE Time:** The outage is officially confirmed by the Cloud Hosting Provider (Microsoft Azure) as a major regional service disruption requiring emergency failover procedures.

---

## 2. Tabletop Scenario Response Structure

### 1. Detection
* **Who detects it?** 
  * Automated cloud monitoring probes and SIEM health checks detect service degradation at 08:30.
  * Internal staff and Customer Support agents identify the outage via failed user logins at 09:00.

### 2. Escalation
* **Who is notified?**
  * The On-Call DevOps Engineer and Lead System Administrator are immediately notified via automated PagerDuty/SMS alerts at 08:30.
  * The Incident Commander (CISO) and Operations Lead (COO) are briefed at 09:00 upon confirmation of widespread business impact.
  * The Crisis Director (CEO) and Crisis Management Team (CMT) are formally convened at 10:00 upon confirmation of a major service disruption.

### 3. Activation
* **When is the BCP activated?**
  * The Business Continuity Plan (BCP) and Disaster Recovery Plan (DRP) are officially activated at **10:00 UAE time** by the Crisis Director, following the confirmation that the cloud outage exceeds the 30-minute operational tolerance threshold.

### 4. Communication Plan
* **Employees:** Internal broadcast dispatched via Microsoft Teams and emergency SMS to all staff detailing the incident status, remote work advisories, and next steps within 15 minutes of BCP activation.
* **Customers:** Transparent status updates published on the public status page and social media channels by 10:30, directing users to backup support communication lines.
* **Management:** Mandatory 30-minute status briefings held by the CMT throughout the duration of the emergency response.
* **Regulators (if applicable):** UAE Data Protection Office and Central Bank notified within regulatory windows if transaction processing or sensitive data availability is severely compromised.
* **Suppliers:** Primary cloud infrastructure vendor (Microsoft Azure support) engaged via priority enterprise bridge; primary clearing bank notified of potential WPS payroll submission delays.

### 5. Recovery Priorities (What gets restored first?)
* **Priority 1 (0–30 Mins post-activation):** Identity & Access Management (CIAM) authentication services to re-establish secure gateway access.
* **Priority 2 (30–60 Mins):** Core database replication promotion to restore transaction processing and WPS payroll execution capabilities.
* **Priority 3 (1–2 Hours):** Customer Support ticketing hubs and secondary operational applications.

### 6. Decision Points (What decisions must management make?)
* Whether to authorize the manual promotion of secondary geo-replicated database instances and forfeit any uncommitted transaction delta.
* Approving public communication releases and managing brand reputation impacts on social media.
* Authorizing the activation of secondary operational workarounds and third-party supplier escalation pathways.

### 7. Recovery Validation (How do you know the service is recovered?)
* Successful execution of automated synthetic end-to-end transaction test scripts verifying user login, database write capabilities, and API responsiveness.
* Zero error rates reported across primary cloud monitoring dashboards for 30 consecutive minutes.
* Formal sign-off from both the Lead Database Administrator and the CISO.

### 8. Lessons Learned (What went wrong?)
* Initial communication lag between technical IT responders and customer support teams caused conflicting messaging to be sent to clients.
* Manual notification bottlenecks delayed public status page updates during the initial 09:00–10:00 window.

### 9. Corrective Actions (What should change?)
* Automate public status page triggers to update directly from SIEM health probe failures.
* Conduct specialized customer support crisis communication training to streamline external messaging during high-stress outages.
* Update emergency contact trees to reduce CMT convening time from 60 minutes down to 30 minutes.

