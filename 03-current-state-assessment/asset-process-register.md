# Verdant Pay Limited
## Asset and Process Register
**Confidential | Internal Use Only**

## Purpose

This register documents the key assets and processes identified during 
Stage 3 of the Verdant Pay cyber risk assessment. It establishes a 
clear inventory of what is being protected, who owns it, and why it 
is relevant to the four defined scope areas. Every asset and process 
listed here was identified through stakeholder engagement, documentation 
review, and technical discovery activities conducted across Stage 3.

---

## Asset Register

### Category 1: People Assets

**Staff Accounts**
Owner: Head of IT Infrastructure and Head of People Operations jointly.
Scope relevance: Identity and Access Management. These accounts 
represent the primary access control surface across all in-scope 
systems. Directly relevant to the Q1 2026 flagged incident confirming 
that former staff accounts remained active after offboarding, indicating 
a breakdown in the joint ownership process between People Operations 
and IT.

**Privileged User Accounts**
Owner: Head of IT Infrastructure and Cloud Administrator.
Scope relevance: Identity and Access Management. These accounts carry 
elevated access rights that create heightened risk if compromised, 
misconfigured, or left active after a staff exit. Directly connects 
to the CISO's interview finding that no formal privileged access 
management process exists at Verdant Pay.

**Access Rights and Permission Assignments**
Owner: Cloud Administrator.
Scope relevance: Identity and Access Management, Customer Data Handling. 
These represent the specific entitlements attached to each user account 
and determine what data and systems each individual can reach. Directly 
connects to the Q1 2026 flagged incident confirming that SharePoint 
permissions expanded beyond originally intended boundaries.

---

### Category 2: Data Assets

**Customer Personal and Financial Data**
Owner: Data Protection Officer.
Scope relevance: Customer Data Handling. This is Verdant Pay's highest 
sensitivity data asset, subject to NDPA 2023, CBN Cybersecurity 
Framework, and PCI-DSS protection requirements. Directly connects to 
the absence of a formal data classification policy identified in Q1 2026 
and the Senior Product Operations Manager's disclosure of customer data 
being stored in personal OneDrive folders and processed through an 
unapproved external document conversion tool.

**Internal HR Data**
Owner: Head of People Operations.
Scope relevance: Customer Data Handling, Governance and Policy Posture. 
Sensitive personal data subject to NDPA 2023 obligations. Connects to 
the interview finding that no formal data handling review has been 
conducted for internally held staff data.

**Transaction Records and Operational Data**
Owner: Senior Product Operations Manager.
Scope relevance: Customer Data Handling. Generated daily through the 
transaction processing workflow. Connects to the interview finding that 
dispute records containing customer names, account numbers, and 
transaction details are being maintained in an unapproved personal 
OneDrive tracker outside officially sanctioned systems.

**Compliance Documentation**
Owner: Chief Compliance Officer.
Scope relevance: Governance and Policy Posture. The evidentiary 
foundation of Verdant Pay's regulatory standing. Directly connects 
to the interview finding that two of three open CBN examination 
findings have exceeded their remediation deadlines.

---

### Category 3: System Assets

**Microsoft 365 Environment**
Owner: Head of IT Infrastructure and Cloud Administrator.
Scope relevance: All four scope areas. Verdant Pay's primary internal 
collaboration and communication platform and the central system through 
which most in-scope risks have been identified. Primary technical 
discovery environment for this assessment.

**Microsoft Azure Cloud Infrastructure**
Owner: Cloud Administrator.
Scope relevance: Identity and Access Management, Customer Data Handling. 
The underlying cloud platform supporting Verdant Pay's payment processing 
operations and data storage. Connects to the technical discovery 
requirement to verify encryption settings and storage configurations 
for customer financial data.

**Operations Dashboard**
Owner: Senior Product Operations Manager.
Scope relevance: Identity and Access Management, Customer Data Handling. 
Used daily for transaction processing and exception management. Directly 
connects to the interview finding that staff share credentials to access 
this dashboard during peak processing periods, eliminating individual 
accountability for system actions.

**Unapproved Third-Party Tools**
Owner: No formal ownership assigned.
Scope relevance: Customer Data Handling, Governance and Policy Posture. 
Includes the external document conversion tool and informal project 
management platform identified during the Senior Product Operations 
Manager interview. Not officially sanctioned by IT and not assessed for 
security risk. Represent a shadow IT exposure requiring immediate 
remediation.

---

## Process Register

### Process 1: Staff Onboarding and Offboarding Workflow
**Owner:** Head of People Operations and Head of IT Infrastructure 
jointly.
**Scope area:** Identity and Access Management.
**Relevance:** Governs how staff access is provisioned when someone 
joins Verdant Pay and deprovisioned when someone leaves. Directly 
connects to the Q1 2026 flagged incident of former staff accounts 
remaining active after offboarding and to interview findings confirming 
that the notification process between People Operations and IT is 
delayed and lacks a confirmation loop. This process is the single most 
critical process gap identified in the assessment.

---

### Process 2: Transaction Processing Workflow
**Owner:** Senior Product Operations Manager.
**Scope areas:** Customer Data Handling, Identity and Access Management.
**Relevance:** Governs how customer transactions are processed, 
escalated, and resolved daily by the operations team. Connects to the 
ground-level operational reality of how customer data is actually 
handled in practice, including the informal workarounds, credential 
sharing, and unapproved tool use identified during the Senior Product 
Operations Manager interview.

---

### Process 3: Customer Data Handling Process
**Owner:** Data Protection Officer.
**Scope area:** Customer Data Handling.
**Relevance:** Governs how customer personal and financial data is 
classified, stored, accessed, shared, and protected across Verdant 
Pay's cloud environment. Directly connects to the absence of an 
approved data classification policy identified in Q1 2026 and the 
DPO's interview finding that a draft classification framework has 
awaited formal approval for six months.

---

### Process 4: Policy Review and Approval Cycle
**Owner:** Chief Compliance Officer.
**Scope area:** Governance and Policy Posture.
**Relevance:** Governs how Verdant Pay's key policies are drafted, 
reviewed, approved, communicated to staff, and kept current against 
evolving regulatory requirements. Directly connects to the 
organization's regulatory standing with CBN and to the examination 
readiness assessment ahead of Q4 2026. Interview findings confirmed 
that two key policies are either absent or inactive, and that two of 
three open CBN examination findings have exceeded their remediation 
deadlines.
