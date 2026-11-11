# Secure Network Design — Financial Services Branch
**Simulation Tool:** Cisco Packet Tracer  
**Core Strategy:** Zero-Trust Network Segmentation, Separation of Duties

---

## Network Architecture Requirements
This project simulated a corporate branch office requiring secure segmentation between departments, strict perimeter access rules, and secure administrative controls.

### Configured Segmentation
1.  **VLAN 10 (Administration):** Restricted network segment for operational personnel.
2.  **VLAN 20 (Customer Service):** Network segment for front-office terminals.
3.  **VLAN 30 (Information Technology):** High-privilege management subnet.

---

## Implemented Security Controls

### 1. Route-on-a-Stick Routing Segmentation
*   Configured distinct sub-interfaces on the central router to manage traffic between VLAN segments. This design enforces central checkpoints for all inter-department traffic.

### 2. Access Control Lists (ACLs)
*   Implemented strict Extended Access Control Lists (ACLs) to manage inter-segment communication. For example, direct communication between VLAN 20 (Customer Service) and VLAN 10 (Administration) is blocked, allowing only IT support to initiate administrative sessions.

### 3. Console Security & Management
*   Disabled legacy Telnet access across all network switches.
*   Enforced SSH for all administrative connections.
*   Configured login banner warnings to warn unauthorized users.
