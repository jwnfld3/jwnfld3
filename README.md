# Enterprise Identity Incident Investigation Lab
![Microsoft Sentinel](https://img.shields.io/badge/Microsoft-Sentinel-0078D4?logo=microsoftazure&logoColor=white)
![Microsoft Entra ID](https://img.shields.io/badge/Microsoft-Entra%20ID-5C2D91?logo=microsoft&logoColor=white)
![Microsoft 365](https://img.shields.io/badge/Microsoft-365-D83B01?logo=microsoftoffice&logoColor=white)
![Kusto Query Language](https://img.shields.io/badge/KQL-Query%20Language-blue)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE-ATT%26CK-red)

This repository demonstrates how identity based security incidents can be detected, investigated, and remediated using Microsoft Sentinel, Microsoft Entra ID authentication logs, and the MITRE ATT&CK framework.

The project simulates the workflow used by Security Operations Center analysts when responding to identity security alerts in Microsoft cloud environments.

The scenarios documented in this repository include authentication attacks, credential compromise activity, suspicious login patterns, and potential data exfiltration behavior.

---
## Quick Navigation

The sections below provide a structured overview of the investigation workflow used in this lab. Each section contains documentation demonstrating how identity based security incidents were detected, investigated, and remediated.

| Section | Description | Link |
|--------|-------------|------|
| Detection Rules | KQL detection logic used to identify suspicious authentication activity in Microsoft Sentinel | https://github.com/jwnfld3/enterprise-identity-incident-investigation/tree/main/detections |
| Evidence Logs | Authentication logs, attack simulations, and supporting investigation evidence used during incident analysis | https://github.com/jwnfld3/enterprise-identity-incident-investigation/tree/main/evidence |
| Investigation Case Files | Detailed SOC style investigation reports documenting how each incident was analyzed | https://github.com/jwnfld3/enterprise-identity-incident-investigation/tree/main/case-files |
| Incident Response Playbooks | Step by step remediation procedures used to respond to identity based security incidents | https://github.com/jwnfld3/enterprise-identity-incident-investigation/tree/main/playbooks |
| Threat Intelligence | Detection query references and threat intelligence correlations used to support investigations | https://github.com/jwnfld3/enterprise-identity-incident-investigation/tree/main/threat-intelligence |

---

---

## Investigation Workflow

This lab follows a structured Security Operations Center investigation workflow used to analyze identity-based security alerts.

The investigation process includes the following stages:

| Stage | Description |
|------|-------------|
| Detection | Security monitoring identifies suspicious authentication activity using KQL detection queries. |
| Evidence Collection | Authentication logs and supporting evidence are collected for analysis. |
| Investigation | Analysts review logs and identify indicators of suspicious behavior. |
| MITRE ATT&CK Mapping | Observed activity is mapped to known adversary techniques. |
| Remediation | Incident response playbooks are used to contain and resolve the security event. |

---

This workflow demonstrates how identity security incidents are analyzed and documented within enterprise cloud environments.
## Investigation Scenarios

The following simulated security incidents were investigated as part of this lab environment.

| Case ID | Incident Type | Investigation File |
|-------|---------------|-------------------|
| CASE-001 | Password Spray Attack | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-001-password-spray.md |
| CASE-002 | Identity Compromise | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-002-identity-compromise.md |
| CASE-003 | MFA Fatigue Attack | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-003-mfa-fatigue.md |
| CASE-004 | Impossible Travel Login | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-004-impossible-travel.md |
| CASE-005 | Phishing Login Attempt | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-005-phishing-login.md |
| CASE-006 | Token Theft Activity | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-006-token-theft.md |
| CASE-007 | Data Exfiltration Investigation | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-007-data-exfiltration.md |

---

## Incident Response Playbooks

The following playbooks document the remediation procedures used to respond to the simulated identity security incidents.

| Playbook | Description | Link |
|---------|-------------|------|
| Conditional Access Policy Block Remediation | Procedures for reviewing and validating Conditional Access policy blocks | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/conditional-access-policy-block-remediation.md |
| Password Spray Attack Remediation | Response procedures for credential spraying attacks targeting multiple user accounts | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/password-spray-attack-remediation.md |
| Identity Compromise Remediation | Response procedures for suspected compromised user identities | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/identity-compromise-remediation.md |
| MFA Fatigue Attack Remediation | Investigation and mitigation procedures for repeated MFA prompt attacks | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/mfa-fatigue-attack-incident-remediation.md |
| Impossible Travel Login Remediation | Investigation procedures for geographically impossible login activity | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/impossible-travel-login-remediation.md |
| Phishing Attack Remediation | Investigation and containment procedures for phishing based authentication attempts | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/phishing-attack-remediation.md |
| Data Exfiltration Investigation Remediation | Investigation and response procedures for suspected data exfiltration activity | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/data-exfiltration-investigation-remediation.md |

---

## Tools and Technologies

This project demonstrates the use of several enterprise security tools and investigation techniques.

- Microsoft Sentinel  
- Microsoft Entra ID  
- Microsoft 365 Security Logs  
- Kusto Query Language (KQL)  
- Authentication Log Analysis  
- Incident Response Playbooks  
- MITRE ATT&CK Mapping

---

## Documentation Sources

Microsoft Sentinel Documentation  
https://learn.microsoft.com/en-us/azure/sentinel/

Microsoft Entra ID Sign-in Logs  
https://learn.microsoft.com/en-us/entra/identity/monitoring-health/concept-sign-ins

Kusto Query Language Documentation  
https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/

MITRE ATT&CK Framework  
https://attack.mitre.org/

---

# Detailed Investigation Documentation

The sections below contain the full investigation documentation, detection logic, and remediation procedures used throughout this lab environment.

These sections provide deeper technical detail for each investigation scenario, including detection queries, authentication log analysis, investigation case files, and incident response playbooks.

---

# Project Overview

Identity based attacks are one of the most common security threats facing organizations that rely on cloud identity platforms.

This project simulates how SOC analysts investigate identity related alerts by analyzing authentication logs, reviewing suspicious activity, and documenting response procedures.

The repository includes detection logic, investigation case files, supporting evidence artifacts, and structured remediation playbooks that demonstrate how security teams respond to identity based incidents.

---

# Investigation Workflow Diagram

The repository follows the investigation lifecycle used by Security Operations Center teams when responding to identity related security alerts.

```
             ┌───────────────┐
             │   Detection   │
             │  KQL Queries  │
             └───────┬───────┘
                     │
                     ▼
             ┌───────────────┐
             │    Evidence   │
             │ Authentication│
             │   Log Data    │
             └───────┬───────┘
                     │
                     ▼
             ┌───────────────┐
             │ Investigation │
             │   Case Files  │
             │  Indicators   │
             └───────┬───────┘
                     │
                     ▼
             ┌───────────────┐
             │   Remediation │
             │   Playbooks   │
             │  Mitigation   │
             └───────────────┘
```

Each section of the repository maps to a stage of the SOC investigation process.

detections → evidence → case-files → playbooks → threat-intelligence

---

# Technologies Used

This project demonstrates investigation techniques using the following technologies.

Microsoft Sentinel  
Microsoft Entra ID  
Microsoft 365 authentication logs  
Kusto Query Language (KQL)  
MITRE ATT&CK framework  

These tools are commonly used by SOC analysts to detect and investigate security incidents in Microsoft cloud environments.

---

# Investigation Methodology and Learning Process

The investigation procedures and response playbooks documented in this repository were developed through hands on practice in a controlled lab environment while studying Microsoft security documentation and the MITRE ATT&CK framework.

The goal of this project was to learn how Security Operations Center analysts investigate identity based alerts using Microsoft Sentinel and Microsoft Entra ID authentication logs.

---

# Detection Rules

The following detection queries simulate security monitoring rules used by Security Operations Center teams to identify suspicious authentication and identity related activity.

| Detection | Description | Link |
|-----------|-------------|------|
| Data Exfiltration Detection | Identifies abnormal file download activity from SharePoint and OneDrive | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/detections/data-exfiltration-detection.md |
| Impossible Travel Detection | Detects geographically impossible authentication attempts | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/detections/impossible-travel-detection.md |
| MFA Fatigue Detection | Detects repeated multi factor authentication prompts | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/detections/mfa-fatigue-detection.md |
| Password Spray Detection | Detects authentication attempts targeting multiple accounts | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/detections/password-spray-detection.md |
| Phishing Login Detection | Detects suspicious login behavior following phishing activity | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/detections/phishing-login-detection.md |
| Token Theft Detection | Detects abnormal authentication token activity | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/detections/token-theft-detection.md |

---

# Investigation Case Files

The following case files document simulated identity security incidents investigated using Microsoft Sentinel authentication logs and security telemetry.

| Case | Description | Link |
|------|-------------|------|
| CASE-001 Password Spray | Investigation of credential spraying attack targeting multiple user accounts | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-001-password-spray.md |
| CASE-002 Identity Compromise | Investigation of suspected compromised user account | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-002-identity-compromise.md |
| CASE-003 MFA Fatigue | Investigation of repeated multi factor authentication prompts | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-003-mfa-fatigue.md |
| CASE-004 Impossible Travel | Investigation of authentication attempts from geographically distant locations | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-004-impossible-travel.md |
| CASE-005 Phishing Login | Investigation of suspicious login activity related to phishing | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-005-phishing-login.md |
| CASE-006 Token Theft | Investigation of authentication token abuse | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-006-token-theft.md |
| CASE-007 Data Exfiltration | Investigation of suspicious file download activity | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/case-files/case-007-data-exfiltration.md |

---

# Incident Response Playbooks

The following playbooks document investigation and remediation procedures for identity based security incidents simulated within this lab environment.

| Playbook | Description | Link |
|----------|-------------|------|
| Conditional Access Policy Block Remediation | Procedures for reviewing and validating Conditional Access policy blocks | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/conditional-access-policy-block-remediation.md |
| Identity Compromise Remediation | Response procedures for compromised user identities | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/identity-compromise-remediation.md |
| Impossible Travel Login Remediation | Investigation procedures for suspicious geographic login activity | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/impossible-travel-login-remediation.md |
| MFA Fatigue Attack Remediation | Investigation procedures for repeated MFA prompts | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/mfa-fatigue-attack-incident-remediation.md |
| Password Spray Attack Remediation | Investigation procedures for credential spray attacks | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/password-spray-attack-remediation.md |
| Phishing Attack Remediation | Investigation procedures for phishing related credential compromise | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/phishing-attack-remediation.md |
| Data Exfiltration Investigation Remediation | Investigation procedures for suspicious file downloads | https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/data-exfiltration-investigation-remediation.md |

---

# Documentation Sources

The investigation techniques and remediation procedures documented in this repository were developed through review of publicly available cybersecurity documentation and vendor guidance.

## Microsoft Security Documentation

Microsoft Sentinel Documentation  
https://learn.microsoft.com/en-us/azure/sentinel/

Microsoft Entra ID Sign in Log Documentation  
https://learn.microsoft.com/en-us/entra/identity/monitoring-health/concept-sign-ins

Kusto Query Language Documentation  
https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/

Microsoft Entra Conditional Access Documentation  
https://learn.microsoft.com/en-us/entra/identity/conditional-access/

---

## MITRE ATT&CK Framework

MITRE ATT&CK Enterprise Matrix  
https://attack.mitre.org/matrices/enterprise/

These sources were used to understand how security analysts investigate authentication activity, analyze identity security alerts, and develop structured incident response procedures.

---

# Project Transparency

All investigations and remediation procedures documented in this repository were performed in a simulated lab environment for educational purposes.

The project demonstrates investigation methodology, authentication log analysis, and documentation practices commonly used within Security Operations Center environments.
