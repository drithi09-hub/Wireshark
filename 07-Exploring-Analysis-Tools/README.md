# Exporting & Analysis Tools

## Overview

Wireshark provides several built-in tools that help analysts export evidence, locate specific packets, improve readability, and build investigation timelines.

---

# Export Objects

**Navigation**

```text
File
    ↓
Export Objects
```

**Purpose**

Recovers files transferred over supported protocols such as HTTP, SMB, FTP, and TFTP.

**Useful For**

- Recovering downloaded files
- Examining transferred documents or images
- Malware analysis

---

# Export Specified Packets

**Navigation**

```text
File
    ↓
Export Specified Packets
```

**Purpose**

Exports selected packets instead of the entire capture.

**Options**

- All Packets
- Displayed Packets
- Marked Packets

**Useful For**

- Creating smaller PCAPs
- Sharing investigation evidence
- Saving filtered traffic

---

# Name Resolution

**Navigation**

```text
View
    ↓
Name Resolution
```

**Purpose**

Displays hostnames instead of IP addresses whenever possible.

**Useful For**

- Easier packet analysis
- Quickly identifying systems
- Improving readability

---

# Coloring Rules

**Navigation**

```text
View
    ↓
Coloring Rules
```

**Purpose**

Applies colors to packets based on predefined or custom rules.

**Useful For**

- Differentiating protocols
- Identifying retransmissions and errors
- Faster packet analysis

---

# Find Packet

**Navigation**

```text
Edit
    ↓
Find Packet
```

**Purpose**

Searches for a specific packet using different search methods.

**Search By**

- Display Filter
- String
- Hex Value
- Packet Number

**Useful For**

- Quickly locating packets
- Navigating large captures

---

# Time Display Format

**Navigation**

```text
View
    ↓
Time Display Format
```

**Purpose**

Changes how packet timestamps are displayed.

**Useful For**

- Building investigation timelines
- Measuring communication duration
- Correlating network events

---

# SOC Investigation Workflow

```text
Receive PCAP
      │
      ▼
Export Evidence (if required)
      │
      ▼
Enable Name Resolution
      │
      ▼
Use Coloring Rules
      │
      ▼
Find Important Packets
      │
      ▼
Analyze Timeline
      │
      ▼
Collect Evidence
      │
      ▼
Final Report
```

