# Paraclete
## Stage 6: Existing Control Assessment
**Confidential | Internal Use Only**

## Purpose

This document assesses the effectiveness of existing controls at 
Paraclete against each of the nineteen identified risks. While 
Stage 3 Part 4 assessed the general maturity of each control across 
scope areas, Stage 6 asks a more specific question: for each 
identified risk, how much protection do existing controls actually 
provide against that specific threat and vulnerability? The output 
of this assessment feeds directly into Stage 7 where residual risk 
is calculated by applying control effectiveness against inherent 
risk scores.

## Control Effectiveness Rating Scale

| Rating | Definition |
|---|---|
| High | The control substantially reduces the likelihood or impact of the risk |
| Moderate | The control partially reduces the likelihood or impact but gaps remain |
| Low | The control provides minimal reduction in likelihood or impact |
| Ineffective | The control exists on paper but provides no meaningful protection against this specific risk |
| Absent | No control exists to address this risk at all |

---

## Area 1: Identity and Access Management

### Risk 1: Unauthorised Access by Former Staff

**Control 1: Offboarding Access Deprovisioning Process**
Effectiveness: Low
Justification: The control exists and is designed to prevent 
unauthorised access by former staff but consistently fails to operate 
within its documented 24-hour requirement, taking three to five 
business days instead, and has no confirmation loop to verify 
completion.

**Control 2: Conditional Access Policies**
Effectiveness: Ineffective
Justification: Conditional access policies are not confirmed as 
operational, meaning they provide no reliable barrier against a former 
staff member accessing M365 using still-active credentials.

**Control 3: Privileged Access Management**
Effectiveness: Absent
Justification: No formal privileged access management process exists, 
meaning there is no inventory of what elevated permissions a former 
staff member held, making complete access revocation during offboarding 
unverifiable.

**Control 4: Periodic Access Reviews**
Effectiveness: Ineffective
Justification: Access reviews occur approximately once every eight 
months against a quarterly requirement and are undocumented, providing 
no meaningful ongoing detection of former staff accounts remaining 
active between review cycles.

**Overall Control Effectiveness: Low**
One control provides minimal protection through the offboarding 
process, two are ineffective, and one is absent. The overall protective 
value against this risk is minimal.

---

### Risk 2: Authentication Bypass Through Weak Conditional Access

**Control 1: Conditional Access Policies**
Effectiveness: Low
Justification: Policies exist in documentation but are not confirmed 
as fully operational. They provide some theoretical protection against 
authentication bypass but the CISO confirmed their operational 
effectiveness cannot be relied upon.

**Control 2: Privileged Access Management**
Effectiveness: Absent
Justification: No formal privileged access management process exists, 
meaning privileged accounts are not protected against authentication 
bypass through legacy protocols or AiTM attacks.

**Control 3: Periodic Access Reviews**
Effectiveness: Ineffective
Justification: Periodic access reviews examine who has access but do 
not address authentication security configurations or detect 
authentication bypass attempts.

**Overall Control Effectiveness: Low**
One control provides minimal theoretical protection through conditional 
access policies but their operational status is unconfirmed. Remaining 
controls are absent or ineffective against this specific risk.

---

### Risk 3: Privilege Escalation Through Ungoverned Privileged Access

**Control 1: Privileged Access Management**
Effectiveness: Absent
Justification: No formal privileged access management process exists 
at Paraclete. There is no inventory, review, or governance of 
privileged accounts, meaning no control exists to detect or prevent 
privilege escalation.

**Control 2: Periodic Access Reviews**
Effectiveness: Ineffective
Justification: Access reviews occur once every eight months against 
a quarterly requirement and are undocumented. Even if a review were 
conducted, the absence of a privileged account inventory means elevated 
permissions would not be systematically identified or challenged.

**Control 3: Conditional Access Policies**
Effectiveness: Ineffective
Justification: Conditional access policies govern how users 
authenticate but do not address the accumulation of permissions beyond 
legitimate scope by users who are already authenticated.

**Overall Control Effectiveness: Absent to Ineffective**
The primary control needed to address this risk, privileged access 
management, is completely absent. Remaining controls are ineffective 
against privilege escalation specifically. This risk has virtually no 
protective controls in place.

---

### Risk 4: Undetected Permission Creep Through Infrequent Access Reviews

**Control 1: Periodic Access Reviews**
Effectiveness: Low
Justification: Access reviews are designed to detect permission creep 
but occur once every eight months against a quarterly requirement. 
They are undocumented and unsigned. The control exists and provides 
some minimal detection capability but is operating far below the 
frequency and rigor needed to effectively manage permission creep.

**Control 2: Conditional Access Policies**
Effectiveness: Ineffective
Justification: Conditional access policies control how users 
authenticate but do not detect or correct permission creep within 
already authenticated sessions.

**Control 3: Privileged Access Management**
Effectiveness: Absent
Justification: The absence of privileged access management means 
elevated permission assignments are not tracked or reviewed, allowing 
privileged permission creep to go entirely undetected.

**Overall Control Effectiveness: Low**
One control provides minimal detection capability through infrequent 
access reviews. Remaining controls are ineffective or absent against 
this specific risk.

---

## Area 2: Customer Data Handling

### Risk 5: Unprotected Customer Data Due to Absent Data Classification

**Control 1: Data Classification Policy**
Effectiveness: Absent
Justification: No approved data classification policy exists in 
operational form. No classification framework exists to guide staff 
in handling customer financial data proportionate to its sensitivity.

**Control 2: Acceptable Use Guidelines**
Effectiveness: Ineffective
Justification: The Acceptable Use Policy exists but has no monitoring 
or enforcement mechanism. Without data classification defining what 
constitutes sensitive data, the acceptable use policy cannot 
effectively guide staff behavior around customer financial data 
specifically.

**Control 3: Access Restriction to Customer Data**
Effectiveness: Low
Justification: Access restrictions exist within SharePoint and Azure 
but have expanded beyond intended boundaries. They provide some minimal 
protection by limiting access to some degree but cannot compensate for 
the complete absence of data classification guidance.

**Control 4: Encryption of Customer Data**
Effectiveness: Low
Justification: Some encryption may exist within Azure infrastructure 
but no documented encryption standard has been defined or communicated. 
Without data classification determining what requires encryption, 
encryption controls cannot be systematically applied proportionate to 
data sensitivity.

**Overall Control Effectiveness: Low to Ineffective**
The foundational control needed to address this risk, data 
classification policy, is completely absent. Remaining controls provide 
minimal or no effective protection without the classification framework 
that would give them operational context.

---

### Risk 6: Customer Data Exposure Through Policy Violations

**Control 1: Acceptable Use Guidelines**
Effectiveness: Ineffective
Justification: The Acceptable Use Policy explicitly prohibits the use 
of personal messaging platforms and personal cloud storage for business 
purposes. However active violations are already confirmed including 
WhatsApp use for customer data communications and personal OneDrive 
storage for dispute records. A policy with no monitoring or enforcement 
mechanism cannot prevent violations that are already occurring.

**Control 2: Data Classification Policy**
Effectiveness: Absent
Justification: No data classification policy exists to help staff 
understand the sensitivity of the data they are mishandling or the 
consequences of doing so through unapproved channels.

**Control 3: Management Reinforcement of Security Behaviors**
Effectiveness: Absent
Justification: No management accountability mechanism exists for 
security behavior enforcement, confirmed by the Senior Product 
Operations Manager's disclosure that violations occur without 
management challenge or correction.

**Overall Control Effectiveness: Ineffective to Absent**
The primary administrative control exists but is completely unenforced. 
Supporting controls are absent. Active violations are already confirmed, 
demonstrating that existing controls provide no meaningful protection 
against this risk.

---

### Risk 7: Unauthorized Access to Customer Data Through Expanded Permissions

**Control 1: Access Restriction to Customer Data**
Effectiveness: Low
Justification: Access restriction controls exist within SharePoint and 
Azure but the Cloud Administrator confirmed that permissions expanded 
beyond originally intended boundaries without detection, indicating 
controls are not operating within intended scope.

**Control 2: Periodic Access Reviews**
Effectiveness: Ineffective
Justification: Access reviews occur once every eight months against 
a quarterly requirement. The SharePoint permission expansion went 
undetected between reviews, demonstrating that the current review 
frequency is insufficient to catch unauthorized permission expansion 
in a timely manner.

**Control 3: Data Classification Policy**
Effectiveness: Absent
Justification: Without data classification, there is no framework 
defining who should have access to what categories of customer data, 
making it impossible to systematically assess whether current 
permission assignments are appropriate.

**Overall Control Effectiveness: Low**
One control provides minimal protection through access restrictions 
that have already proven insufficient to maintain intended boundaries. 
Remaining controls are ineffective or absent against this specific risk.

---

### Risk 8: Customer Data Interception Through Inadequate Encryption

**Control 1: Encryption of Customer Data**
Effectiveness: Low
Justification: Some encryption capability exists within Azure 
infrastructure but no documented encryption standard has been defined 
or applied systematically. The absence of a data classification policy 
means encryption cannot be applied proportionate to data sensitivity 
across all storage services.

**Control 2: Data Classification Policy**
Effectiveness: Absent
Justification: Without data classification defining what data requires 
what level of encryption protection, encryption controls cannot be 
systematically applied or verified across Paraclete's cloud 
environment.

**Control 3: Access Restriction to Customer Data**
Effectiveness: Low
Justification: Access restrictions provide some protection against 
unauthorized access to customer data but do not address the risk of 
data interception during transmission or exposure through inadequate 
encryption at rest.

**Overall Control Effectiveness: Low**
Minimal encryption capability exists within Azure infrastructure but 
is not systematically applied or documented. The foundational control 
needed to guide encryption decisions, data classification policy, 
is absent.

---

### Risk 9: Regulatory Sanction Due to Absent Breach Notification Procedure

**Control 1: Breach Notification Procedure**
Effectiveness: Absent
Justification: No operational breach notification procedure exists 
at Paraclete. The organization cannot currently determine what 
constitutes a notifiable breach, who should be notified, or within 
what timeframe.

**Control 2: Data Classification Policy**
Effectiveness: Absent
Justification: Without data classification, the organization cannot 
determine what data is subject to breach notification requirements 
under NDPA 2023 or PCI-DSS, making any breach notification attempt 
unstructured and likely incomplete.

**Control 3: Remediation Tracking Control**
Effectiveness: Ineffective
Justification: The remediation tracker exists for CBN examination 
findings but does not address the absence of a breach notification 
procedure as an operational control gap requiring immediate remediation.

**Overall Control Effectiveness: Absent**
No controls exist to address this risk. Both the breach notification 
procedure and the data classification policy that would inform it are 
completely absent. This risk has zero protective controls in place.

---

## Area 3: Cybersecurity Awareness and Human Risk

### Risk 10: Staff Susceptibility to Phishing and Social Engineering

**Control 1: Cybersecurity Awareness Training Program**
Effectiveness: Low
Justification: Annual training exists and covers phishing awareness 
but knowledge retention is unverified and training occurs only once 
per year without reinforcement. It provides some minimal protection 
but is insufficient to maintain staff vigilance against evolving 
phishing techniques throughout the year.

**Control 2: Formal Knowledge Assessment**
Effectiveness: Absent
Justification: No formal knowledge assessment exists, meaning the 
effectiveness of phishing awareness training cannot be verified 
or measured.

**Control 3: Phishing Simulation Program**
Effectiveness: Absent
Justification: No phishing simulation program exists at Verdant Pay. 
Staff susceptibility to phishing has never been tested, meaning the 
organization has no mechanism to identify and remediate vulnerable 
staff before a real attack occurs.

**Control 4: Continuous Security Awareness Communications**
Effectiveness: Absent
Justification: No ongoing security awareness communications program 
exists to reinforce phishing awareness between annual training cycles.

**Overall Control Effectiveness: Low**
One control provides minimal protection through annual training. Three 
supporting controls that would substantially strengthen protection 
against phishing are completely absent.

---

### Risk 11: Unverified Security Behavior Due to Absent Knowledge Assessment

**Control 1: Formal Knowledge Assessment**
Effectiveness: Absent
Justification: No formal knowledge assessment exists at the end of 
training. This is the primary control needed to address this risk 
and it is completely absent.

**Control 2: Cybersecurity Awareness Training Program**
Effectiveness: Low
Justification: Annual training exists and provides some foundation 
for security behavior but without assessment, its effectiveness in 
producing behavioral change cannot be verified or demonstrated to 
a CBN examiner.

**Overall Control Effectiveness: Low to Absent**
The primary control needed to address this risk is completely absent. 
The supporting training program provides minimal foundation but cannot 
compensate for the absence of knowledge verification.

---

### Risk 12: Undetected Phishing Susceptibility Across Staff

**Control 1: Phishing Simulation Program**
Effectiveness: Absent
Justification: No phishing simulation program exists at Paraclete. 
This is the primary control needed to detect and measure staff phishing 
susceptibility and it is completely absent.

**Control 2: Cybersecurity Awareness Training Program**
Effectiveness: Low
Justification: Annual training covers phishing awareness but cannot 
substitute for simulation exercises that test actual staff behavior 
under realistic phishing conditions.

**Control 3: Formal Knowledge Assessment**
Effectiveness: Absent
Justification: No knowledge assessment exists to measure whether 
phishing awareness training has produced any change in staff ability 
to identify phishing attempts.

**Overall Control Effectiveness: Low to Absent**
The primary control needed to address this risk, phishing simulation, 
is completely absent. Supporting controls provide minimal theoretical 
protection without the simulation program that would validate their 
effectiveness.

---

### Risk 13: Fraudulent Access Through Undetected Credential Sharing

**Control 1: Credential Sharing Detection**
Effectiveness: Absent
Justification: Audit logs are not regularly reviewed, meaning the 
credential sharing practice already confirmed during the Senior Product 
Operations Manager interview has gone undetected and unchallenged. 
No detective control exists to identify or prevent this behavior.

**Control 2: Acceptable Use Guidelines**
Effectiveness: Ineffective
Justification: The Acceptable Use Policy prohibits credential sharing 
but has no monitoring or enforcement mechanism. Credential sharing is 
already confirmed as an established practice, demonstrating that the 
policy provides no effective protection against this behavior.

**Control 3: Management Reinforcement of Security Behaviors**
Effectiveness: Absent
Justification: No management accountability mechanism exists. 
Credential sharing occurs during peak periods without management 
challenge or correction, confirming that management reinforcement 
provides no protection against this risk.

**Overall Control Effectiveness: Ineffective to Absent**
The primary detective control needed to identify credential sharing, 
audit log review, is absent. The administrative control that should 
prevent it is unenforced. Active credential sharing is already 
confirmed, demonstrating that existing controls provide no meaningful 
protection.

---

### Risk 14: Security Behavior Degradation Between Training Cycles

**Control 1: Continuous Security Awareness Communications**
Effectiveness: Absent
Justification: No ongoing security awareness communications program 
exists to reinforce security behaviors between annual training cycles. 
This is the primary control needed to address this risk and it is 
completely absent.

**Control 2: Cybersecurity Awareness Training Program**
Effectiveness: Low
Justification: Annual training provides some foundation but without 
reinforcement between cycles, behavioral degradation is confirmed as 
already occurring based on the policy violations identified during 
stakeholder interviews.

**Control 3: Management Reinforcement of Security Behaviors**
Effectiveness: Absent
Justification: No management accountability mechanism exists to 
reinforce security behaviors within teams between training cycles.

**Overall Control Effectiveness: Low to Absent**
The primary control needed to address this risk is completely absent. 
The supporting annual training program provides minimal foundation 
but is demonstrably insufficient to prevent behavioral degradation 
between cycles.

---

### Risk 15: Normalised Policy Violations Through Absent Management Accountability

**Control 1: Management Reinforcement of Security Behaviors**
Effectiveness: Absent
Justification: No management accountability mechanism exists for 
security behavior enforcement. Policy violations are confirmed as 
occurring without management challenge or correction, demonstrating 
complete absence of this control.

**Control 2: Acceptable Use Guidelines**
Effectiveness: Ineffective
Justification: The Acceptable Use Policy exists but is unenforced. 
Active violations are already normalised across the operations team, 
demonstrating that the policy provides no effective protection against 
normalized violations.

**Control 3: Continuous Security Awareness Communications**
Effectiveness: Absent
Justification: No ongoing communications program exists to reinforce 
policy compliance expectations between annual training cycles.

**Overall Control Effectiveness: Ineffective to Absent**
The primary control needed to address this risk, management 
accountability, is completely absent. Supporting controls are either 
unenforced or absent. Active policy violations are already normalised, 
demonstrating that existing controls provide no meaningful protection.

---

## Area 4: Governance and Policy Posture

### Risk 16: Regulatory Non-Compliance Due to Outdated or Absent Policies

**Control 1: Policy Review and Management Control**
Effectiveness: Low
Justification: A policy review cycle exists in principle but policies 
are not being reviewed on schedule and two key policies are either 
absent or inactive. The control provides minimal governance oversight 
but is operating far below the standard needed to maintain regulatory 
compliance.

**Control 2: Policy Approval Governance Control**
Effectiveness: Absent
Justification: No formal policy approval timeline or escalation process 
exists. The DPO's draft data classification framework has sat unapproved 
for six months, demonstrating that the policy approval process provides 
no effective governance over policy currency.

**Control 3: Remediation Tracking Control**
Effectiveness: Low
Justification: A remediation tracker exists for CBN examination findings 
and provides some minimal oversight of open compliance commitments, but 
two of three findings have exceeded their deadlines, limiting its 
effectiveness against this risk.

**Overall Control Effectiveness: Low**
One control provides minimal protection through an underperforming 
policy review cycle. The policy approval governance control is absent. 
Overall protection against regulatory non-compliance is minimal.

---

### Risk 17: Escalated Regulatory Findings Due to Overdue Remediation

**Control 1: Remediation Tracking Control**
Effectiveness: Low
Justification: A remediation tracker exists and provides some minimal 
visibility into open CBN examination findings. However two of three 
findings have exceeded their target remediation deadlines without being 
closed, demonstrating that the tracker is not driving timely remediation 
action effectively.

**Control 2: Policy Review and Management Control**
Effectiveness: Ineffective
Justification: The policy review cycle does not specifically address 
the tracking and closure of open regulatory examination findings within 
required timeframes.

**Overall Control Effectiveness: Low**
One control provides minimal protection through an underperforming 
remediation tracker. No other controls effectively address the specific 
risk of escalated regulatory findings due to overdue remediation.

---

### Risk 18: Supply Chain Attack Through Unassessed Third Party Vendors

**Control 1: Third Party Risk Management**
Effectiveness: Absent
Justification: The Third Party Risk Management Policy exists only in 
draft form and has never been operationalized. No vendor risk 
assessments have been conducted. This is the primary control needed 
to address this risk and it is completely absent.

**Control 2: Acceptable Use Guidelines**
Effectiveness: Ineffective
Justification: The Acceptable Use Policy requires IT approval for 
third party tools but has no monitoring or enforcement mechanism. 
The unapproved external document conversion tool is already confirmed 
as in use, demonstrating that the policy provides no effective 
protection against unapproved vendor use.

**Control 3: Policy Approval Governance Control**
Effectiveness: Absent
Justification: The absence of a functioning policy approval process 
means the Third Party Risk Management Policy remains in draft form 
indefinitely, preventing it from becoming an operational control.

**Overall Control Effectiveness: Absent to Ineffective**
The primary control needed to address this risk, third party risk 
management, is completely absent. Supporting controls are ineffective 
or absent. An unapproved vendor is already confirmed as processing 
customer reference data without a security assessment or data 
processing agreement.

---

### Risk 19: Governance Failure Due to Absent Policy Approval Process

**Control 1: Policy Approval Governance Control**
Effectiveness: Absent
Justification: No formal policy approval timeline or escalation process 
exists. This is both the risk being assessed and the control needed 
to address it. The complete absence of this control means the risk 
cannot be mitigated by any existing governance mechanism.

**Control 2: Policy Review and Management Control**
Effectiveness: Low
Justification: A policy review cycle exists in principle and provides 
some minimal governance oversight but does not include a formal approval 
timeline or escalation process to ensure drafted policies move through 
to operational status within a defined timeframe.

**Control 3: Remediation Tracking Control**
Effectiveness: Ineffective
Justification: The remediation tracker addresses open CBN examination 
findings but does not track or escalate stalled policy approval 
processes.

**Overall Control Effectiveness: Low to Absent**
The primary control needed to address this risk is completely absent. 
Supporting controls provide minimal or no protection against governance 
failure arising from a non-functional policy approval process.

---

## Stage 6 Summary

| Overall Control Effectiveness | Number of Risks | Percentage |
|---|---|---|
| High | 0 | 0% |
| Moderate | 0 | 0% |
| Low | 10 | 53% |
| Ineffective to Absent | 9 | 47% |
| **Total** | **19** | **100%** |

No risk across any of Paraclete's four scope areas has controls 
rated as high or moderate effectiveness. Ten risks have controls rated 
as low effectiveness, meaning existing controls provide only minimal 
protection. Nine risks have controls rated as ineffective to absent, 
meaning existing controls provide no meaningful protection at all.

This control effectiveness profile directly reflects the Stage 3 
finding that zero controls across all four scope areas were rated as 
strong. The implication for Stage 7 is significant: with no controls 
providing high or moderate effectiveness across any of the nineteen 
identified risks, residual risk scores will remain very close to 
inherent risk scores for most risks.
