# Paraclete — Cyber Risk Assessment

An end-to-end cyber risk assessment designed for a fictional Lagos-based fintech, covering everything from scope 
definition through to a prioritized risk register with treatment plans under Nigerian regulatory conditions.

---

## The Organization

Paraclete is a fictional cloud-native fintech operating a digital payments platform for peer-to-peer transfers, bill payments, 
and merchant collections across Nigeria. For the purposes of this simulated assessment, Paraclete is assumed to operate under a CBN-regulated payment-services model and serves approximately 340,000 active users processing NGN 2.1 billion in monthly transactions.

In Q1 2026, Paraclete's compliance team flagged three concerns 
during a routine internal review:

- Former staff accounts remained active in the M365 environment 
  weeks after offboarding
- SharePoint permissions had expanded beyond originally intended 
  boundaries
- No formal data classification policy existed to govern how 
  sensitive customer financial data was being handled internally

These findings triggered a board-authorized cyber risk assessment 
ahead of a planned Series B fundraising round and a CBN regulatory 
examination expected in Q4 2026.

---

## What Was Assessed

Four scope areas across Paraclete's cloud environment:

- Identity and Access Management
- Customer Data Handling
- Cybersecurity Awareness and Human Risk
- Governance and Policy Posture

Physical infrastructure, on-premises hardware, and consumer-facing 
application security were explicitly excluded with documented 
justification.

---

## Methodology

Eight stages, each building directly on the last:

| Stage | Description |
|---|---|
| 1 | Scope definition and boundary setting |
| 2 | Stakeholder identification and engagement planning |
| 3 | Information gathering and current state assessment |
| 4 | Threat and vulnerability identification |
| 5 | Inherent risk assessment using likelihood and impact |
| 6 | Existing control effectiveness assessment |
| 7 | Residual risk assessment |
| 8 | Risk register with treatment plans and recommendations |

Full methodology detail: [docs/methodology.md](docs/methodology.md)

---

## Key Findings

### Control Environment

Nineteen controls were assessed across all four scope areas.

| Maturity Rating | Count | Percentage |
|---|---|---|
| Strong | 0 | 0% |
| Moderate | 1 | 5% |
| Weak | 8 | 42% |
| Absent | 9 | 47% |
| Unconfirmed | 1 | 5% |

Not one control across all four scope areas was operating at full 
design effectiveness. Nine control categories did not exist at all.

### Risk Profile

| Stage | Critical | High | Medium | Low |
|---|---|---|---|---|
| Inherent Risk | 19 | 0 | 0 | 0 |
| Residual Risk | 16 | 3 | 0 | 0 |
| Target After Treatment | 0 | 2 | 13 | 4 |

Every identified risk rated critical before controls were considered. 
Sixteen remained critical after existing controls were applied, 
reflecting the minimal protective value of a control environment 
where no control reached high or moderate effectiveness.

Full implementation of all nineteen treatment plans would reduce 
Paraclete's risk profile from nineteen critical risks to an 
acceptable level.

---

## Regulatory Frameworks Applied

| Framework | Application |
|---|---|
| CBN Cybersecurity Framework for Payment Service Providers | Examination readiness assessment, governance posture evaluation, remediation prioritization |
| Nigeria Data Protection Act 2023 (NDPA 2023) | Customer data classification, breach notification requirements, regulatory exposure assessment |
| PCI-DSS | Customer financial data protection, encryption requirements, access control standards |

---
