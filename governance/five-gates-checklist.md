# Five Gates Checklist

The Five Gates are the mandatory clearance sequence for every Digital 
Worker before it moves from Shadow Mode to Full Agency. Each gate has 
a named owner, a defined evidence requirement, and a binary outcome: 
cleared or not cleared.

There is no partial clearance. A worker that clears four gates is not 
almost ready. It is not ready.

---

## How to use this checklist

Complete one checklist per Digital Worker per deployment transition. 
Retain the completed checklist as evidence for audit and conformity 
assessment purposes.

Gates must be cleared in sequence. Gate 2 cannot open until Gate 1 
is cleared. Gate 3 cannot open until Gate 2 is cleared.

---

## Worker details

| Field | Value |
|-------|-------|
| Worker ID | |
| Worker name | |
| DJD version | |
| Transition from | Shadow Mode |
| Transition to | Full Agency |
| Checklist completed by | |
| Date | |

---

## Gate 1: Identity Gate

**Owner:** Business Owner  
**Purpose:** Confirm the worker has a valid, unique cryptographic 
identity before any other gate is assessed.

| # | Evidence requirement | Status | Evidence reference | Date | Owner sign-off |
|---|---------------------|--------|-------------------|------|----------------|
| 1.1 | SPIRE registration entry created and active | | | | |
| 1.2 | SPIFFE/SVID issued and validated | | | | |
| 1.3 | SVID TTL configured correctly (standard: 15 min, high-assurance: 5 min) | | | | |
| 1.4 | Worker ID in SPIRE entry matches Worker ID in DJD exactly | | | | |
| 1.5 | No shared service account in use | | | | |

**Gate 1 outcome:** Cleared / Not cleared  
**Business Owner sign-off:** ________________  
**Date:** ________________

---

## Gate 2: Policy Gate

**Owner:** Risk & Compliance  
**Purpose:** Confirm the worker's Digital Job Description is approved 
and its OPA policy bundle is loaded and verified before it operates 
in any environment.

| # | Evidence requirement | Status | Evidence reference | Date | Owner sign-off |
|---|---------------------|--------|-------------------|------|----------------|
| 2.1 | DJD approved and signed by Business Owner | | | | |
| 2.2 | OPA policy bundle compiled from approved DJD | | | | |
| 2.3 | Policy bundle hash verified against DJD record | | | | |
| 2.4 | Policy bundle loaded to Policy Decision Point | | | | |
| 2.5 | Deny-by-default posture confirmed | | | | |
| 2.6 | Scope of Authority reviewed against regulatory obligations | | | | |
| 2.7 | Prohibited actions list reviewed and confirmed complete | | | | |

**Gate 2 outcome:** Cleared / Not cleared  
**Risk & Compliance sign-off:** ________________  
**Date:** ________________

---

## Gate 3: Shadow Gate

**Owner:** Technical Lead  
**Purpose:** Confirm the worker has operated correctly in Shadow Mode 
and that the Kill Switch functions within the required revocation window.

| # | Evidence requirement | Status | Evidence reference | Date | Owner sign-off |
|---|---------------------|--------|-------------------|------|----------------|
| 3.1 | Shadow Mode operation log reviewed | | | | |
| 3.2 | Minimum Shadow Mode period completed (define period in DJD) | | | | |
| 3.3 | Human approval rate during Shadow Mode reviewed | | | | |
| 3.4 | Escalation triggers fired correctly during Shadow Mode | | | | |
| 3.5 | Kill Switch tested in non-production environment | | | | |
| 3.6 | Kill Switch revocation confirmed within TTL window | | | | |
| 3.7 | Kill Switch test documented with date and tester name | | | | |
| 3.8 | Post-revocation SVID reissue procedure confirmed | | | | |

**Gate 3 outcome:** Cleared / Not cleared  
**Technical Lead sign-off:** ________________  
**Date:** ________________

---

## Gate 4: Audit Gate

**Owner:** GRC Analyst  
**Purpose:** Confirm the Attribution Ledger is recording correctly and 
that chain integrity can be verified independently.

| # | Evidence requirement | Status | Evidence reference | Date | Owner sign-off |
|---|---------------------|--------|-------------------|------|----------------|
| 4.1 | Attribution Ledger active and receiving records | | | | |
| 4.2 | All required fields present in every log entry | | | | |
| 4.3 | HMAC chain integrity verified | | | | |
| 4.4 | Ledger records tamper-evident (test attempted modification) | | | | |
| 4.5 | Retention period configured correctly | | | | |
| 4.6 | Ledger accessible to audit team independently of worker | | | | |
| 4.7 | Shadow Mode approval records present and complete | | | | |

**Gate 4 outcome:** Cleared / Not cleared  
**GRC Analyst sign-off:** ________________  
**Date:** ________________

---

## Gate 5: Conformity Gate

**Owner:** CISO / DPO  
**Purpose:** Confirm regulatory and data protection obligations are met 
before the worker operates autonomously.

| # | Evidence requirement | Status | Evidence reference | Date | Owner sign-off |
|---|---------------------|--------|-------------------|------|----------------|
| 5.1 | DPIA completed and approved | | | | |
| 5.2 | EU AI Act risk classification confirmed | | | | |
| 5.3 | Conformity assessment documented | | | | |
| 5.4 | SMCR accountability mapping confirmed (named individual in DJD) | | | | |
| 5.5 | DORA ICT risk assessment completed | | | | |
| 5.6 | FCA Consumer Duty impact assessed | | | | |
| 5.7 | Incident response procedure confirmed and tested | | | | |
| 5.8 | All previous gate sign-offs verified present | | | | |

**Gate 5 outcome:** Cleared / Not cleared  
**CISO / DPO sign-off:** ________________  
**Date:** ________________

---

## Final authorisation

All five gates must be cleared before this section is completed.

| Gate | Outcome | Owner | Date |
|------|---------|-------|------|
| Gate 1: Identity Gate | | Business Owner | |
| Gate 2: Policy Gate | | Risk & Compliance | |
| Gate 3: Shadow Gate | | Technical Lead | |
| Gate 4: Audit Gate | | GRC Analyst | |
| Gate 5: Conformity Gate | | CISO / DPO | |

**Authorisation to transition to Full Agency**

Authorised by: ________________  
Role: ________________  
Date: ________________  
Worker ID: ________________  
DJD version: ________________

---

## Re-clearance triggers

The following events require re-clearance of the affected gates before 
the worker continues in Full Agency:

| Event | Gates requiring re-clearance |
|-------|------------------------------|
| DJD change (any field) | Gates 2, 4, 5 |
| OPA policy bundle update | Gate 2 |
| SPIRE registration change | Gate 1 |
| Kill Switch activation | Gates 1, 3 |
| Attribution Ledger integrity failure | Gate 4 |
| Regulatory obligation change | Gate 5 |
| Security incident involving the worker | All gates |

---

*Part of the Governed Digital Worker Reference Architecture.*  
*Published under CC BY 4.0. Attribution required.*  
*https://github.com/KaosKal/reclaimed-workforce*
