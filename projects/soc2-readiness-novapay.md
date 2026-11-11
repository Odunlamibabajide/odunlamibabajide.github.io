# SOC 2 Type I Readiness Assessment — NovaPay
**Methodology:** AICPA Trust Services Criteria (SOC 2), Security + Availability
**Format:** STAR (Situation, Task, Action, Result)

---

## Executive Summary
Enterprise customers increasingly require SOC 2 evidence before signing SaaS contracts. This project simulates the readiness step a GRC analyst performs before a company pursues formal certification — assessing a fictional B2B SaaS company ("NovaPay") against all 36 applicable Trust Services Criteria, identifying control gaps, and delivering a prioritized remediation roadmap.

## Situation
NovaPay is a fictional B2B payments-automation SaaS company (~45 employees) hosting customer financial data on AWS. Enterprise prospects were requiring SOC 2 evidence before signing, but the company had never undergone a formal readiness review.

## Task
Conduct a full SOC 2 Type I readiness assessment scoped to Security (Common Criteria CC1–CC9) and Availability (A1), identify where the control environment fell short of audit-ready evidence, and produce a prioritized remediation plan.

## Actions
* Mapped all 36 applicable criteria to the control NovaPay would be expected to have in place
* Scored each control as In Place, Partially In Place, or Not In Place, with a documented rationale
* Assigned a priority rating (High/Medium/Low) per gap based on audit criticality and business risk
* Sequenced remediation into a 30/60/90-day roadmap grouped by which deliverables closed the most gaps with the fewest dependencies

## Result

| Metric | Result |
|---|---|
| Criteria assessed | 36 (Security + Availability) |
| Fully in place | 7 of 36 (19%) |
| High-priority gaps | 16 |
| Projected readiness after 30-day items | ~45–50% |

The technical foundation was strong (MFA, encryption in transit, code review) but almost nothing was documented or tested. A single written Information Security Policy was identified as closing or improving 8 of the 36 criteria on its own.

## Frameworks & Standards
AICPA Trust Services Criteria (SOC 2), 2017 framework as revised in 2022 — Security and Availability categories

## Organizational Benefits
* Clear, prioritized roadmap replaces guesswork with a sequenced plan leadership can resource and track
* Identifies the highest-leverage remediation items first, reducing time and cost to audit-readiness
* Gives sales and leadership a defensible answer to enterprise prospects asking about SOC 2 status
* Reduces risk of audit failure by surfacing gaps before engaging an external auditor

---

**[View full STAR-format report (PDF) →](https://github.com/Odunlamibabajide/soc2-readiness-novapay/blob/main/deliverables/SOC2_Portfolio_Entry_STAR.pdf)**

**[View control matrix + repo on GitHub →](https://github.com/Odunlamibabajide/soc2-readiness-novapay)**
