# Regulatory Mapping: EU AI Act and Related Frameworks

This document maps the Governed Digital Worker reference architecture 
to the EU AI Act and the regulatory frameworks applicable to financial 
services organisations in the UK and EU. It is a companion to the 
Digital Job Description template and Five Gates checklist.

---

## EU AI Act: Article-level mapping

| Article | Requirement | Architecture component | Evidence |
|---------|-------------|----------------------|----------|
| Article 9 | Risk management system | Five Gates clearance sequence | Completed Five Gates checklist |
| Article 10 | Data governance | DJD data access section | Approved DJD, data access log |
| Article 11 | Technical documentation | Digital Job Description | Signed, version-controlled DJD |
| Article 12 | Record-keeping and logging | Attribution Ledger | HMAC-chained audit log |
| Article 13 | Transparency and information provision | DJD scope of authority | Published DJD, worker naming convention |
| Article 14 | Human oversight | Shadow Mode / Escalation triggers | Shadow Mode log, escalation records |
| Article 17 | Quality management system | DJD change management / review cycle | Version history, re-approval records |
| Article 26 | Obligations of deployers | Named business owner in DJD | DJD Section 5, SMCR mapping |
| Article 72 | Post-market monitoring | Attribution Ledger / success metrics | Ledger records, metrics dashboard |

---

## Risk classification

Digital Workers deployed in financial services are likely to fall 
within EU AI Act Annex III high-risk categories. Classification must 
be confirmed per worker before Gate 5 clearance.

| Annex III category | Applicable to Digital Workers in financial services |
|-------------------|--------------------------------------------------|
| 5(b) — AI in employment, worker management | Applicable where Digital Workers are assessed, monitored, or managed through AI systems |
| 4(a) — AI used in education and vocational training | Not typically applicable |
| 6(b) — AI in access to essential services | Applicable where Digital Workers influence credit, insurance, or eligibility decisions |
| 1(a) — Biometric categorisation | Not applicable |

**Classification obligation:** The deploying organisation must confirm 
the risk classification of each Digital Worker before deployment and 
document the assessment in the conformity assessment record (Gate 5).

---

## DORA: ICT risk management mapping

| DORA requirement | Architecture component | Evidence |
|-----------------|----------------------|----------|
| ICT risk identification | DJD scope and prohibited actions | Approved DJD |
| ICT risk protection | Policy Decision Point (OPA) | Policy bundle, deny-by-default log |
| ICT risk detection | Attribution Ledger monitoring | Ledger records, anomaly alerts |
| ICT risk response and recovery | Kill Switch procedure | Kill Switch test record |
| ICT risk testing | Shadow Mode / Kill Switch test | Gate 3 checklist |
| Third-party ICT risk | Worker identity isolation (SPIFFE/SVID) | SPIRE registration records |
| ICT incident reporting | Escalation trigger records | Attribution Ledger escalation log |

**DORA Article 11 — ICT Business Continuity:** The Kill Switch 
revocation procedure satisfies the requirement for documented recovery 
capabilities for critical ICT systems. Kill Switch must be tested 
before Gate 3 clearance.

---

## FCA Consumer Duty mapping

| Consumer Duty outcome | Architecture component | Evidence |
|----------------------|----------------------|----------|
| Products and services | DJD scope of authority | Approved DJD |
| Price and value | Success metrics | DJD Section 4, metrics records |
| Consumer understanding | Transparency of action | Attribution Ledger |
| Consumer support | Escalation triggers | Escalation log, human response records |

**Audit trail requirement:** The Attribution Ledger provides the 
tamper-evident, append-only record of every Digital Worker action 
required to demonstrate Consumer Duty compliance in the event of 
regulatory review.

---

## SMCR: Accountability mapping

Under the Senior Managers and Certification Regime, a named individual 
must be accountable for every system that can affect regulated 
activities. Digital Workers are no exception.

| SMCR requirement | Architecture component | Evidence |
|-----------------|----------------------|----------|
| Named Senior Manager accountability | DJD Section 5: Business Owner | Signed DJD |
| Reasonable steps defence | Five Gates clearance | Completed Five Gates checklist |
| Governance record | Attribution Ledger | Ledger records |
| Incident accountability | Kill Switch procedure, escalation log | Gate 3 records, escalation log |

**Accountability chain:** Every Attribution Ledger entry carries the 
Worker ID, which maps to a named Business Owner in the DJD. The chain 
from action to accountable individual is unbroken and auditable.

---

## NIST AI 600-1 mapping

| NIST AI 600-1 function | Architecture component | Notes |
|-----------------------|----------------------|-------|
| Govern (GV-1.1) | DJD governance structure | Organisational AI policies reflected in DJD |
| Govern (GV-1.2) | DJD review and approval cycle | Version control and re-approval requirements |
| Map (MP-2.3) | Risk classification | EU AI Act Annex III classification |
| Measure (MG-2.2) | Attribution Ledger | Observable metrics and audit trail |
| Manage (MG-3.2) | Escalation triggers | Human oversight for high-risk actions |
| Map (MP-5.1) | Shadow Mode | Pre-deployment safety evaluation for high-risk agentic systems |

---

## Regulatory framework versions

This mapping reflects the following regulatory versions. Confirm 
currency before use in a conformity assessment.

| Framework | Version / Status | Effective date |
|-----------|-----------------|----------------|
| EU AI Act | Regulation (EU) 2024/1689 | 2 August 2026 (high-risk provisions) |
| DORA | Regulation (EU) 2022/2554 | 17 January 2025 |
| FCA Consumer Duty | PS22/9 | 31 July 2023 |
| SMCR | FCA SM&CR regime | In force |
| NIST AI 600-1 | Initial public draft | July 2024 |

---

## Disclaimer

This mapping is provided for reference purposes. It does not constitute 
legal or regulatory advice. Organisations should confirm the 
applicability of each requirement to their specific deployment context 
with qualified legal and compliance counsel.

---

*Part of the Governed Digital Worker Reference Architecture.*  
*Published under CC BY 4.0. Attribution required.*  
*https://github.com/KaosKal/reclaimed-workforce*
