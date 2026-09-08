# Awareness-Related Risk Assessment & Register

**Classification:** Confidential / Enterprise Risk Governance  
**Version:** 3.2  
**Owner:** Enterprise Risk Management & Security Awareness Team  

---

> **FICTIONAL / EDUCATIONAL SIMULATION**  
> *This risk assessment register, along with all associated analysis and remediation workflows, is produced exclusively for fictional and educational simulation purposes within a Governance, Risk, and Compliance (GRC) framework.*

---

## 1. Executive Summary & Methodology
This risk register evaluates human-vector and awareness-related vulnerabilities across the enterprise. Risks are categorized into High, Medium, and Low severity tiers based on likelihood of occurrence and potential business impact. Each entry outlines the root cause, downstream impact, compensating controls, proposed treatment strategies, and designated risk owners.

---

## 2. High-Severity Risks

### 1. High-Frequency Credential Harvesting Compromise
* **Risk:** High susceptibility of employees falling victim to targeted credential-harvesting attacks (phishing/quishing).
* **Cause:** Sophisticated multi-channel lures mimicking corporate SSO portals combined with employee fatigue and urgency bias.
* **Impact:** Unauthorized enterprise network access, lateral movement, potential ransomware deployment, and severe regulatory breach notifications.
* **Existing Control:** Monthly automated phishing simulations, mandatory onboarding training, and basic URL filtering.
* **Treatment:** Implement advanced browser-based anti-phishing isolation tools, deploy FIDO2 hardware security keys for all non-privileged users, and mandate immediate micro-training upon simulation failure.
* **Owner:** Head of Information Security & Identity Operations

### 2. Executive Spear-Phishing (Whaling) Vulnerability
* **Risk:** C-suite executives and board members compromising corporate communications or authorizing fraudulent wire transfers due to bespoke spear-phishing.
* **Cause:** High public profile, accessibility of executive contact details, and delegation of communication tasks to administrative staff.
* **Impact:** Severe financial loss via Business Email Compromise (BEC), compromise of strategic enterprise data, and reputational damage.
* **Existing Control:** General security awareness training and standard email gateway spam rules.
* **Treatment:** Enforce out-of-band secondary voice/video verification protocols for all financial transactions and executive data requests; deploy VIP email tagging and enhanced inbound inspection rules.
* **Owner:** Chief Information Security Officer (CISO) & Corporate Controller

### 3. Untracked Onboarding Training Deficits
* **Risk:** New hires operating corporate systems prior to completing mandatory security and privacy awareness modules.
* **Cause:** Lags in automated provisioning synchronization between Human Resources Management Systems (HRMS) and the Learning Management System (LMS).
* **Impact:** Uninformed personnel handling sensitive customer data or intellectual property, violating compliance mandates (e.g., GDPR, ISO 27001).
* **Existing Control:** Manual HR spreadsheet audits and periodic compliance reminders.
* **Treatment:** Implement automated identity provisioning blocks that restrict network and application access until LMS training completion certificates are verified via API sync.
* **Owner:** Director of Human Resources & IT Operations

---

## 3. Medium-Severity Risks

### 4. Low Phish-Alarm Button (PAB) Adoption Velocity
* **Risk:** Employees identifying suspicious emails but failing to report them promptly to the Security Operations Center (SOC).
* **Cause:** Friction in reporting workflows, lack of awareness regarding the importance of reporting, or fear of false-positive reprimands.
* **Impact:** Delayed incident detection window, allowing active phishing campaigns to persist longer across the organization.
* **Existing Control:** Availability of a generic email reporting mailbox.
* **Treatment:** Deploy a standardized one-click Phish-Alarm Button (PAB) in all client mailboxes accompanied by an enterprise-wide positive reinforcement campaign celebrating fast incident reporting.
* **Owner:** Security Operations Center (SOC) Manager

### 5. Inadequate Security Awareness for Third-Party Contractors
* **Risk:** External contractors and temporary agency staff operating without adequate security awareness education.
* **Cause:** Exclusion of third-party personnel from standard enterprise LMS onboarding workflows and compliance tracking.
* **Impact:** Introduction of insecure personal devices or unverified credentials into the corporate ecosystem, creating a backdoor for threat actors.
* **Existing Control:** Vendor contract clauses stipulating general security expectations without verification.
* **Treatment:** Integrate third-party contractor email domains into the enterprise LMS contractor portal, enforcing mandatory certificate upload prior to badge or network activation.
* **Owner:** Vendor Risk Management (VRM) Lead

### 6. Departmental Security Training Fatigue
* **Risk:** High-frequency training and continuous simulation schedules causing employee apathy and desensitization.
* **Cause:** Overlapping compliance modules, frequent ad-hoc testing, and lack of engaging, bite-sized delivery formats.
* **Impact:** Diminished training retention, increased error rates, and negative employee sentiment toward security initiatives.
* **Existing Control:** Annual compliance tracking reviews.
* **Treatment:** Transition to concise, gamified 3-to-5-minute micro-learning modules distributed monthly and streamline campaign frequency based on departmental risk scores.
* **Owner:** Security Awareness Training Manager

---

## 4. Low-Severity Risks

### 7. Outdated Physical Security Signage in Hybrid Offices
* **Risk:** Employees overlooking physical tailgating or "clean desk" policy infractions in hybrid work environments.
* **Cause:** Degradation of physical office reminder posters and infrequent reinforcement of physical security protocols during hybrid schedules.
* **Impact:** Minor physical security lapses, unauthorized visitor movement in regional facilities.
* **Existing Control:** Annual facility security walk-throughs and basic physical badge access controls.
* **Treatment:** Refresh digital signage across office intranet portals and corporate screensavers with modern "clean desk" and badge-piggybacking awareness graphics.
* **Owner:** Facilities & Physical Security Manager

### 8. Low Engagement with Optional Security Intranet Channels
* **Risk:** Minimal voluntary readership of security tips, newsletters, and advisory posts on corporate chat channels.
* **Cause:** Information overload on enterprise collaboration platforms and lack of interactive incentives.
* **Impact:** Reduced passive absorption of supplemental security advice among tech-savvy employees.
* **Existing Control:** Broadcast posts sent to general company chat channels.
* **Treatment:** Introduce interactive security quizzes with corporate rewards (e.g., peer recognition badges) to drive voluntary engagement with security awareness channels.
* **Owner:** Internal Communications & Security Awareness Lead

