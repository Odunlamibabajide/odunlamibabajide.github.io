# Bank Cloud Vendor Risk Assessment — Third-Party GRC Advisory
**Regulatory Focus:** Central Bank of Nigeria (CBN) Cybersecurity Framework, PCI DSS v4.0  
**Target Architecture:** Migration of Customer Information to Third-Party Cloud

---

## Risk Assessment Methodology
This audit analyzed operational risks across 8 domains, utilizing a standard 5x5 Likelihood-Impact matrix to determine pre-mitigation and residual exposure.

### Key Risk Profiles Cataloged

### R-01: Vendor-Side Security Compromise (Initial Level: Critical)
*   **Threat Event:** Attackers exploit configuration weaknesses within the vendor's cloud networks, gaining unauthorized access to the bank's active customer directories.
*   **Mitigation Actions:** Enforce Customer-Managed Encryption Keys (CMEK). Require annual SOC 2 Type II assessment reviews. Establish legally binding SLAs requiring breach notifications within 24 hours.
*   **Residual Level:** Medium

### R-02: Vendor Dependency Lock-In (Initial Level: Critical)
*   **Threat Event:** Service quality declines or contract prices increase unexpectedly, with no viable pathway to migrate assets back to local enterprise infrastructure.
*   **Mitigation Actions:** Mandate standard open data formats. Require formal testing of exit strategies twice per year. Ensure contracts include a 90-day termination clause.
*   **Residual Level:** Medium

### R-03: System Regulatory Gaps (Initial Level: High)
*   **Threat Event:** Hosting clinical or financial directories in regional locations that breach sovereign data residency requirements.
*   **Mitigation Actions:** Enforce storage localization within approved local geographies. Require NDPA validation audits.
*   **Residual Level:** Low

---

## 10-Step Vendor Security Management Plan
1.  **Contractual Requirements Check** (Before Onboarding)
2.  **Review SOC 2 Type II & Attestations** (Before Onboarding)
3.  **Define Encryption Control Keys** (Onboarding)
4.  **Confirm RBAC Account Access Policies** (Onboarding)
5.  **Review Network Path Hardening** (Quarterly)
6.  **Analyze Incident Response Preparedness** (Quarterly)
7.  **Run Scheduled Disaster Recovery Exercises** (Bi-Annually)
8.  **Evaluate Threat Log Activity** (Bi-Annually)
9.  **Conduct Complete Third-Party Assessments** (Annually)
10. **Formulate Regulatory Compliance Attestations** (Annually)


## Interactive Demonstration
Explore an illustrative 5×5 likelihood-impact risk scoring tool. It is a portfolio demonstration, not a substitute for an organization-approved risk methodology.

[Open the Risk Assessment Simulator →](../demos/risk-assessment-simulator.html)
