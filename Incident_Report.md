# SOC Incident Investigation - NetSupport Manager RAT

## Overview

This project documents a packet analysis investigation conducted using Wireshark.

The investigation was performed in response to SIEM alerts indicating potential NetSupport Manager RAT activity from external IP address 45.131.214.85 over TCP port 443.

The objective was to identify the infected workstation, determine user attribution, and document evidence supporting the investigation.

## Tools Used

* Wireshark
* Active Directory
* DNS
* NBNS
* Kerberos
* SAMR

## Investigation Workflow

1. Reviewed protocol hierarchy
2. Identified key endpoints
3. Analyzed host conversations
4. Investigated DNS activity
5. Identified workstation hostname through NBNS
6. Identified user account through Kerberos authentication traffic
7. Identified full user information through SAMR analysis
8. Documented findings

## Key Findings

| Item                     | Value             |
| ------------------------ | ----------------- |
| Infected Host IP         | 10.2.28.88        |
| MAC Address              | 00:19:d1:b2:4d:ad |
| Hostname                 | DESKTOP-TEYQ2NR   |
| User Account             | brolf             |
| Full Name                | Becka Rolf        |
| Malicious Infrastructure | 45.131.214.85     |

## Skills Demonstrated

* Network Traffic Analysis
* Incident Response
* Threat Hunting
* Wireshark
* Active Directory Investigation
* DNS Analysis
* Kerberos Analysis
* Evidence-Based Investigation
