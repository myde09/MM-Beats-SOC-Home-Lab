# SOC-001 — Social Engineering Attack
## Incident Overview

This scenario simulates a social engineering attack against the HR-PC01 Windows 11 endpoint. A fake HR update file was hosted on the BLACKWOLF Kali Linux machine and downloaded to HR-PC01.
The activity was monitored and investigated using Wazuh and Sysmon. Relevant alerts and process activity were reviewed to understand what occurred and determine the appropriate response.

## Investigation Flow
1. Fake HR update file hosted on BLACKWOLF.
2. HTTP server started on the attacker machine.
3. HR-PC01 connected to the BLACKWOLF server.
4. Fake HR update file downloaded to HR-PC01.
5. Process activity investigated using Wazuh and Sysmon telemetry.
6. Wazuh alert details and MITRE ATT&CK information reviewed.
7. Suspicious file moved to quarantine.
   
## SOC Documentation
- Full Incident Report
- SOC Incident Ticket
- Investigation screenshots and supporting evidence

## Skills Demonstrated
- SIEM alert investigation
- Windows endpoint monitoring
- Sysmon log analysis
- Process-chain analysis
- Threat identification
- Incident documentation
- Containment
- SOC escalation and response decision-making

## Tools Used
- Oracle VirtualBox
- Wazuh
- Sysmon
- Windows 11
- Kali Linux
- Ubuntu
- Windows Security Event Logs

## Evidence Walkthrough
The evidence below follows the attack and investigation in chronological order.

1. **HR Update Hosted on BLACKWOLF** — Fake HR update file prepared and hosted on the Kali Linux attacker machine.
2. **BLACKWOLF HTTP Server Started** — HTTP server started to make the file available to the victim endpoint.
3. **HR-PC01 Accessing BLACKWOLF** Server — HR-PC01 connected to the attacker-controlled HTTP server.
4. **HR Update Downloaded on HR-PC01** — The fake HR update file was successfully downloaded to the Windows endpoint.
5. **Wazuh Process Chain Investigation** — Process activity associated with the HR update was reviewed in Wazuh/Sysmon. Raw and annotated evidence are included.
6. **Wazuh Alert and MITRE ATT&CK Review** — Wazuh alert details, rule information and MITRE ATT&CK mapping were reviewed. Raw and annotated evidence are included.
7. **Suspicious File Quarantined** — The suspicious HR update file was moved to quarantine as the containment action.

### Incident Documentation

- [**SOC-001 Incident Ticket**](SOC-001_Incident-Ticket_HR-Update.pdf) - Short case record covering the alert, investigation, assessment and response.
- [**SOC-001 Full Incident Report**](SOC-001_Full-Incident-Report_HR-Update.pdf) — Detailed report covering the complete incident investigation and response.
>Where two versions of an evidence screenshot are provided, one is the original raw evidence and the other is annotated to highlight the security-relevant information used during the investigation.
