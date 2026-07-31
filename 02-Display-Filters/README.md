# Display Filters

## Overview

Display Filters help analyze captured packets by showing only the traffic relevant to an investigation. Unlike Capture Filters, they do **not** discard packets—they simply control what is displayed in Wireshark.

---

## Why Use Display Filters?

Without filters, a packet capture may contain thousands of packets from different protocols and devices, making analysis difficult.

Display Filters help you:

- Focus on specific protocols
- Investigate communication from a particular device
- Analyze traffic on specific ports
- Reduce unnecessary information during investigations

---

# Common Display Filters

## Filter by Protocol

| Filter | Description |
|---------|-------------|
| `dns` | Displays DNS packets only |
| `tcp` | Displays TCP packets only |
| `udp` | Displays UDP packets only |
| `http` | Displays HTTP packets only |
| `tls` | Displays TLS/HTTPS packets |
| `icmp` | Displays ICMP packets |
| `arp` | Displays ARP packets |

---

## Filter by IP Address

| Filter | Description |
|---------|-------------|
| `ip.addr == 192.168.1.10` | Shows all packets involving the IP address |
| `ip.src == 192.168.1.10` | Shows packets sent by the IP address |
| `ip.dst == 192.168.1.10` | Shows packets received by the IP address |

---

## Filter by Port

| Filter | Description |
|---------|-------------|
| `tcp.port == 80` | HTTP traffic |
| `tcp.port == 443` | HTTPS traffic |
| `tcp.port == 22` | SSH traffic |
| `udp.port == 53` | DNS traffic |

---

## Combining Filters

### AND

```text
tcp && ip.addr == 192.168.1.15
```

Displays only TCP packets involving the specified IP address.

---

### OR

```text
dns || http
```

Displays DNS or HTTP packets.

---

### NOT

```text
!arp
```

Hides ARP packets from the capture.




