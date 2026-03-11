# The Reclaimed Workforce: Digital Worker Reference Architecture

A governance framework for deploying AI Digital Workers in regulated 
financial services environments. Built for organisations operating under 
FCA, DORA, EU AI Act, and SMCR obligations.

---

## What this repository contains

This repository is the technical companion to The Reclaimed Workforce 
four-part series published on LinkedIn, with the Champion's Guide 
publishing on Medium.

It provides the reference architecture, governance templates, and 
regulatory mapping for deploying Digital Workers with cryptographic 
identity, policy enforcement, and a tamper-evident audit trail.

The series addresses a straightforward problem. Skilled people in 
financial services spend the majority of their working week on 
high-volume, process-intensive work that consumes their expertise 
without rewarding it. Digital Workers can handle that work. But an 
ungoverned AI agent operating inside a regulated firm is not a 
productivity tool. This framework makes the difference.

**The Reclaimed Workforce — LinkedIn series:**
- [Part 1: Hiring the Invisible Colleague](https://www.linkedin.com/pulse/reclaimed-workforce-part-1-hiring-invisible-colleague-kal-perwaz-1zqae/)
- [Part 2: The Identity Framework](https://www.linkedin.com/pulse/copy-reclaimed-workforce-cxos-guide-digital-workplace-kal-perwaz-buoie/)
- [Part 3: Governance and the Digital Job Description](https://www.linkedin.com/pulse/reclaimed-workforce-cxos-guide-digital-workplace-framework-kal-perwaz-evxhe/)
- [Part 4: The Investment Roadmap](https://www.linkedin.com/pulse/reclaimed-workforce-cxos-guide-digital-workplace-framework-kal-perwaz-qm2te/)

**Champion's Guide** — publishing on Medium. Link to follow.

---

## The core problem this solves

An AI agent without governance is a liability, not an asset.

No identity. No policy. No audit trail. No accountability.

This framework gives every Digital Worker:
- A unique, time-limited cryptographic identity (SPIFFE/SVID)
- A Policy Decision Point that enforces its Digital Job Description 
  before any action executes
- An append-only Attribution Ledger with cryptographic chain of custody
- A tested Kill Switch with a maximum 15-minute revocation window
- A named human accountability owner on every record

---

## Repository structure
```
reclaimed-workforce/
├── README.md                  # This file
├── LICENSE                    # CC BY 4.0
├── diagrams/                  # Architecture diagrams (SVG)
│   ├── vocabulary-bridge.svg
│   └── from-wish-to-mandate.svg
├── governance/                # Governance templates
│   ├── digital-job-description-template.md
│   └── five-gates-checklist.md
└── regulatory-mapping/        # Regulatory alignment tables
    └── eu-ai-act-mapping.md
```

---

## The Five Gates

No Digital Worker moves from Shadow Mode to Full Agency until all 
five gates are cleared. Each gate has a named owner and a defined 
evidence requirement.

| # | Gate | Owner | Evidence required |
|---|------|-------|-------------------|
| 1 | Identity Gate | Business Owner | SPIRE registration confirmed. SVID issued and validated. |
| 2 | Policy Gate | Risk & Compliance | Signed DJD approved. OPA bundle loaded and verified. |
| 3 | Shadow Gate | Technical Lead | Shadow Mode log reviewed. Kill Switch tested. |
| 4 | Audit Gate | GRC Analyst | Ledger records present. Chain integrity verified. |
| 5 | Conformity Gate | CISO / DPO | DPIA completed. Conformity assessment documented. |

A worker that clears four gates is not almost ready. It is not ready.

---

## Key components

**Digital Passport (SPIFFE/SVID)**  
A time-limited cryptographic identity for each worker. Not a shared 
service account. Standard TTL: 15 minutes. High-assurance: 5 minutes.

**Policy Bus / Policy Decision Point (OPA)**  
Every action checked against the approved Digital Job Description 
before execution. Deny-by-default posture.

**Attribution Ledger**  
HMAC-chained append-only audit log. Cryptographic chain of custody. 
Satisfies EU AI Act Article 12 logging requirements.

**Digital Job Description**  
The governance document that defines what the worker may do, expressed 
as a signed OPA policy bundle. Satisfies EU AI Act Article 14 human 
oversight requirements.

**Kill Switch**  
SPIRE registration entry deletion. Revokes the SVID within the TTL 
window. Must be tested before go-live. A Kill Switch that has never 
been tested is not a control.

---

## Regulatory alignment

This architecture is designed for compliance with:

- **EU AI Act** — Articles 12 (logging), 14 (human oversight), 
  17 (quality management)
- **DORA** — ICT risk management and incident response
- **FCA Consumer Duty** — Audit trail and accountability requirements
- **SMCR** — Named individual accountability for every worker
- **NIST AI 600-1** — Shadow Mode satisfies pre-deployment safety 
  evaluation requirements for high-risk agentic systems

Full regulatory mapping table in `/regulatory-mapping/`.

---

## Status

| Component | Status |
|-----------|--------|
| Reference architecture diagrams | Available |
| Digital Job Description template | Available |
| Five Gates checklist | Available |
| EU AI Act mapping table | Available |
| Implementation examples | Planned |

---

## Author

**Kal Perwaz** — AI Security Architect and GRC Specialist  
30 years in infrastructure and governance. Financial services.  
[LinkedIn](https://www.linkedin.com/in/kal-perwaz/) · [GitHub](https://github.com/KaosKal)

---

## Licence

This architecture and documentation is published under the 
[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).  
You are free to use, adapt, and build on it. Attribution required.
