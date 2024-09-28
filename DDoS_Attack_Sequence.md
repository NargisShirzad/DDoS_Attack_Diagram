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

## Sequence Diagram Steps in Detail
1. **Attacker Command**: The attacker instructs the BotNet to initiate the DDoS attack.
2. **BotNet Flooding**: The bots unleash a flood of requests on the WebServer.
3. **Firewall Detection**: The WebServer detects the sudden surge in traffic.
4. **Alert to WebServer**: The Firewall alerts the WebServer about a potential DDoS attack.
5. **Rate Limiting**: The Firewall implements rate limiting to control incoming requests.
6. **IP Blocking**: The Firewall blocks the IP addresses of the bots to mitigate the attack.
7. **Service Denied**: Legitimate users are unable to access the WebServer.
8. **Traffic Analysis**: The Firewall conducts traffic analysis to enhance future defenses.
