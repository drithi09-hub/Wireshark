# Wireshark Basics & Packet Capturing

## Key Concepts

### Wireshark

Wireshark is an open-source Network Protocol Analyzer that captures and analyzes network traffic in real time.

---

### Packet

- Layer 3 (Network Layer)
- Uses IP Addresses
- Travels between networks

---

### Frame

- Layer 2 (Data Link Layer)
- Uses MAC Addresses
- Delivers packets within the local network

---

### Network Interface

Wireshark captures traffic only from the selected network interface.

Examples:

- Wi-Fi
- Ethernet
- VPN
- Virtual Adapters

---

### Capture Filter

Applied **before** capturing packets.

Only matching packets are recorded.

---

### Display Filter

Applied **after** capturing packets.

Shows only matching packets while keeping the original capture intact.

---

## Basic Packet Flow

```text
DNS Request
      ↓
DNS Response
      ↓
TCP Three-Way Handshake
      ↓
HTTPS Request
      ↓
Webpage/Data Transfer
      ↓
TCP Connection Close
```

---

## Summary

- Packets use IP addresses.
- Frames use MAC addresses.
- Choose the correct network interface before capturing traffic.
- Capture Filters reduce captured traffic.
- Display Filters simplify packet analysis.
- DNS resolution happens before TCP communication.
- FIN closes a connection gracefully, while RST terminates it immediately.