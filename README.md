# Enterprise Identity Incident Investigation
![Microsoft Sentinel](https://img.shields.io/badge/Microsoft-Sentinel-0078D4?logo=microsoftazure&logoColor=white)
![Microsoft Entra ID](https://img.shields.io/badge/Microsoft-Entra%20ID-5C2D91?logo=microsoft&logoColor=white)
![Microsoft 365](https://img.shields.io/badge/Microsoft-365-D83B01?logo=microsoftoffice&logoColor=white)
![Kusto Query Language](https://img.shields.io/badge/KQL-Query%20Language-blue)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE-ATT%26CK-red)

This repository demonstrates how identity based security incidents can be detected, investigated, and remediated using Microsoft Sentinel, Microsoft Entra ID authentication logs, and the MITRE ATT&CK framework.

The project simulates the workflow used by Security Operations Center analysts when responding to identity security alerts in Microsoft cloud environments.

The scenarios documented in this repository include authentication attacks, credential compromise activity, suspicious login patterns, and potential data exfiltration behavior.

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

## Detection Rules

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

## Evidence Collection

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

## Investigation

The security investigation performed in this lab is based on the enterprise identity incident investigation project available in the repository below.

Project Repository  
https://github.com/jwnfld3/enterprise-identity-incident-investigation

This project simulates identity related security incidents within an enterprise environment and documents how security analysts investigate suspicious authentication activity across Microsoft identity systems.

The investigation process focuses on identifying abnormal login behavior, analyzing authentication logs, correlating security events, and determining whether the activity represents a potential account compromise or other malicious behavior.

### Investigation Environment

The simulated enterprise environment used for the investigation includes several common enterprise technologies used in identity management and security monitoring.

• Windows Server 2022  
• Active Directory Domain Services  
• Microsoft 365  
• Microsoft Entra ID  
• Microsoft Intune  
• Windows 11 client systems  
• Hyper V virtualization  

These technologies were used to simulate enterprise authentication activity and identity security monitoring scenarios. Enterprise environments commonly rely on centralized identity platforms and authentication services to manage user access and enforce security policies.

### Investigation Approach

The investigation followed a structured process similar to the workflow used by security operations center analysts.

1. Identify suspicious authentication activity.

   Investigation begins by reviewing authentication alerts or abnormal login behavior that may indicate a compromised account or unauthorized access attempt.

2. Review authentication logs.

   Security analysts analyze authentication events such as login failures, login successes, and multi factor authentication requests to determine whether abnormal patterns are present.

3. Correlate events across systems.

   Authentication events are compared with other security events to determine whether the activity is isolated or part of a broader attack pattern.

4. Identify indicators of compromise.

   Analysts look for indicators that suggest malicious activity, such as repeated authentication failures, abnormal login locations, or suspicious device access.

5. Document findings.

   All investigation results are documented in structured incident reports that describe the suspicious activity, the analysis performed, and the recommended remediation actions.

### Investigation Objective

The goal of the investigation is to simulate real world blue team analysis performed by security analysts when responding to identity related security incidents. By analyzing authentication logs and correlating security events, analysts can determine whether suspicious activity represents a legitimate security threat or normal system behavior.

This investigation helps demonstrate how security analysts detect potential identity compromise, analyze authentication patterns, and document incident response procedures within enterprise environments.

---

## MITRE ATT&CK Mapping

The incident scenarios investigated in this project were mapped to the MITRE ATT&CK framework to identify the adversary tactics and techniques associated with each activity. The MITRE ATT&CK framework is a widely used knowledge base that documents real-world attacker behavior based on observed threat actor techniques.

Mapping incidents to ATT&CK techniques helps security analysts understand how attackers operate during different phases of an intrusion. It also assists defenders in building detection strategies, improving monitoring, and strengthening defensive controls.

| Incident Scenario | Tactic | Tactic ID | Technique | Technique ID |
|------------------|--------|-----------|-----------|--------------|
| Identity Compromise Investigation | Credential Access | TA0006 | Valid Accounts | T1078 |
| MFA Fatigue Attack | Credential Access | TA0006 | Multi Factor Authentication Request Generation | T1621 |
| Conditional Access Policy Block | Defense Evasion | TA0005 | Valid Accounts | T1078 |
| Data Exfiltration Investigation | Exfiltration | TA0010 | Exfiltration Over Web Services | T1567 |
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

**Detection**  
Security monitoring tools such as Microsoft Sentinel identify suspicious authentication activity using detection queries and alerting rules.

**Evidence Collection**  
Authentication logs, sign in data, and other relevant evidence are collected to understand the scope of the activity.

**Investigation**  
Security analysts review the collected logs to determine whether the activity represents a legitimate event or a potential compromise.

**MITRE ATT&CK Mapping**  
Observed activity is mapped to known attacker tactics and techniques to better understand adversary behavior.

**Remediation**  
Security controls such as Conditional Access policies, account resets, or access restrictions are implemented to secure the environment. Each section of the repository maps to a stage of the SOC investigation process.

**Workflow Summary**  
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


## Documentation Sources

The investigation techniques and remediation procedures documented in this repository were developed through review of publicly available cybersecurity documentation and official Microsoft security guidance. These resources provide detailed information on monitoring authentication activity, analyzing security logs, creating detection queries, and implementing identity protection controls within Microsoft cloud environments.

### Microsoft Security Documentation

The following Microsoft documentation sources were referenced to understand how security analysts monitor authentication activity, investigate suspicious sign in behavior, and implement identity protection controls.

• Microsoft Sentinel Documentation  
https://learn.microsoft.com/en-us/azure/sentinel/

• Microsoft Entra ID Sign in Log Documentation  
https://learn.microsoft.com/en-us/entra/identity/monitoring-health/concept-sign-ins

• Kusto Query Language Documentation  
https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/

• Microsoft Entra Conditional Access Documentation  
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
