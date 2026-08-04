# Packet Analysis

## Overview

Packet analysis is the process of examining captured network packets to understand how devices communicate. Wireshark provides multiple analysis features that help investigate packet details, communication sessions, endpoints, and protocol distribution.

---

## Packet Analysis Workflow

```text
Captured Packet
        │
        ▼
Packet List
View packet summary
        │
        ▼
Packet Details
Inspect protocol fields
        │
        ▼
Packet Bytes
View raw hexadecimal data
        │
        ▼
Follow TCP Stream
Reconstruct communication
        │
        ▼
Conversations
Analyze communication between devices
        │
        ▼
Endpoints
Identify individual devices
        │
        ▼
Protocol Hierarchy
Summarize protocols in the capture
```

---

# Packet List

### Purpose

Displays a summary of every captured packet.

### Why It Is Needed

Provides a quick overview of network traffic, including source, destination, protocol, and packet information.

---

# Packet Details

### Purpose

Displays the decoded contents of the selected packet.

### Why It Is Needed

Allows analysts to examine fields such as IP addresses, TTL, ports, flags, and protocol-specific information.

---

# Packet Bytes

### Purpose

Displays the raw packet data in hexadecimal and ASCII format.

### Why It Is Needed

Helps verify the actual bytes transmitted across the network and supports advanced packet analysis.

---

# Follow TCP Stream

### Purpose

Reconstructs the complete communication between a client and a server.

### Why It Is Needed

Allows analysts to examine an entire TCP conversation instead of individual packets.

### Access

```text
Analyze
    ↓
Follow
    ↓
TCP Stream
```

---

# Conversations

### Purpose

Displays communication between pairs of devices.

### Why It Is Needed

Summarizes packet counts, bytes transferred, and ports used for each communication session.

### Access

```text
Statistics
    ↓
Conversations
```

---

# Endpoints

### Purpose

Lists every individual device involved in the capture.

### Why It Is Needed

Helps identify hosts that participated in network communication and their traffic statistics.

### Access

```text
Statistics
    ↓
Endpoints
```

---

# Protocol Hierarchy

### Purpose

Displays all protocols present in the capture in a hierarchical structure.

### Why It Is Needed

Provides a quick overview of protocol usage and helps identify the dominant traffic within a capture.

### Access

```text
Statistics
    ↓
Protocol Hierarchy
```


