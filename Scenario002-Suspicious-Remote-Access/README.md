# SOC-002 — Suspicious Remote Access to HR-PC01

## Incident Overview
This scenario simulates suspicious remote access to the HR-PC01 Windows 11 endpoint. Network logon activity originating from the BLACKWOLF Kali Linux machine was detected and investigated using Wazuh and Windows Security Event Logs.
The investigation focused on determining the source of the connection, the affected user account, the type of logon, and whether the activity required escalation.

## Investigation Flow
1. Suspicious network logon activity detected on HR-PC01.
2. Wazuh alert reviewed to identify the affected endpoint and user.
3. Windows Event ID 4624 reviewed to analyse the successful network logon.
4. Logon Type 3 and NTLM authentication identified.
5. Source IP address 192.168.1.155 traced to the BLACKWOLF Kali Linux machine.
6. Earlier reconnaissance activity from BLACKWOLF was checked for additional context.
7. Available evidence assessed and the activity treated as suspicious.
8. Incident escalated for further validation and investigation.

## SOC Documentation
- Full Incident Report
- SOC Incident Ticket
- Investigation screenshots and supporting evidence

## Skills Demonstrated
- SIEM alert investigation
- Windows Security Event Log analysis
- Successful logon analysis
- Network Logon Type analysis
- NTLM authentication analysis
- Source IP investigation
- Alert triage and evidence correlation
- Incident documentation
- SOC escalation and response decision-making

## Tools Used
- Oracle VirtualBox
- Wazuh
- Windows 11
- Windows Security Event Logs
- Kali Linux
- Nmap

## Evidence Walkthrough
The evidence below follows the activity and investigation in chronological order.

1. **BLACKWOLF Attacker Identification** — Kali Linux system identified as the BLACKWOLF attacker machine.
2. **BLACKWOLF IP Address** — Network information showing the source IP address used during the simulation.
3. **Nmap Reconnaissance from BLACKWOLF** — Nmap activity performed against HR-PC01 before the remote access activity.
4. **Wazuh Remote Logon Alert** — Wazuh alert showing suspicious network logon activity on HR-PC01.
5. **Windows Event ID 4624 Investigation** — Successful logon event reviewed to identify the affected user, Logon Type 3, authentication method and source address.
6. **Source IP Correlation** — Source IP 192.168.1.155 correlated with the BLACKWOLF Kali Linux machine.
7. **Analyst Assessment and Escalation** — Available evidence assessed as suspicious and escalated for further validation.

### Evidence Files
#### 01 — BLACKWOLF Attacker Hostname and IP
- [Raw Evidence](01_BLACKWOLF_Attacker_Hostname_IP.png)
- [Annotated Evidence](01_BLACKWOLF_Attacker_Hostname_IP.jpg)
#### 02 — BLACKWOLF SMB Login Attempt to HR-PC01
- [Raw Evidence](02_BLACKWOLF_SMB_Login_Attempt_HR-PC01.png)
- [Annotated Evidence](02_BLACKWOLF_SMB_Login_Attempt_HR-PC01.jpg)
#### 03 — Wazuh Network Logon Source IP on HR-PC01
- [Raw Evidence](03_Wazuh_Network_Logon_Source_IP_HR-PC01.png)
- [Annotated Evidence](03_Wazuh_Network_Logon_Source_IP_HR-PC01.jpg)
#### 04 — Wazuh Successful Logon for Mel from BLACKWOLF
- [Raw Evidence](04_Wazuh_Successful_Logon_Mel_From_BLACKWOLF.png)
- [Annotated Evidence](04_Wazuh_Successful_Logon_Mel_From_BLACKWOLF.jpg)
#### 05 — Wazuh Successful Remote Logon Alert
- [Raw Evidence](05_Wazuh_Successful_Remote_Logon_Alert.png)
- [Annotated Evidence](05_Wazuh_Successful_Remote_Logon_Alert.jpg)
#### 06 — Wazuh Remote Logon Rule and MITRE Details
- [Raw Evidence](06_Wazuh_Remote_Logon_Rule_MITRE_Details.png)
- [Annotated Evidence](06_Wazuh_Remote_Logon_Rule_MITRE_Details.jpg)

## Incident Documentation
- [**SOC-002 Incident Ticket**](SOC-002_Suspicious-Remote-Access-Ticket.pdf) — Short SOC case record covering the alert, investigation, analyst assessment and escalation.
- [**SOC-002 Full Incident Report**](SOC-002_Suspicious%20Remote%20Access%20to%20HR-PC01-Report.pdf) — Detailed report covering the complete investigation and escalation decision.
