# Port Scan Investigation

## Incident Summary

A network host was observed sending TCP SYN packets to multiple ports on a target system within a short period of time.

The behavior is consistent with a TCP SYN Port Scan, commonly used during the reconnaissance phase of an attack to identify open services running on a target machine.

## Objective

Determine:

- Source of the scan
- Target host
- Ports being probed
- Nature of the activity
- Potential security impact

## Investigation Findings

### Source Host

10.100.25.14

### Target Host

10.100.18.12

### Activity Observed

The source host transmitted SYN packets to numerous ports on the destination host.

Examples include:

- 21 (FTP)
- 22 (SSH)
- 23 (Telnet)
- 25 (SMTP)
- 80 (HTTP)
- 135 (RPC)
- 139 (NetBIOS)
- 443 (HTTPS)
- 445 (SMB)
- 8080 (Web Service)

A total of 29 SYN packets were identified.

### Analysis

The traffic pattern indicates reconnaissance activity.

The attacker attempted to discover which services were available on the target system by sending TCP SYN packets to multiple ports.

No application-layer communication was observed.

The capture primarily contains scan activity rather than exploitation attempts.

## Evidence

Screenshots stored in the Screenshots folder.

## Conclusion

The observed traffic is consistent with a TCP SYN Port Scan.

The source system performed reconnaissance against the target host by probing multiple ports to identify available services.