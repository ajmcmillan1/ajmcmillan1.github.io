# DDoS Attack Sequence Diagram

```mermaid
sequenceDiagram
    participant Attacker
    participant BotNet
    participant WebServer
    participant Firewall
    participant LegitimateUser
    
    Attacker->>BotNet: The attacker tell BotNet to attack the target
    BotNet->>WebServer: Sends excessive overload traffic
    WebServer->>Firewall: Detects unusual traffic
    Firewall->>BotNet: Blocks IP addresses
    Firewall->>WebServer: Manages to Mitigates traffic
    WebServer->>LegitimateUser: Continues to serve legitimate requests

## Description of the Sequence Diagram

1. **Attacker Compromises Systems**: The attacker gains control over multiple systems, creating a botnet.
2. **BotNet Sends Excessive Requests**: The compromised systems (bots) start sending a large number of requests to the target web server, overwhelming it with traffic.
3. **WebServer Detects Unusual Traffic**: The web server detects an unusual amount of traffic and alerts the firewall.
4. **Firewall Blocks IP Addresses**: The firewall analyzes the traffic, identifies the sources of the excessive requests, and blocks the IP addresses of the bots.
5. **Firewall Mitigates Traffic**: The firewall continues to monitor and mitigate incoming traffic to ensure that only legitimate requests reach the web server.
6. **WebServer Continues to Serve Legitimate Requests**: The web server, now protected by the firewall, continues to serve legitimate users without interruption.
