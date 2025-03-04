 # Kill Chain Attack Description: Solaris Health 360 Attack Scenario 2: Attack against Machine Processes and the data lake
 
 ## Stages of the Attack
 
 ### Reconnaissance
 - Attackers scan the system for exposed APIs, endpoints, or misconfigured services. 
 - Attackers gather information about the data lake (e.g., storage locations, access controls).
 
 ### Weaponization
 - Attackers craft malicious payloads targeting backend services (e.g., SQL injection, API abuse). 
 - Attackers create malware to exploit vulnerabilities in the data lake (e.g., unauthorized access to S3 buckets).
 
 ### Delivery
 - Attackers deliver malicious payloads via phishing emails, malicious API calls, or compromised third-party integrations. 
 - Attackers exploit misconfigured S3 buckets or Lambda functions to deliver malware.
 
 ### Exploitation
 - Attackers exploit vulnerabilities in backend services (e.g., unpatched software, weak authentication).
 - Attackers exploit misconfigured data lake access controls to gain unauthorized access.
 
 ### Installation
 - Attackers install malware or backdoors in backend services to maintain persistence.
 - Attackers exfiltrate data from the data lake to external servers.

 ### Command and Control (C2)
 - Attackers establish communication channels with compromised backend services or data lake resources.
 - Attackers use encrypted channels to evade detection.
 
 ### Actions on Objectives
 - Attackers exfiltrate sensitive patient data from the data lake. 
 - Attackers disrupt backend services, causing downtime or data corruption.
 
 
```mermaid
graph TD
    A[<b>Reconnaissance</b>] --> A1[Scan for exposed APIs, endpoints, or misconfigured services]
    A1 --> B[<b>Weaponization</b>]
    B --> B1[Create malicious payloads targeting backend services]
    B1 --> C[<b>Delivery</b>]
    C --> C1[Deliver payloads via phishing, malicious API calls, or compromised integrations]
    C1 --> D[<b>Exploitation</b>]
    D --> D1[Exploit vulnerabilities in backend services<br>e.g., unpatched software, weak authentication]
    D1 --> E[<b>Installation</b>]
    E --> E1[Install malware or backdoors in backend services]
    E1 --> F[<b>Command and Control C2</b>]
    F --> F1[Establish communication channels with compromised systems]
    F1 --> G[<b>Actions on Objectives</b>]
    G --> G1[Exfiltrate sensitive patient data from the data lake]
    G1 --> G2[Disrupt backend services, causing downtime or data corruption]

    %% Additional actions
    A --> A2[Gather information about the data lake<br>e.g., storage locations, access controls]
    A2 --> B
    B --> B2[Develop malware to exploit data lake vulnerabilities]
    B2 --> C
    C --> C2[Exploit misconfigured S3 buckets or Lambda functions]
    C2 --> D
    D --> D2[Exploit misconfigured data lake access controls]
    D2 --> E
    E --> E2[Exfiltrate data from the data lake]
    E2 --> F
    F --> F2[Use encrypted channels to evade detection]
    F2 --> G