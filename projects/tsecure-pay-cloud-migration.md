# T-Secure Pay — Hybrid Cloud Migration GRC Assessment
**Client Scenario:** Payment infrastructure migrating to hybrid cloud.  
**Compliance Mandate:** ISO/IEC 27001:2022 Mapping to NDPR, Shared Responsibility Alignment.

---

## AWS Shared Responsibility Model Matrix
Determining clear operational liability boundaries is essential for board-level risk management.

| Asset Layer | Primary Owner | Compliance Obligation | Verification Audit Metric |
| :--- | :--- | :--- | :--- |
| **Physical Centers** | AWS | ISO 27001 A.7 (Physical Controls) | Third-Party SOC 2 Audit Report |
| **Hypervisor Security** | AWS | Host Hardening Requirements | AWS Attestation of Compliance (AOC) |
| **OS Patch Processes** | T-Secure Pay | System Configuration Mappings | Configuration Vulnerability Scans |
| **Database Encryption** | T-Secure Pay | NDPR S.2.6 (Data Isolation) | KMS Cryptographic Configuration Audit |
| **IAM Access Control** | T-Secure Pay | Principle of Least Privilege | IAM Policies Audit Logs |

---

## ISO 27001:2022 Control Mappings

### 1. ISO 27001 Annex A.8.24 (Use of Cryptography) ──► NDPR S.2.6
*   **Requirement:** Ensure secure transmission of cardholder information and preserve data residency boundaries.
*   **Remediation:** Enforce AES-256 for storage encryption and TLS 1.3 for transit. Utilize AWS KMS with local customer-managed keys to maintain data residency control.

### 2. ISO 27001 Annex A.8.3 (Access Restriction) ──► NDPR S.2.6
*   **Requirement:** Protect production database networks from lateral access or excessive administrative privileges.
*   **Remediation:** Implement distinct IAM roles. Deploy AWS CloudTrail to log API activity, and schedule access reviews within 30 days of onboarding.
