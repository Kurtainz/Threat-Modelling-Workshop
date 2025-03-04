```mermaid
sequenceDiagram
    participant Attacker
    participant System
    participant DataLake
    participant BackendServer
    participant User

    %% Reconnaissance
    activate Attacker
    Attacker->>System: Scan for exposed APIs, endpoints, or misconfigured services
    System-->>Attacker: Exposed APIs and endpoints identified
    Attacker->>DataLake: Gather information about data lake (e.g., storage locations, access controls)
    DataLake-->>Attacker: Data lake information gathered
    deactivate Attacker

    %% Weaponization
    activate Attacker
    Attacker->>System: Create malicious payloads targeting backend services
    System-->>Attacker: Payloads created
    Attacker->>DataLake: Develop malware to exploit data lake vulnerabilities
    DataLake-->>Attacker: Malware developed
    deactivate Attacker

    %% Delivery
    activate Attacker
    Attacker->>User: Deliver payloads via phishing, malicious API calls, or compromised integrations
    User-->>Attacker: Payloads delivered
    Attacker->>System: Exploit misconfigured S3 buckets or Lambda functions
    System-->>Attacker: Exploitation successful
    deactivate Attacker

    %% Exploitation
    activate Attacker
    Attacker->>BackendServer: Exploit vulnerabilities in backend services (e.g., unpatched software, weak authentication)
    BackendServer-->>Attacker: Backend compromised
    Attacker->>DataLake: Exploit misconfigured data lake access controls
    DataLake-->>Attacker: Data lake access gained
    deactivate Attacker

    %% Installation
    activate Attacker
    Attacker->>BackendServer: Install malware or backdoors in backend services
    BackendServer-->>Attacker: Malware installed
    Attacker->>DataLake: Exfiltrate data from the data lake
    DataLake-->>Attacker: Data exfiltrated
    deactivate Attacker

    %% Command and Control (C2)
    activate Attacker
    Attacker->>BackendServer: Establish communication channels with compromised systems
    BackendServer-->>Attacker: C2 channel established
    Attacker->>BackendServer: Use encrypted channels to evade detection
    BackendServer-->>Attacker: Encrypted communication active
    deactivate Attacker

    %% Actions on Objectives
    activate Attacker
    Attacker->>DataLake: Exfiltrate sensitive patient data from the data lake
    DataLake-->>Attacker: Data exfiltration complete
    Attacker->>BackendServer: Disrupt backend services, causing downtime or data corruption
    BackendServer-->>Attacker: Services disrupted
    deactivate Attacker