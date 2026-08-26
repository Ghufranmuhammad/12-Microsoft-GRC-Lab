# Internal Audit Interview Simulation: IT Security Manager

## Overview
This document outlines a simulated interview session between the **Lead Internal Auditor** and the **IT Security Manager** of the fictional UAE organization. The simulation illustrates how auditors gather facts, probe for compliance evidence, and uncover operational gaps during fieldwork walkthroughs.

---

## Interview Transcript

**Auditor:** Good morning. Thank you for taking the time to meet with me today as part of our annual information security internal audit. To start, could you walk me through how your team manages information security governance and policy updates?

**IT Security Manager:** Good morning. We maintain a centralized master information security policy framework. Every year, our team reviews the policies against changing operational requirements and ISO 27001 standards, and then we submit them to the CISO and executive board for formal sign-off.

**Auditor:** That aligns with our governance requirements. Can you provide the latest approved version of the Information Security Policy along with the digital board sign-off metadata?

**IT Security Manager:** Yes, absolutely. I will export the policy document and the executive sign-off audit trail from our GRC repository and email it to you by this afternoon.

---

**Auditor:** Moving on to access control, how often are privileged accounts and administrative rights reviewed?

**IT Security Manager:** Privileged access reviews are conducted on a strict quarterly schedule to ensure adherence to the principle of least privilege.

**Auditor:** Can you provide the review logs and evidence of sign-off for both Q1 and Q2 of 2026?

**IT Security Manager:** I can readily provide the Q1 access review logs—they were fully documented and signed off in January. However, regarding Q2... to be completely transparent, while the review walkthrough was performed, our team forgot to archive the final sign-off sheet before our cloud administrator went on leave.

**Auditor:** *[Noteing evidence gap]* Understood. We will note Q1 as verified and flag Q2 as a partial evidence gap pending retrospective sign-off. Now, regarding multi-factor authentication, is MFA enforced across all remote and administrative logins?

**IT Security Manager:** Yes, MFA is mandatory tenant-wide through Microsoft Entra ID conditional access policies. There are zero un-enforced accounts.

**Auditor:** Excellent. Can you provide the Entra ID conditional access policy export confirming that configuration?

**IT Security Manager:** Certainly. I have that export ready right here on my screen; I'll share the file with your working papers.

---

**Auditor:** Let's discuss vulnerability management. What is your scanning cadence for cloud infrastructure?

**IT Security Manager:** We run automated vulnerability scans of all cloud assets and web applications monthly using Microsoft Defender for Cloud and Tenable.

**Auditor:** Can you share the scan schedules and summary reports for the past six months?

**IT Security Manager:** Yes, our automated scheduler generates those reports on the first of every month. I'll pull the folder for you.

---

**Auditor:** How does your team handle third-party penetration testing?

**IT Security Manager:** We engage an independent third-party cybersecurity firm to conduct comprehensive penetration testing of our web applications and APIs annually.

**Auditor:** Can you provide the most recent third-party penetration test report?

**IT Security Manager:** The last test report on file is dated February 2025. 

**Auditor:** *[Reviewing timeline]* Today is August 2026, which means that report is 18 months old. Why hasn't an annual test been conducted in 2026?

**IT Security Manager:** To be candid, budget reallocation and competing cloud migration projects caused us to push the annual testing schedule out. We are currently in the process of booking a vendor for next quarter.

**Auditor:** *[Noting finding]* We will note that as a high-severity finding regarding lapsed annual penetration testing. 

---

**Auditor:** Turning to business continuity and disaster recovery, when was the last full-scale BCP/DR failover test performed?

**IT Security Manager:** Our last major DR failover simulation was executed in June 2025.

**Auditor:** That exceeds the 12-month annual testing requirement under our ISO 27001 scope. Can you provide any documentation for a 2026 test?

**IT Security Manager:** Unfortunately, we haven't performed a full-scale failover drill this year due to production stability freezes. 

**Auditor:** *[Noting finding]* That represents our second major testing gap. Let's discuss incident response. Does your incident response plan include a defined timeframe for notifying customers in the event of a data breach?

**IT Security Manager:** Our incident response plan outlines internal escalation trees and containment steps, but to be honest, it doesn't currently specify a strict 24 or 48-hour customer notification SLA.

**Auditor:** *[Noting finding]* We will raise a medium-severity finding for undefined breach notification SLAs. Finally, regarding supply chain security, how do you vet sub-processors used by your core vendors like GulfPay Services?

**IT Security Manager:** We review the primary vendor's SOC 2 or ISO certificates during onboarding, but we don't always independently track or request security reports for their downstream subcontractors.

**Auditor:** *[Concluding interview]* That creates a visibility gap in our fourth-party risk posture. Thank you for your transparency during this walkthrough; your openness helps us strengthen our overall control environment. We will compile these findings into our draft report.

