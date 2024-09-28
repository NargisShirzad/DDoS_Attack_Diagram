```mermaid
sequenceDiagram
    participant Attacker
    participant BotNet
    participant WebServer
    participant Firewall

    Attacker->>BotNet: Command to start attack
    BotNet->>WebServer: Flood with requests
    WebServer->>Firewall: Detects high traffic
    Firewall-->>WebServer: Alert (potential DDoS attack)
    Firewall->>WebServer: Rate limiting activated
    Firewall->>BotNet: IP blocking initiated
    WebServer->>LegitimateUser: Denied service
    Firewall-->>LegitimateUser: Traffic analysis response
