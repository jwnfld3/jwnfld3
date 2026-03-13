# James Winfield

Security Operations | Identity Security | Microsoft Cloud Security

Hands-on cybersecurity portfolio focused on identity-based threat detection, Microsoft Sentinel investigations, and incident response playbooks within Microsoft cloud environments.

---

## Security Specializations

Identity Security Investigation  
Authentication Threat Detection  
Microsoft Sentinel Log Analysis  
MITRE ATT&CK Mapping  
Incident Response Documentation  
Microsoft Entra ID Security Monitoring  

---

## Core Security Technologies

| Category | Technologies |
|:---------|:-------------|
| Identity Security | Microsoft Entra ID, Identity and Access Management |
| Security Monitoring | Microsoft Sentinel, Microsoft Defender |
| Cloud Security | Microsoft 365 Security |
| Log Analysis | Kusto Query Language (KQL) |
| Infrastructure | Active Directory, Windows Server |

---

# Featured Security Investigation Project

## Enterprise Identity Security Incident Investigation

This project demonstrates structured SOC-style investigations of identity-based attacks including password spraying, MFA fatigue attacks, phishing authentication attempts, and impossible travel login activity.

The repository contains investigation case files, detection engineering examples, and incident response playbooks designed to simulate real-world identity security incidents within Microsoft cloud environments.

Key capabilities demonstrated:

• Authentication log analysis  
• Detection engineering using KQL  
• MITRE ATT&CK technique mapping  
• Incident response playbooks  
• Security investigation documentation  

Project Repository  
https://github.com/jwnfld3/enterprise-identity-incident-investigation

---

## Security Investigation Dashboard

View the investigation case tracker documenting simulated identity-based security incidents.

Investigation Dashboard  
https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/README.md

Example investigations include:

• Password Spray Attack Investigation  
• Identity Compromise Investigation  
• MFA Fatigue Attack Investigation  
• Impossible Travel Authentication Investigation  
• Phishing Authentication Attempt Investigation  
• Authentication Token Theft Investigation  
• Data Exfiltration Activity Investigation  

Each case documents investigation workflow, evidence collection, MITRE ATT&CK mapping, and remediation actions.

---

## Incident Response Playbooks

The following playbooks document investigation and remediation procedures for identity-based security incidents simulated within this lab environment.

These procedures were developed while studying Microsoft security documentation, the MITRE ATT&CK framework, and Microsoft Sentinel investigation workflows. Each playbook represents the structured response process used during the simulated investigations documented in this repository.

| Playbook | Description | MITRE ATT&CK Technique | Playbook |
|:---------|:-------------|:----------------------|:---------|
| Conditional Access Policy Block Remediation | Procedures for blocking suspicious authentication activity using Conditional Access policies | Defense Evasion / Initial Access | [View Playbook](https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/conditional-access-policy-block-remediation.md) |
| Data Exfiltration Investigation Remediation | Investigation and remediation procedures for suspected data exfiltration activity | T1041 Exfiltration Over Command and Control Channel | [View Playbook](https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/data-exfiltration-investigation-remediation.md) |
| Identity Compromise Remediation | Response procedures for compromised user identities and unauthorized access | T1078 Valid Accounts | [View Playbook](https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/identity-compromise-remediation.md) |
| Impossible Travel Login Remediation | Investigation procedures for logins originating from geographically distant locations within a short timeframe | T1078 Valid Accounts | [View Playbook](https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/impossible-travel-login-remediation.md) |
| MFA Fatigue Attack Remediation | Investigation and mitigation procedures for repeated MFA authentication prompts | T1621 Multi-Factor Authentication Request Generation | [View Playbook](https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/mfa-fatigue-attack-incident-remediation.md) |
| Password Spray Attack Remediation | Investigation and containment procedures for password spray authentication attempts | T1110.003 Password Spraying | [View Playbook](https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/password-spray-attack-remediation.md) |
| Phishing Attack Remediation | Investigation procedures for phishing-based authentication attempts targeting user credentials | T1566 Phishing | [View Playbook](https://github.com/jwnfld3/enterprise-identity-incident-investigation/blob/main/playbooks/phishing-attack-remediation.md) |

---

### Documentation Sources

The investigation techniques and remediation procedures documented in these playbooks were developed through review of publicly available cybersecurity documentation and vendor guidance.

Primary resources used include:

Microsoft Sentinel Documentation  
https://learn.microsoft.com/en-us/azure/sentinel/

Microsoft Entra ID Sign-in Log Documentation  
https://learn.microsoft.com/en-us/entra/identity/monitoring-health/concept-sign-ins

Kusto Query Language Documentation  
https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/

Microsoft Entra Conditional Access Documentation  
https://learn.microsoft.com/en-us/entra/identity/conditional-access/

MITRE ATT&CK Enterprise Matrix  
https://attack.mitre.org/matrices/enterprise/

These resources were used to understand how security analysts investigate authentication activity, analyze identity security alerts, and develop structured response procedures for identity-based threats.

---

## Current Focus

Building practical experience in:

Identity threat detection  
Security investigation workflows  
Microsoft Sentinel query development  
Incident response documentation  
Authentication log analysis  

---

## Portfolio Goal

This portfolio is designed to demonstrate hands-on experience investigating identity-based threats within Microsoft cloud environments and documenting structured incident response procedures aligned with industry frameworks such as MITRE ATT&CK.
