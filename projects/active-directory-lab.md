# Active Directory Lab & Vulnerability Assessment
**Operating Environment:** VM Virtualization Lab (VMware workstation)  
**Assessed Assets:** Windows Server 2022 Domain Controller, Windows 10 client, Kali Linux attacker workstation.

---

## Vulnerability Lab Configuration
The goal of this project was to construct an enterprise network environment to test security controls, analyze Active Directory vulnerability profiles, and review audit logs.

### Network Configuration Map
*   **Domain Controller (AD-DC-2022):** Formulates directories, manages security policies, and hosts directory roles.
*   **Workstation (WS-10-Secure):** Configured client system subject to centralized Group Policy Object (GPO) controls.
*   **Reconnaissance Host (Kali-Attack):** Isolated terminal used to run scans, check service configurations, and verify access boundaries.

---

## Assessment Findings

### 1. Active Directory Principal Enumeration (Kerbrute)
*   **Observation:** The testing tool confirmed three active system accounts using pre-authentication checks. This indicates susceptibility to targeted dictionary attacks.
*   **Remediation:** Enforce strong password complexity rules. Implement account lockout policies after three invalid login attempts.

### 2. Open Directory Querying (Anonymous LDAP Bind)
*   **Observation:** The LDAP server permitted unauthenticated queries, exposing basic naming context details and organizational attributes.
*   **Remediation:** Disable LDAP Anonymous Bind permissions within the Active Directory configuration.

### 3. Shared Directory Mapping (SMB Exposure)
*   **Observation:** System queries mapped and accessed public SMB shares without authentication, indicating vulnerability to lateral movement.
*   **Remediation:** Disable SMBv1 across the network. Enforce SMB signing requirements and restrict write access to authorized system accounts.
