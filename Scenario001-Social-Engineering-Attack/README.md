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
