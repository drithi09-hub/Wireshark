# Advanced Display Filters


---

# IP Address Filters

| Filter | Purpose |
|---------|---------|
| `ip.src==<IP>` | Show packets sent from a specific IP address |
| `ip.dst==<IP>` | Show packets sent to a specific IP address |
| `ip.addr==<IP>` | Show packets where the IP appears as either source or destination |

---

# Port Filters

| Filter | Purpose |
|---------|---------|
| `tcp.port==443` | Show packets using port 443 |
| `tcp.srcport==443` | Show packets originating from port 443 |
| `tcp.dstport==443` | Show packets destined for port 443 |

---

# Logical Operators

| Operator | Purpose |
|----------|---------|
| `&&` | Both conditions must be true |
| `||` | Either condition can be true |
| `!` | Exclude matching packets |

Example:

```text
ip.addr==192.168.29.189 && tcp.port==443
```

Displays HTTPS traffic involving the specified IP address.

---

# Searching Packet Contents

```text
frame contains "google"
```

Searches for packets containing the specified text.

This is useful when analyzing unencrypted protocols such as HTTP.

---

# TCP Streams

A TCP Stream represents one complete TCP conversation between two endpoints.

Example:

```text
tcp.stream==12
```

Displays only packets belonging to Stream 12.

---

# TCP Flag Filters

| Filter | Purpose |
|---------|---------|
| `tcp.flags.syn==1 && tcp.flags.ack==0` | Show connection requests |
| `tcp.flags.syn==1 && tcp.flags.ack==1` | Show server responses during the handshake |
| `tcp.flags.reset==1` | Show connection reset packets |
| `tcp.flags.fin==1` | Show graceful connection termination |



