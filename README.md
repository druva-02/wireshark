🌐 Wireshark Network Protocol Analysis

<p align="center">
<img src="https://img.shields.io/badge/Tool-Wireshark-blue?logo=wireshark" />
<img src="https://img.shields.io/badge/Domain-Cybersecurity-red" />
<img src="https://img.shields.io/badge/Category-Network%20Analysis-green" />
<img src="https://img.shields.io/badge/Status-Completed-success" />
</p>

📌 Project Overview

This project focuses on network traffic monitoring and protocol analysis using Wireshark, an open-source network protocol analyzer.

The objective is to capture, inspect, and understand different network protocols involved in communication between devices.

The project covers packet capturing, protocol identification, display filtering, TCP communication, DNS resolution, and basic network security observations.

📑 Table of Contents
Project Objectives
Tools and Technologies
Protocols Analyzed
Network Architecture
Packet Analysis Workflow
TCP Three-Way Handshake
DHCP DORA Process
Wireshark Display Filters
Project Directory Structure
Installation and Usage
Security Observations
Learning Outcomes
References
🎯 Project Objectives
Understand network communication and packet transmission.
Capture live network traffic using Wireshark.
Identify commonly used network protocols.
Analyze packet headers and protocol information.
Understand TCP connection establishment.
Examine DNS queries and responses.
Apply Wireshark display filters.
Identify basic network security indicators.
🛠️ Tools and Technologies
Tool / Technology	Purpose
Wireshark	Packet capturing and analysis
TCP/IP	Network communication
DNS	Domain name resolution
DHCP	Dynamic IP assignment
HTTP/HTTPS	Web communication
ARP	IP-to-MAC resolution
ICMP	Network diagnostics
PCAPNG	Packet capture storage
Windows/Linux	Operating system
🔍 Protocols Analyzed
Protocol	Port	Description
ARP	N/A	Resolves IP addresses to MAC addresses
DNS	53	Resolves domain names
DHCP	67/68	Assigns IP configurations
HTTP	80	Transfers web content
HTTPS	443	Secure web communication
TCP	N/A	Reliable data transmission
UDP	N/A	Connectionless data transmission
ICMP	N/A	Network diagnostics
TLS	N/A	Encrypts network communication
Protocol Descriptions

1. ARP – Address Resolution Protocol

ARP identifies the MAC address associated with an IPv4 address in a local network.

2. DNS – Domain Name System

DNS translates domain names into IP addresses.

3. DHCP – Dynamic Host Configuration Protocol

DHCP automatically assigns IP addresses and other network configuration parameters.

4. TCP – Transmission Control Protocol

TCP provides reliable and ordered communication between devices.

5. UDP – User Datagram Protocol

UDP provides connectionless communication with low overhead.

6. HTTP – Hypertext Transfer Protocol

HTTP enables communication between web browsers and web servers.

7. HTTPS – Hypertext Transfer Protocol Secure

HTTPS protects web communication using TLS encryption.

8. ICMP – Internet Control Message Protocol

ICMP supports network diagnostics and error reporting.

9. TLS – Transport Layer Security

TLS provides encryption and authentication for network communication.

🏗️ Network Architecture

The following diagram illustrates a basic network traffic monitoring environment.

mermaid
flowchart TD
    A[Client Device] --> B[Wi-Fi / Ethernet]
    B --> C[Router]
    C --> D[Internet]
    D --> E[Destination Server]

    B --> F[Wireshark]
    F --> G[Packet Capture]
    G --> H[Protocol Identification]
    H --> I[Traffic Analysis]
    I --> J[Security Observations]

🔄 Packet Analysis Workflow
mermaid
flowchart TD
    A([Start]) --> B[Open Wireshark]
    B --> C[Select Network Interface]
    C --> D[Start Packet Capture]
    D --> E[Generate Network Traffic]
    E --> F[Capture Packets]
    F --> G[Apply Display Filters]
    G --> H[Inspect Packet Details]
    H --> I[Identify Protocols]
    I --> J[Analyze Results]
    J --> K[Export Capture File]
    K --> L([End])

🤝 TCP Three-Way Handshake

TCP establishes a connection using three steps.

mermaid
sequenceDiagram
    participant Client
    participant Server

    Client->>Server: SYN
    Server-->>Client: SYN-ACK
    Client->>Server: ACK

    Note over Client,Server: TCP Connection Established

Explanation
SYN: Client requests a connection.
SYN-ACK: Server acknowledges the request.
ACK: Client confirms the connection.
📡 DHCP DORA Process

DHCP uses four steps to assign network configuration.

mermaid
sequenceDiagram
    participant Client
    participant DHCP_Server

    Client->>DHCP_Server: DHCP Discover
    DHCP_Server-->>Client: DHCP Offer
    Client->>DHCP_Server: DHCP Request
    DHCP_Server-->>Client: DHCP Acknowledge

    Note over Client,DHCP_Server: IP Configuration Assigned

🔎 Wireshark Display Filters
Protocol / Purpose	Display Filter
ARP	arp
DNS	dns
DHCP	dhcp
TCP	tcp
UDP	udp
HTTP	http
TLS	tls
ICMP	icmp
Specific IP	ip.addr == 192.168.1.1
Source IP	ip.src == 192.168.1.1
Destination IP	ip.dst == 192.168.1.1
TCP Port 443	tcp.port == 443
DNS Queries	dns.flags.response == 0
TCP SYN	tcp.flags.syn == 1
📁 Project Directory Structure
text
Wireshark-Network-Analysis/
│
├── README.md
│
├── docs/
│   ├── protocol_analysis.md
│   └── security_observations.md
│
├── reports/
│   └── Wireshark_Protocol_Analysis_Report.pdf
│
├── captures/
│   └── sample_capture.pcapng
│
├── screenshots/
│   ├── wireshark_dashboard.png
│   ├── arp_analysis.png
│   ├── dns_analysis.png
│   ├── tcp_analysis.png
│   └── protocol_hierarchy.png
│
├── diagrams/
│   ├── network_architecture.md
│   ├── packet_capture_flow.md
│   └── tcp_handshake.md
│
└── filters/
    └── wireshark_filters.txt

⚙️ Installation and Usage
Step 1: Install Wireshark

Download Wireshark from:

https://www.wireshark.org/download.html

Step 2: Open Wireshark

Launch Wireshark and select the active network interface.

Step 3: Start Packet Capture

Click the Start Capture button.

Step 4: Generate Network Traffic

Use a browser or network diagnostic commands to generate traffic.

Step 5: Apply Display Filters

Examples:

bash
arp
dns
tcp
udp
http
tls
icmp

Step 6: Analyze Packets

Inspect:

Source IP address
Destination IP address
Source and destination ports
Protocol type
Packet length
Packet details
Step 7: Export Capture

Save the capture in PCAPNG format for future analysis.

🛡️ Security Observations

Wireshark can help identify potentially suspicious network behavior.

Observation	Possible Concern
Unencrypted HTTP	Sensitive data exposure
Unusual DNS requests	Suspicious domain communication
Repeated TCP attempts	Connectivity issues or scanning
Unexpected ARP responses	Possible ARP spoofing
High retransmissions	Network performance problems
Unknown destinations	Requires further investigation

These indicators require additional analysis before concluding that an attack has occurred.

📊 Learning Outcomes

After completing this project, the following concepts can be understood:

Network packet capturing.
OSI and TCP/IP communication.
Protocol identification.
TCP three-way handshake.
DNS query and response.
DHCP address assignment.
Wireshark display filtering.
Basic network security monitoring.
📚 References
Wireshark Official Website
Wireshark Documentation
RFC Editor
TCP Specification – RFC 9293
DNS Specification – RFC 1035
TLS Specification – RFC 8446
⚠️ Disclaimer

This project is intended strictly for educational purposes and authorized network analysis.

Only capture and analyze network traffic on systems and networks where you have permission.

👨‍💻 Project Information

Project Name: Wireshark Network Protocol Analysis

Domain: Networking and Cybersecurity

Primary Tool: Wireshark

Project Category: Practical Network Analysis

⭐ If you find this project useful, consider giving the repository a star!
