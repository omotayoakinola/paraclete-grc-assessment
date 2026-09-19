# Paraclete
## Stakeholder Identification and Engagement Plan
**Confidential | Internal Use Only**

## Purpose

This document identifies the key stakeholders relevant to the cyber 
risk assessment at ParacletE and outlines the specific 
information required from each. The stakeholder engagement process 
is structured around the four defined scope areas: identity and access 
management, customer data handling, cybersecurity awareness and human 
risk, and governance and policy posture.

## Stakeholder Identification Methodology

Stakeholders were identified by following four logical trails:

- The four scope areas and who owns, operates, or is affected by each
- The three incidents flagged by the compliance team in Q1 2026 and 
  who was responsible for or affected by them
- Decision authority, meaning who approves policies, controls access, 
  and reports to regulators
- Data flow, meaning whose hands customer and internal data passes 
  through across the organization

Each identified stakeholder was validated against three questions: 
do they know something the assessment needs, do they own something 
being assessed, and do they have authority to act on findings. Only 
stakeholders meeting at least one of these criteria were included.

## Stakeholder Register

### 1. Head of IT Infrastructure
**Primary scope area:** Identity and Access Management.

**What they uniquely know:** The technical reality of how access is 
provisioned, managed, and configured across the M365 environment. 
They have direct visibility into user provisioning workflows, privileged 
access assignments, conditional access policy configurations, and how 
the M365 environment is actually administered day to day.

**Information required:** Current user provisioning and offboarding 
process from the IT side. Privileged access assignments and review 
history. Conditional access policy configuration. Evidence of any 
access reviews conducted. How IT receives and acts on offboarding 
notifications from People Operations. Technical access review records 
showing periodic confirmation that access assignments remain appropriate 
and that no unauthorized or outdated access exists.

---

### 2. Cloud Administrator
**Primary scope areas:** Customer Data Handling, Identity and Access 
Management.

**What they uniquely know:** The technical reality of how customer data 
is stored and accessed within Azure and M365. They can show what is 
actually configured versus what policy says should be configured, which 
is where the most significant data handling risks are likely to surface.

**Information required:** How customer data is stored in Azure and which 
systems hold it. Who currently has permissions to access SharePoint 
folders containing financial data. Whether those permissions have been 
reviewed recently and by whom. Any misconfigurations or unintended access 
points identified. Whether the current technical configuration matches 
what the DPO's policies say should be in place. Configuration exports, 
permission reports, and access logs showing what is actually configured 
right now rather than what policy says should exist.

---

### 3. Head of People Operations
**Primary scope areas:** Identity and Access Management, Cybersecurity 
Awareness and Human Risk, Governance and Policy Posture.

**What they uniquely know:** The full employee lifecycle from onboarding 
to offboarding, including how access requirements are communicated to IT 
when staff join and how IT is notified when staff leave. They also hold 
training completion records, policy acknowledgment records, and internal 
HR data handling practices.

**Information required:** The formal process for communicating new staff 
access requirements to IT during onboarding. The formal offboarding 
notification process to IT for access deactivation. Cybersecurity 
training completion records, training frequency, and any knowledge 
assessment results. Records of staff acknowledgment of key policies 
including the acceptable use policy. How sensitive internal HR data 
including employment contracts, salary records, and performance 
information is stored and handled internally. Proof of acceptable use 
guidelines as they relate to staff access.

---

### 4. Data Protection Officer
**Primary scope area:** Customer Data Handling.

**What they uniquely know:** The regulatory and policy obligations 
governing how Paraclete handles customer personal data under NDPA 
2023. They understand what the organization is legally required to do 
with customer data including consent mechanisms, data subject rights, 
breach notification obligations, and data classification requirements.

**Information required:** How customer data is formally classified and 
what policy governs its handling. Acceptable use guidelines covering 
data use across all stakeholders. Consent mechanisms currently in place. 
Breach notification history and any regulatory correspondence related 
to data protection. Compliance evidence including audit trails relevant 
to customer data. Data subject request handling procedures. Current data 
handling practices showing how data moves through the organization day 
to day.

---

### 5. Chief Compliance Officer
**Primary scope areas:** Governance and Policy Posture, Cybersecurity 
Awareness and Human Risk.

**What they uniquely know:** The organization's regulatory standing with 
CBN, the history of examinations and findings, and the current state of 
the internal policy framework. They know what CBN expects, what gaps 
have previously been identified, what open remediation commitments exist, 
and how confident the organization should be about its Q4 2026 
examination readiness.

**Information required:** Current status of all key policies including 
acceptable use, data classification, incident response, and third-party 
risk management. Date of last review for each policy. Findings from the 
most recent CBN examination and status of any open remediation 
commitments. Current assessment of examination readiness for Q4 2026. 
Any regulatory correspondence received since the last examination. 
Internal and external compliance policies and frameworks currently in 
operation.

---

### 6. Chief Information Security Officer
**Primary scope areas:** Governance and Policy Posture, Identity and 
Access Management.

**What they uniquely know:** The organization's overall security 
strategy, control design decisions, known gaps, and risk tolerance. 
They know what security controls were designed for each scope area, 
why they were designed that way, what controls were put in place in 
response to the three Q1 2026 flagged incidents, and where the 
organization knowingly accepts risk versus where gaps are unintentional.

**Information required:** Security controls currently in place across 
all four scope areas and how they are reviewed. What controls were 
designed specifically in response to the three Q1 2026 flagged incidents 
and whether those controls are now operating effectively. Known security 
gaps currently being tracked. The organization's formally defined risk 
tolerance or risk appetite. Incident response capability in practice, 
not just on paper. Overall security posture documentation across all 
four scope areas.

---

### 7. Senior Product Operations Manager
**Primary scope areas:** Identity and Access Management, Customer Data 
Handling, Cybersecurity Awareness and Human Risk.

**What they uniquely know:** They have ground-level visibility into how 
the operations team actually works day to day, close enough to 
operational reality to know where official processes break down and 
senior enough to have visibility across the entire operations function. 
They are the primary source of information about workarounds, informal 
practices, and shadow IT that no policy document, configuration review, 
or technical scan would surface.

**Information required:** Any informal process guides or team SOPs the 
operations team uses internally that may not be formally documented. 
Any third-party tools or platforms the team uses that may not be 
formally approved by IT. Any internal communications or trackers that 
involve customer data outside of officially sanctioned systems. How the 
operations team actually behaves around security practices under 
pressure, whether staff follow data handling guidelines, whether 
credentials are shared informally, and whether unapproved shortcuts are 
taken when official processes are slow or inconvenient.

## Engagement Approach

Each stakeholder will be engaged through a structured one-on-one 
interview. Questions will be tailored specifically to each role rather 
than using a generic question list, ensuring that each interview 
extracts information only that stakeholder can provide.

Interviews will be preceded by a short written communication to each 
stakeholder explaining the purpose of the assessment, what will be 
discussed, and any documentation they should have available during 
the session.

Following each interview, a summary of findings will be circulated 
back to the relevant stakeholder for validation before findings are 
incorporated into the assessment. This ensures accuracy and protects 
against misinterpretation.

Where documentation is referenced during interviews, formal requests 
will be made in writing so that a clear evidence trail exists linking 
each risk finding to its source.
