# Control Failure Case Study & Lifecycle Workpaper

* **Control:** Privileged-Account Multi-Factor Authentication (CTL-07)
* **Requirement:** 100% of privileged administrator accounts must have multi-factor authentication enforced via Conditional Access policies.
* **Test:** Sampled 20 privileged administrator accounts from Microsoft Entra ID and verified their active authentication methods.
* **Evidence:** Entra ID user authentication method export and Conditional Access policy scope assignment report.
* **Result:** **Fail**
* **Finding:** 3 out of 20 sampled privileged accounts did not have MFA enforced due to an exclusion group misconfiguration during a recent administrative migration.
* **Risk:** High exposure to credential stuffing, account takeover, and unauthorized privilege escalation.
* **Severity:** High
* **Root Cause:** Administrative oversight during a recent tenant update where temporary emergency break-glass exclusion tags were left active on standard operational admin accounts.
* **Corrective Action:** Immediately revoke temporary exclusion groups, re-apply the mandatory MFA Conditional Access policy to the 3 non-compliant accounts, and verify active challenge prompts.
* **Retest Procedure:** Re-pull the Entra ID authentication method export for the affected accounts and test live sign-in challenges.
* **Closure Evidence:** Updated Conditional Access policy scope export and successful live test sign-in logs confirming active MFA enforcement across all 20 privileged accounts, dated August 22, 2026.

