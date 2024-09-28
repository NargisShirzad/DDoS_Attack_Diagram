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

Steps of the sequence diagram
1. Attacker Command: The attacker tells the BotNet to launch the DDoS attack.
2. BotNet Flooding: The bots bombard the WebServer with a massive wave of requests.
3. Firewall Detection: The WebServer notices the sudden spike in traffic.
4. Alert to WebServer: The Firewall warns the WebServer about a potential DDoS attack.
5. Rate Limiting: The Firewall kicks in, limiting the number of requests to the server.
6. IP Blocking: The Firewall starts blocking the IPs of the bots to stop the flood.
7. Service Denied: Legitimate users find themselves unable to access the server.
8. Traffic Analysis: The Firewall analyzes the traffic to better respond to future attacks.
