# Medicare Clinics — Information Security Risk Assessment
**Methodology:** NIST SP 800-30 Rev. 1  
**Regulatory Underpinning:** Nigeria Data Protection Regulation (NDPR 2023), ISO/IEC 27001:2022, HIPAA-equivalent Clinical Security

---

## Executive Summary
Following an Electronic Health Record (EHR) migration, Medicare Clinics engaged an independent GRC consultant to assess its operational security posture. This audit identified significant critical compliance exposures, including an ongoing, regulatory-notifiable data breach.

### Identified Threat Posture Summary
*   **Critical Risks:** 2
*   **High Risks:** 3
*   **Medium Risks:** 2
*   **Low Risks:** 1

---

## Material Audit Findings

### 1. Active NDPR Breach: Unauthorized Patient PHI Transmission
*   **Threat Event:** Patient HIV clinical records and diagnosis lists were transmitted via standard personal Gmail profiles by medical practitioners.
*   **Regulatory Exposure:** Immediate, notifiable breach under NDPR S.2.6 (Unsecured Transit of Sensitive Personal Data).
*   **Mitigation Strategy:** Implement strict organizational policies banning personal mail use. Deploy enterprise-level email encryption layers and outbound Data Loss Prevention (DLP) filters.

### 2. Lack of Third-Party Assurance
*   **Threat Event:** The designated Cloud EHR software vendor failed to provide valid ISO/IEC 27001 certifications or SOC 2 Type II audit attestations upon request.
*   **Regulatory Exposure:** Critical Governance vulnerability.
*   **Mitigation Strategy:** Establish vendor management questionnaires. Renegotiate cloud service agreements to mandate annual security audits.

### 3. Missing RBAC (Role-Based Access Control) Policy
*   **Threat Event:** Administrative and non-clinical employees maintained generic high-privileged access privileges to the core patient database.
*   **Mitigation Strategy:** Enforce Principle of Least Privilege. Restrict nurse and administrative accounts strictly to non-diagnostic panels. Ensure all access events generate unique log entries.

---

## Recommended Phased Mitigation Roadmap

| Phase | Remediation Objective | Target Compliance Alignment | Timeline |
| :--- | :--- | :--- | :--- |
| **Phase 1** | Stop unstructured clinical email transit; notify oversight agencies. | NDPR 2023 | 48 Hours |
| **Phase 2** | Enforce localized clinical role-based restrictions on EHR console. | Principle of Least Privilege | 14 Days |
| **Phase 3** | Formulate vendor compliance SLAs and draft Business Continuity plans. | ISO 27001 Annex A.5.21 | 30 Days |


## Interactive Demonstration
Use the sample risk scoring simulator to explore how likelihood and impact ratings affect a risk rating. All values are illustrative.

[Open the Risk Assessment Simulator →](../demos/risk-assessment-simulator.html)
