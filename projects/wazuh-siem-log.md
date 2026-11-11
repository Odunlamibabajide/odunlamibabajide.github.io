# Wazuh SIEM Deployment — Log Management & Compliance Monitoring
**Compliance Alignment:** ISO/IEC 27001:2022 Control A.12.4 (Event Logging), NDPR Audit Requirements

---

## System Architecture Design
A virtualized Wazuh SIEM manager was deployed within a virtual sandbox to aggregate security event logs from multiple endpoints.

```
  [Windows Client Agent]        [Linux Server Agent]
             │                            │
             └──────────────┬─────────────┘
                            ▼
                  [Wazuh SIEM Manager]
                            │
              (Log Decoders & Rules Engines)
                            │
                            ▼
             [Alert Dashboards & Reports]
```

---

## Implemented Monitoring Controls

### 1. Event Log Collection
*   Configured endpoints to forward OS-level events and access logs to the Wazuh SIEM manager. This centralized logging structure satisfies NDPR requirements for auditable data access histories.

### 2. Custom Rule Configuration
*   Created specific rule definitions to identify unauthorized administrative access attempts, such as multiple failed login attempts followed by a successful login.

### 3. File Integrity Monitoring (FIM)
*   Configured continuous file integrity monitoring on critical system directories, setting up real-time alerts for unauthorized modifications to configuration files.
