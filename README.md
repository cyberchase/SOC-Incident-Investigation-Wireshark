# SOC Incident Investigation – NetSupport Manager RAT

## Overview

This project documents a SOC Analyst-style packet analysis investigation conducted using Wireshark.

The investigation was initiated after SIEM alerts identified potential NetSupport Manager RAT activity communicating with external IP address 45.131.214.85 over TCP port 443.

The objective was to identify the infected host, determine user attribution, and document supporting evidence.

---

## Environment

| Item                    | Value                    |
| ----------------------- | ------------------------ |
| Domain                  | easyas123.tech           |
| Active Directory Domain | EASYAS123                |
| Domain Controller       | 10.2.28.2 (EASYAS123-DC) |
| Gateway                 | 10.2.28.1                |
| Network Range           | 10.2.28.0/24             |

---

## Investigation Workflow

1. Reviewed Protocol Hierarchy
2. Analyzed IPv4 Endpoints
3. Investigated Host Conversations
4. Examined DNS Activity
5. Identified Hostname using NBNS
6. Identified User Account using Kerberos
7. Identified Full User Information using SAMR
8. Correlated evidence to identify the infected host

---

## Findings

| Finding                  | Value             |
| ------------------------ | ----------------- |
| Infected IP Address      | 10.2.28.88        |
| MAC Address              | 00:19:d1:b2:4d:ad |
| Hostname                 | DESKTOP-TEYQ2NR   |
| User Account             | brolf             |
| Full User Name           | Becka Rolf        |
| Malicious Infrastructure | 45.131.214.85     |

---

## Tools Used

* Wireshark
* Active Directory
* DNS
* NBNS
* Kerberos
* SAMR
* Network Traffic Analysis

---

## Skills Demonstrated

* Incident Response
* Network Traffic Analysis
* Threat Hunting
* Host Attribution
* User Attribution
* Active Directory Investigation
* Evidence-Based Analysis

---

## Supporting Documentation

Detailed investigation report:

* Incident_Report.md

Evidence screenshots:

* Screenshots/Protocol_Hierarchy.png
* Screenshots/Endpoints.png
* Screenshots/Conversations.png
* Screenshots/MAC_Address_Verification.png
* Screenshots/Kerberos_Analysis.png
* Screenshots/User_Identification.png

---

## Conclusion

Analysis confirmed that workstation DESKTOP-TEYQ2NR (10.2.28.88) communicated with infrastructure associated with NetSupport Manager RAT activity.

Through packet analysis, host attribution, and user attribution techniques, the affected workstation and associated user account were successfully identified and documented.
