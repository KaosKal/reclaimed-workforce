# Digital Job Description Template

A Digital Job Description (DJD) is the governance document that defines 
what a Digital Worker may do, under what conditions, and who is 
accountable for its actions. It is not a configuration file. It is an 
employment contract for an AI agent.

Every Digital Worker must have a signed, approved DJD before it is 
registered with SPIRE. No DJD means no Identity Gate clearance. No 
Identity Gate clearance means no deployment.

---

## Document metadata

| Field | Value |
|-------|-------|
| Worker ID | |
| Worker name | |
| Version | |
| Status | Draft / Under review / Approved / Superseded |
| Date created | |
| Date approved | |
| Approved by | |
| Business owner | |
| Next review date | |

---

## 1. Worker identity

**Worker ID**  
Unique identifier. Must match the SPIRE registration entry exactly.

**Worker name**  
Human-readable name. Descriptive of function, not technology.  
Example: `GRC-Compliance-Monitor-01` not `GPT-Agent-7`.

**Worker type**  
Specify one: Monitoring / Analysis / Reporting / Execution / Escalation

**Deployment environment**  
Specify one: Development / Shadow Mode / Full Agency

---

## 2. Scope of authority

Define precisely what this worker is permitted to do. Be specific. 
Ambiguity at this stage becomes a compliance gap at audit.

**Permitted actions**

| Action | Scope | Conditions |
|--------|-------|------------|
| | | |
| | | |
| | | |

**Prohibited actions**

List explicitly. Do not rely on the absence of a permitted action as 
an implied prohibition. State prohibitions clearly.

| Action | Reason for prohibition |
|--------|----------------------|
| | |
| | |

**Data access**

| Data source | Access level | Retention permitted |
|-------------|-------------|-------------------|
| | Read / Write / None | Yes / No |
| | | |

---

## 3. Threshold of autonomy

Defines the boundary between autonomous action and required human 
approval.

**Operating mode**  
Specify one:

- **Shadow Mode** — Worker executes all tasks. Human approves every 
  action before it takes effect. No action executes without explicit 
  approval.
- **Full Agency** — Worker acts autonomously within defined boundaries. 
  Human monitors output and receives escalations. Individual actions 
  do not require prior approval.

**Escalation triggers**

Define the conditions under which the worker must escalate to a human 
rather than act autonomously.

| Trigger | Escalation recipient | Maximum response time |
|---------|--------------------|--------------------|
| | | |
| | | |

**Confidence threshold**  
Minimum confidence score required before the worker acts without 
escalation: _____%

**Monetary threshold**  
Maximum transaction or commitment value the worker may authorise 
autonomously: £_____

---

## 4. Success metrics

Define how performance will be measured. Metrics must be observable, 
auditable, and tied to business outcomes rather than model outputs.

| Metric | Target | Measurement method |
|--------|--------|------------------|
| | | |
| | | |

---

## 5. Accountability

**Named business owner**  
The individual accountable for this worker's actions under SMCR.  
Name: ________________  
Role: ________________  
Senior Manager Function (if applicable): ________________

**Technical owner**  
The individual responsible for the worker's configuration and policy 
bundle.  
Name: ________________  
Role: ________________

**GRC owner**  
The individual responsible for audit trail integrity and conformity 
assessment.  
Name: ________________  
Role: ________________

---

## 6. Policy bundle

**OPA policy file**  
Location: ________________  
Version: ________________  
Hash (SHA-256): ________________

**Signing authority**  
Name: ________________  
Date signed: ________________  
Signature reference: ________________

---

## 7. Identity and access

**SPIFFE/SVID configuration**

| Parameter | Value |
|-----------|-------|
| SPIFFE ID | spiffe://[trust-domain]/[worker-id] |
| Standard TTL | 15 minutes |
| High-assurance TTL | 5 minutes |
| SPIRE registration entry | |

**Kill Switch procedure**  
Revocation method: SPIRE registration entry deletion  
Revocation window: Within SVID TTL (maximum 15 minutes)  
Kill Switch tested: Yes / No  
Test date: ________________  
Tested by: ________________

A Kill Switch that has never been tested is not a control.

---

## 8. Audit and logging

**Attribution Ledger**  
Location: ________________  
Chain integrity verification: HMAC-SHA256  
Retention period: ________________  
Regulatory basis: EU AI Act Article 12

**Log contents**  
Every Attribution Ledger entry must capture:
- Timestamp
- Worker ID
- Action taken
- Input data reference
- Output data reference
- Confidence score
- Human approver (Shadow Mode only)
- Escalation flag

---

## 9. Regulatory mapping

| Regulation | Requirement | Satisfied by |
|------------|-------------|-------------|
| EU AI Act Article 12 | Record-keeping and logging | Attribution Ledger |
| EU AI Act Article 14 | Human oversight | Shadow Mode / Escalation triggers |
| EU AI Act Article 17 | Quality management | DJD version control and review cycle |
| DORA | ICT risk management | Kill Switch / Incident escalation |
| FCA Consumer Duty | Audit trail | Attribution Ledger |
| SMCR | Named accountability | Section 5 of this document |

---

## 10. Change management

Any change to this document requires:
1. New version number
2. Re-approval by business owner
3. Updated OPA policy bundle (if scope changes)
4. Re-verification of SPIRE registration entry
5. Re-clearance of affected Five Gates

A changed DJD that has not been re-approved is not an approved DJD.

---

## 11. Review and sign-off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Business Owner | | | |
| Risk & Compliance | | | |
| Technical Lead | | | |
| GRC Analyst | | | |
| CISO / DPO | | | |

---

## Document history

| Version | Date | Author | Change summary |
|---------|------|--------|----------------|
| 1.0 | | | Initial issue |
| | | | |

---

*Part of the Governed Digital Worker Reference Architecture.*  
*Published under CC BY 4.0. Attribution required.*  
*https://github.com/KaosKal/reclaimed-workforce*
