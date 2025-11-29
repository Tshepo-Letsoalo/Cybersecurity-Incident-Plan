# 🛡️ Cybersecurity Incident Response Plan (SIRP)

This repository demonstrates my understanding of structured security incident handling, developed through the **IBM Cybersecurity Analyst** and **Google Cybersecurity** Professional Certificates.

---

## Scenario: Phishing and Account Compromise

A critical incident was reported: a senior employee fell victim to a **phishing email**, leading to the compromise of their primary corporate account credentials and potential data exfiltration.

## Incident Response: Six Phases

The following steps outline the systematic approach taken to mitigate the threat and restore operations, based on industry frameworks (e.g., NIST, SANS). 
### 1. Preparation
* **Goal:** Ensure resources and policies are ready *before* an incident.
* **Actions:** Defined clear roles (Incident Response Team, Communication Lead); maintained up-to-date documentation; ensured endpoint detection tools (EDR) were active on all critical assets.

### 2. Identification
* **Goal:** Determine if an incident occurred, its scope, and its root cause.
* **Actions:** Analyzed email logs and SIEM data (e.g., Splunk) for unauthorized login attempts or data access; isolated the compromised user's workstation and disabled the account immediately upon confirmation.

### 3. Containment
* **Goal:** Stop the spread of the attack and limit damage.
* **Actions:** **Short-Term:** Revoked all active sessions for the compromised user; enforced a network-wide password reset policy. **Long-Term:** Analyzed all logs for persistence mechanisms used by the attacker; blocked malicious IPs/domains at the firewall level.

### 4. Eradication
* **Goal:** Remove the threat completely.
* **Actions:** Scanned all affected systems for malware/backdoors; ensured the root cause (the phishing email) was removed from the mail server and all user inboxes; applied all necessary security patches.

### 5. Recovery
* **Goal:** Restore systems to normal operation and validate security.
* **Actions:** Monitored the restored system for 24 hours to ensure no recurrence; restored user account access with multi-factor authentication (MFA) enabled; notified relevant regulatory bodies (if required by compliance).

### 6. Lessons Learned (Post-Incident Activity)
* **Goal:** Improve security posture based on the incident.
* **Actions:** Documented the full timeline of the incident; updated the employee security awareness training with specific examples from this phishing attack; reviewed and updated the SIRP documentation.
