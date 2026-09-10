# Verdant Pay Limited
## Stage 3, Part 4: Control Environment Map
**Confidential | Internal Use Only**

## Purpose

This document maps the current control environment across Verdant 
Pay's four defined scope areas. It consolidates findings from 
documentation review, stakeholder interviews, and technical discovery 
into a structured assessment of what controls exist, their type, their 
maturity, and the evidence supporting each rating. This control 
environment map forms the evidentiary foundation for risk identification 
and rating in Stage 4.

## Maturity Scale

| Rating | Definition |
|---|---|
| Strong | Control exists, is documented, and evidence confirms it is operating as intended |
| Moderate | Control exists and is documented but evidence suggests inconsistent operation |
| Weak | Control exists on paper but evidence confirms it is not operating effectively in practice |
| Absent | No control exists either in documentation or in practice |

## Control Type Definitions

- **Preventive:** Stops an incident from happening before it occurs
- **Detective:** Identifies a problem or gap that already exists
- **Corrective:** Addresses and corrects a confirmed problem after 
  it has occurred

---

## Control Environment Map

| Scope Area | Control Name | Control Type | Maturity Rating | Evidence Summary | Follow-up Required |
|---|---|---|---|---|---|
| Identity and Access Management | Offboarding Access Deprovisioning Process | Preventive | Weak | HR notification to IT takes three to five business days against a documented 24-hour requirement. No confirmation loop exists between HR and IT to verify that account deactivation was completed following notification. Directly explains Q1 2026 flagged incident of former staff accounts remaining active after offboarding. | Obtain IT helpdesk ticket logs for offboarding requests over last 12 months to measure actual revocation turnaround times. |
| Identity and Access Management | Conditional Access Policies in M365 | Preventive | Weak | Policies exist in documentation but CISO confirmed several controls documented as active are not functioning at the level documentation implies. Technical verification required to confirm operational status of specific configurations. | Review M365 admin center conditional access policy dashboard to confirm which policies are active and correctly configured. |
| Identity and Access Management | Privileged Access Management | Preventive | Absent | CISO explicitly confirmed no formal privileged access management process exists at Verdant Pay. Privileged accounts are not formally inventoried, reviewed, or governed through a defined process. | Obtain full privileged account inventory from Cloud Administrator to confirm scope of exposure. |
| Identity and Access Management | Periodic Access Reviews | Detective | Weak | Cloud Administrator confirmed last formal access review was eight months ago against a quarterly requirement. Review was manual, undocumented, and had no formal sign-off from IT Manager or compliance representative. | Obtain any available output from last permission review and M365 admin center user export used during that review. |
| Customer Data Handling | Data Classification Policy | Preventive | Absent | DPO confirmed no approved data classification policy exists in operational form. Draft framework has awaited formal approval for six months. Staff treat all data the same regardless of sensitivity, creating direct NDPA 2023 Section 24 exposure. | Obtain DPO's draft data classification framework to assess suitability as interim control pending formal approval. |
| Customer Data Handling | Acceptable Use Guidelines | Preventive | Weak | Policy exists and was distributed during onboarding but DPO confirmed no monitoring or enforcement mechanism exists. Senior Product Operations Manager interview revealed active violations including WhatsApp use for customer data communications and personal OneDrive storage for dispute records. | Obtain current Acceptable Use Policy and staff acknowledgment records held by HR. |
| Customer Data Handling | Access Restriction to Customer Data | Preventive | Weak | Access restriction controls exist within SharePoint and Azure but Cloud Administrator confirmed permissions expanded beyond originally intended boundaries without detection. Last formal permission review was eight months ago. | Review current SharePoint permission report and compare against original design documentation to identify all expanded permission boundaries. |
| Customer Data Handling | Encryption of Customer Data | Preventive | Weak | No documented encryption standard exists within the absent data classification policy. No formal encryption requirement has been defined or communicated for different categories of customer data. Technical verification of current encryption status required. | Review Azure storage account configurations and encryption settings dashboard to confirm encryption status across all customer data storage services. |
| Customer Data Handling | Breach Notification Procedure | Corrective | Absent | No operational breach notification procedure confirmed during stakeholder interviews. Given the absence of an approved data classification policy, which is the foundational control defining what constitutes sensitive data and therefore what requires breach notification, it is reasonably inferred that no operational breach notification procedure exists. This inference is consistent with the broader governance posture finding that key policies across Verdant Pay are either absent or inactive. This gap creates direct regulatory exposure under NDPA 2023 which requires data controllers to notify the Nigeria Data Protection Commission of a data breach within 72 hours. | Follow up directly with DPO and CCO to confirm existence and operational status of breach notification procedure before risk rating is finalized. |
| Cybersecurity Awareness and Human Risk | Cybersecurity Awareness Training Program | Preventive | Moderate | Annual training exists and completion is tracked through M365 learning platform. However HR confirmed training occurs once annually without formal knowledge retention assessment, making effectiveness inconsistent and unverifiable beyond completion records. | Obtain most recent training completion report from M365 learning platform broken down by department. |
| Cybersecurity Awareness and Human Risk | Formal Knowledge Assessment | Detective | Absent | HR confirmed no formal assessment or test exists at end of training. Completion is recorded but knowledge retention is not measured, meaning organization cannot verify whether training has produced meaningful change in staff security behavior. | Design and propose formal post-training knowledge assessment as part of remediation recommendations in Stage 8. |
| Cybersecurity Awareness and Human Risk | Phishing Simulation Program | Preventive and Detective | Absent | No phishing simulation program was referenced by any stakeholder across all seven interviews. At a fintech processing NGN 2.1 billion in monthly transactions, the absence of phishing simulation represents a significant unverified human risk exposure. | Propose phishing simulation program as priority remediation recommendation in Stage 8. |
| Cybersecurity Awareness and Human Risk | Credential Sharing Detection | Detective | Absent | Audit logs are not regularly reviewed, meaning credential sharing identified during Senior Product Operations Manager interview has gone undetected and unchallenged. Behavior has continued without consequence or correction. | Review M365 sign-in logs and activity logs for impossible travel patterns, concurrent sessions, and unusual activity volumes to confirm scope of credential sharing exposure. |
| Cybersecurity Awareness and Human Risk | Continuous Security Awareness Communications | Preventive | Absent | No ongoing security awareness communications program was referenced by HR, CISO, or any other stakeholder. Security awareness is limited to annual mandatory training with no reinforcement through regular communications or security reminders between training cycles. | Propose continuous security awareness communications program as remediation recommendation in Stage 8. |
| Cybersecurity Awareness and Human Risk | Management Reinforcement of Security Behaviors | Preventive | Absent | Senior Product Operations Manager disclosed staff use personal WhatsApp groups for customer data communications and share credentials during peak periods, confirming management is not actively reinforcing expected security behaviors within teams. | Propose formal management accountability framework for security behavior enforcement as remediation recommendation in Stage 8. |
| Governance and Policy Posture | Policy Review and Management Control | Preventive and Detective | Weak | CCO confirmed policies exist but are not reviewed on schedule. Two key policies, data classification and third-party risk management, are either absent or inactive against documented governance framework requirements. | Obtain current policy register showing status, version, and last review date for all active policies. |
| Governance and Policy Posture | Remediation Tracking Control | Detective | Weak | CCO confirmed remediation tracker exists for open CBN examination findings. However two of three open findings have exceeded target remediation deadlines without being closed, indicating tracker is not driving timely remediation action. | Obtain full CBN examination remediation tracker including current status of all three open findings and responsible owners. |
| Governance and Policy Posture | Third Party Risk Management | Preventive and Detective | Absent | CCO confirmed Third Party Risk Management Policy exists only in draft form and has never been operationalized. Several vendors with cloud-adjacent access have never been formally assessed, including unapproved external document conversion tool identified during Senior Product Operations Manager interview. | Obtain list of all current vendors with access to or adjacency to Verdant Pay's cloud environment for retrospective risk assessment. |
| Governance and Policy Posture | Policy Approval Governance Control | Preventive | Absent | No formal policy approval timeline or escalation process exists. DPO's draft data classification framework has sat unapproved for six months with no escalation or resolution, confirming policy approval process is not functioning as a governance control. | Establish formal policy approval timeline and escalation process as priority governance recommendation in Stage 8. |

---

## Control Environment Summary

| Maturity Rating | Number of Controls | Percentage |
|---|---|---|
| Strong | 0 | 0% |
| Moderate | 1 | 5% |
| Weak | 8 | 42% |
| Absent | 9 | 47% |
| Unconfirmed | 1 | 5% |
| **Total** | **19** | **100%** |

## Key Observations

Zero controls rated as strong across all four scope areas. Not one 
control across all four assessed scope areas was operating at full 
design effectiveness.

Nine controls rated as absent represent nearly half of all assessed 
controls. This is not a picture of weak controls that need 
strengthening. It is a picture of systemic governance gaps where 
entire control categories do not exist, particularly across 
cybersecurity awareness and governance posture.

The single moderate control, the annual cybersecurity training program, 
is the only control approaching acceptable effectiveness, and even this 
is undermined by the complete absence of knowledge retention assessment, 
phishing simulation, and ongoing security communications to reinforce it.

Eight weak controls confirm that Verdant Pay has made efforts to 
establish a control framework but has not invested in ensuring those 
controls operate effectively in practice. The gap between documented 
controls and operating effectiveness is the defining characteristic 
of Verdant Pay's current security posture.

These findings collectively confirm that Verdant Pay's control 
environment requires significant investment across all four scope areas 
before the Q4 2026 CBN examination.
