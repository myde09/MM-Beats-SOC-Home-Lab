# SOC-003 — Brute Force Attack

## Incident Overview
This scenario simulates a brute-force attack against the HR-PC01 Windows 11 endpoint. Multiple failed authentication attempts were generated from the BLACKWOLF Kali Linux attacker machine and monitored using Wazuh and Windows Security Event Logs. The authentication activity was investigated to identify the source of the attempts, the targeted account, and whether any login attempt was successful.

## Investigation Flow
1. Multiple authentication attempts were generated against HR-PC01 from BLACKWOLF.
2. Wazuh was monitored for authentication-related security events.
3. Failed Windows logon events were identified and reviewed.
4. The source of the authentication attempts and targeted user account were investigated.
5. Related authentication events were correlated to determine the pattern and frequency of the attempts.
6. Successful logon activity was checked to determine whether the brute-force attempts resulted in account access.
7. The activity was assessed and documented from a Level 1 SOC analyst perspective.

## SOC Documentation 
- SOC Incident Ticket
- Full Incident Report
- Investigation screenshots and supporting evidence

## Skills Demonstrated
- SIEM alert monitoring and investigation
- Windows authentication log analysis
- Failed logon event analysis
- Brute-force attack identification
- Source IP and user account investigation
- Event correlation and timeline analysis
- Successful vs failed authentication validation
- Alert triage and analyst decision-making
- Incident documentation and escalation assessment

## Tools Used
- Wazuh SIEM
- Ubuntu Linux — Wazuh Server
- Windows 11 — HR-PC01
- Windows Security Event Logs
- Kali Linux — BLACKWOLF (Attacker)
- Oracle VirtualBox — Virtual Machine

## Evidence Walkthrough
The evidence below follows the brute-force attack and investigation in chronological order.

1. **BLACKWOLF Pre-Attack Timestamp** — The attacker machine timestamp was captured before the brute-force activity to establish a clear starting point for the investigation timeline.
2. **Failed Login Activity Detected in Wazuh** — Wazuh detected repeated failed authentication activity on HR-PC01. The related alerts were reviewed to confirm the affected endpoint, targeted account and authentication failure pattern.
3. **Failed Login Events Correlated** — Multiple authentication failures were reviewed together to identify the repeated login pattern and determine that the activity was consistent with a brute-force attempt rather than an isolated failed login.
4. **Successful Logon Activity Checked** — Authentication events following the failed attempts were reviewed to determine whether any login was successful and whether the targeted account may have been accessed.
5. **Successful Login Detected After Failed Attempts** — Wazuh authentication events showed a successful logon following the repeated failed attempts. This increased the severity of the investigation and required further review to determine whether the successful authentication was related to the preceding brute-force activity.
6. **Analyst Assessment and Escalation** — The combination of repeated failed authentication attempts followed by a successful login was treated as suspicious and requiring escalation. The relevant authentication evidence, timeline and affected endpoint details were documented for further investigation.

## Incident Documentation
The investigation was documented using both a SOC incident ticket and a full incident report.
These documents record the alert details, investigation findings, analyst assessment, escalation decision and recommended response actions.
## Evidence Files
