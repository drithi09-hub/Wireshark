# Network Protocols

## Overview

When a user enters a website such as `https://google.com`, multiple network protocols work together to successfully load the webpage. Each protocol performs a specific task before passing the communication to the next protocol.

---

## Protocol Flow

```text
User enters https://google.com
        │
        ▼
ARP
Find the router's MAC address
        │
        ▼
DNS
Resolve the domain name to an IP address
        │
        ▼
TCP
Establish a reliable connection
        │
        ▼
TLS
Create a secure encrypted channel
        │
        ▼
HTTP
Request the webpage
        │
        ▼
Server Response
Browser displays the webpage
```

---

# ARP (Address Resolution Protocol)

### Purpose

Resolves an IP address to its corresponding MAC address within the local network.

### Why It Is Needed

Before sending packets, the device must know the MAC address of the next hop (usually the default gateway).

### Common Wireshark Filter

```text
arp
```

---

# DNS (Domain Name System)

### Purpose

Converts a domain name into an IP address.

### Why It Is Needed

Computers communicate using IP addresses, not domain names.

### Common Wireshark Filter

```text
dns
```

---

# TCP (Transmission Control Protocol)

### Purpose

Establishes a reliable connection between the client and the server.

### Why It Is Needed

Ensures both devices are ready to communicate before data is exchanged.

### Three-Way Handshake

```text
SYN
   ↓
SYN-ACK
   ↓
ACK
```

### Common Wireshark Filter

```text
tcp
```

---

# TLS (Transport Layer Security)

### Purpose

Encrypts communication between the client and the server.

### Why It Is Needed

Protects sensitive information from being read during transmission.

### Common Wireshark Filter

```text
tls
```

---

# HTTP (HyperText Transfer Protocol)

### Purpose

Requests and transfers webpages between the client and the server.

### Why It Is Needed

Retrieves website content after a secure connection has been established.

### Common Wireshark Filter

```text
http
```

---

# UDP (User Datagram Protocol)

### Purpose

Provides fast communication without guaranteeing packet delivery.

### Common Uses

- DNS
- Video Streaming
- Online Gaming
- VoIP

### Common Wireshark Filter

```text
udp
```

---

# ICMP (Internet Control Message Protocol)

### Purpose

Provides network diagnostics and error reporting.

### Common Uses

- Ping
- Connectivity Testing
- Network Troubleshooting

### Common Wireshark Filter

```text
icmp
```

---

# Protocol Comparison

| Protocol | Primary Purpose |
|----------|-----------------|
| ARP | Find the MAC address of a local device |
| DNS | Resolve a domain name to an IP address |
| TCP | Establish a reliable connection |
| TLS | Encrypt communication |
| HTTP | Request webpages |
| UDP | Fast communication without guaranteed delivery |
| ICMP | Network diagnostics and error reporting |

