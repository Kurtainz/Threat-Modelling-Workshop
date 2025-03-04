 # Kill Chain Attack Description: Solaris Health 360 Attack Scenario 2: Attack against Machine Processes and the data lake
 
 ## Stages of the Attack
 
 ### Reconnaissance
 Attackers scan the system for exposed APIs, endpoints, or misconfigured services. 
 Attackers gather information about the data lake (e.g., storage locations, access controls).
 
 ### Weaponization
 Attackers craft malicious payloads targeting backend services (e.g., SQL injection, API abuse). 
 Attackers create malware to exploit vulnerabilities in the data lake (e.g., unauthorized access to S3 buckets).
 
 ### Delivery
 Attackers deliver malicious payloads via phishing emails, malicious API calls, or compromised third-party integrations. 
 Attackers exploit misconfigured S3 buckets or Lambda functions to deliver malware.
 
 ### Exploitation
 Attackers exploit vulnerabilities in backend services (e.g., unpatched software, weak authentication).
 Attackers exploit misconfigured data lake access controls to gain unauthorized access.
 
 ### Installation
 Attackers install malware or backdoors in backend services to maintain persistence.
 Attackers exfiltrate data from the data lake to external servers.

 ### Command and Control (C2)
 Attackers establish communication channels with compromised backend services or data lake resources.
 Attackers use encrypted channels to evade detection.
 
 ### Actions on Objectives
 Attackers exfiltrate sensitive patient data from the data lake. 
 Attackers disrupt backend services, causing downtime or data corruption.
 
 
 ```mermaid
graph TD
    A[Reconnaissance] --> B[Weaponization]
    B --> C[Delivery]
    C --> D[Exploitation]
    D --> E[Installation]
    E --> F[Command and Control (C2)]
    F --> G[Actions on Objectives]

    %% Reconnaissance
    A --> A1[Scan for exposed APIs, endpoints, or misconfigured services]
    A --> A2[Gather information about the data lake (e.g., storage locations, access controls)]

    %% Weaponization
    B --> B1[Create malicious payloads targeting backend services]
    B --> B2[Develop malware to exploit data lake vulnerabilities]

    %% Delivery
    C --> C1[Deliver payloads via phishing, malicious API calls, or compromised integrations]
    C --> C2[Exploit misconfigured S3 buckets or Lambda functions]

    %% Exploitation
    D --> D1[Exploit vulnerabilities in backend services (e.g., unpatched software, weak authentication)]
    D --> D2[Exploit misconfigured data lake access controls]

    %% Installation
    E --> E1[Install malware or backdoors in backend services]
    E --> E2[Exfiltrate data from the data lake]

    %% Command and Control (C2)
    F --> F1[Establish communication channels with compromised systems]
    F --> F2[Use encrypted channels to evade detection]

    %% Actions on Objectives
    G --> G1[Exfiltrate sensitive patient data from the data lake]
    G --> G2[Disrupt backend services, causing downtime or data corruption]