# Paraclete
## Stage 7: Residual Risk Assessment
**Confidential | Internal Use Only**

## Purpose

This document calculates the residual risk for each of the nineteen 
identified risks at Paraclete after accounting for the protective 
value of existing controls assessed in Stage 6. Residual risk 
represents the danger that remains after existing controls are applied. 
It is calculated by adjusting the inherent risk score from Stage 5 
based on the overall control effectiveness rating from Stage 6.

## Residual Risk Calculation Methodology

| Control Effectiveness | Reduction Applied |
|---|---|
| High | Inherent risk score reduced by 75% |
| Moderate | Inherent risk score reduced by 50% |
| Low | Inherent risk score reduced by 25% |
| Ineffective to Absent | Inherent risk score reduced by 0% |

**Formula:** Residual Risk = Inherent Risk × (1 − Control 
Effectiveness Reduction Percentage)

**Rounding rule:** Where the calculated residual risk produces 
a decimal, the score is rounded to the nearest whole number 
for risk level classification.

**Note on reduction percentages:** The reduction percentages 
applied in this assessment represent Paraclete's defined 
risk reduction assumptions for translating overall control 
effectiveness into residual risk scores. They are not 
presented as universally established facts but as the 
agreed methodology for this engagement.

## Residual Risk Level

| Score | Level |
|---|---|
| 1 to 4 | Low |
| 5 to 9 | Medium |
| 10 to 14 | High |
| 15 to 25 | Critical |

---

## Area 1: Identity and Access Management

### Risk 1: Unauthorised Access by Former Staff
**Inherent Risk Score:** 25
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 25 × (1 − 0.25) = 18.75, rounded to 19
**Residual Risk Score:** 19
**Residual Risk Level:** Critical
**Justification:** The offboarding access deprovisioning process 
provides minimal protection but consistently fails to operate within 
its documented 24-hour requirement. Remaining controls are ineffective 
or absent. The residual risk remains critical reflecting the confirmed 
ongoing condition of former staff accounts remaining active after exit, 
evidenced by the HR interview finding that notification to IT takes 
three to five business days against a documented 24-hour requirement.

---

### Risk 2: Authentication Bypass Through Weak Conditional Access
**Inherent Risk Score:** 20
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 20 × (1 − 0.25) = 15
**Residual Risk Score:** 15
**Residual Risk Level:** Critical
**Justification:** Conditional access policies exist in documentation 
but are not confirmed as operational, providing only minimal theoretical 
protection against Legacy Authentication Abuse and AiTM attacks. The 
residual risk remains critical reflecting the unconfirmed operational 
status of the primary protective control.

---

### Risk 3: Privilege Escalation Through Ungoverned Privileged Access
**Inherent Risk Score:** 20
**Overall Control Effectiveness:** Ineffective
**Residual Risk Calculation:** 20 × (1 − 0) = 20
**Residual Risk Score:** 20
**Residual Risk Level:** Critical
**Justification:** No meaningful controls exist to address privilege 
escalation at Paraclete. Privileged access management is completely 
absent and remaining controls are ineffective against this specific 
risk. The residual risk equals the inherent risk reflecting zero 
protective value from existing controls.

---

### Risk 4: Undetected Permission Creep Through Infrequent Access Reviews
**Inherent Risk Score:** 20
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 20 × (1 − 0.25) = 15
**Residual Risk Score:** 15
**Residual Risk Level:** Critical
**Justification:** Periodic access reviews occur but at insufficient 
frequency and without formal documentation or sign-off. The minimal 
protection they provide reduces the residual risk slightly but the 
score remains critical reflecting the confirmed eight-month gap between 
reviews against a quarterly requirement.

---

## Area 2: Customer Data Handling

### Risk 5: Unprotected Customer Data Due to Absent Data Classification
**Inherent Risk Score:** 25
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 25 × (1 − 0.25) = 18.75, rounded to 19
**Residual Risk Score:** 19
**Residual Risk Level:** Critical
**Justification:** Minimal protection is provided through access 
restrictions and some encryption capability within Azure infrastructure. 
However the foundational control, data classification policy, is 
completely absent, meaning remaining controls cannot be systematically 
applied proportionate to data sensitivity. The overall control 
effectiveness is rated Low reflecting the minimal protection provided 
by access restriction and encryption controls, despite the absence of 
the foundational data classification policy. Residual risk remains 
critical.

---

### Risk 6: Customer Data Exposure Through Policy Violations
**Inherent Risk Score:** 25
**Overall Control Effectiveness:** Ineffective
**Residual Risk Calculation:** 25 × (1 − 0) = 25
**Residual Risk Score:** 25
**Residual Risk Level:** Critical
**Justification:** The Acceptable Use Policy is completely unenforced 
and active violations are already confirmed through the Senior Product 
Operations Manager interview, including personal WhatsApp groups being 
used for customer data communications and personal OneDrive folders 
being used for customer dispute records. Management reinforcement and 
data classification controls are absent. Existing controls provide zero 
protective value against this risk. Residual risk equals inherent risk.

---

### Risk 7: Unauthorized Access to Customer Data Through Expanded Permissions
**Inherent Risk Score:** 25
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 25 × (1 − 0.25) = 18.75, rounded to 19
**Residual Risk Score:** 19
**Residual Risk Level:** Critical
**Justification:** Access restrictions provide minimal protection but 
have already proven insufficient to maintain intended permission 
boundaries. Periodic access reviews are too infrequent to detect 
unauthorized permission expansion in a timely manner. Residual risk 
remains critical.

---

### Risk 8: Customer Data Interception Through Inadequate Encryption
**Inherent Risk Score:** 15
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 15 × (1 − 0.25) = 11.25, rounded to 11
**Residual Risk Score:** 11
**Residual Risk Level:** High
**Justification:** Some encryption capability exists within Azure 
infrastructure providing minimal protection. The absence of a 
documented encryption standard means encryption cannot be 
systematically applied across all storage services. This is one of 
three risks that reduces from critical to high at the residual level, 
alongside Risks 11 and 14, reflecting some existing encryption 
capability within the Azure environment.

---

### Risk 9: Regulatory Sanction Due to Absent Breach Notification Procedure
**Inherent Risk Score:** 20
**Overall Control Effectiveness:** Ineffective
**Residual Risk Calculation:** 20 × (1 − 0) = 20
**Residual Risk Score:** 20
**Residual Risk Level:** Critical
**Justification:** No controls exist to address this risk. Both the 
breach notification procedure and the data classification policy that 
would inform it are completely absent. Residual risk equals inherent 
risk reflecting zero protective value from existing controls.

---

## Area 3: Cybersecurity Awareness and Human Risk

### Risk 10: Staff Susceptibility to Phishing and Social Engineering
**Inherent Risk Score:** 20
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 20 × (1 − 0.25) = 15
**Residual Risk Score:** 15
**Residual Risk Level:** Critical
**Justification:** Annual training provides minimal protection against 
phishing and social engineering but knowledge retention is unverified 
and training occurs only once per year without reinforcement. Three 
supporting controls are completely absent. Residual risk remains 
critical.

---

### Risk 11: Unverified Security Behavior Due to Absent Knowledge Assessment
**Inherent Risk Score:** 15
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 15 × (1 − 0.25) = 11.25, rounded to 11
**Residual Risk Score:** 11
**Residual Risk Level:** High
**Justification:** Annual training provides some minimal foundation 
for security behavior but without knowledge assessment its 
effectiveness cannot be verified or demonstrated. The primary control 
needed to address this risk is completely absent. The overall control 
effectiveness is rated Low reflecting the minimal foundation provided 
by the annual training program. Residual risk reduces from critical 
to high, making this one of three risks at the high residual level 
alongside Risks 8 and 14.

---

### Risk 12: Undetected Phishing Susceptibility Across Staff
**Inherent Risk Score:** 20
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 20 × (1 − 0.25) = 15
**Residual Risk Score:** 15
**Residual Risk Level:** Critical
**Justification:** Annual training provides minimal theoretical 
protection against phishing susceptibility but without simulation 
exercises actual staff susceptibility remains unmeasured and 
unaddressed. The primary control, phishing simulation, is completely 
absent. The overall control effectiveness is rated Low reflecting the 
minimal protection provided by annual training. Residual risk remains 
critical.

---

### Risk 13: Fraudulent Access Through Undetected Credential Sharing
**Inherent Risk Score:** 25
**Overall Control Effectiveness:** Ineffective
**Residual Risk Calculation:** 25 × (1 − 0) = 25
**Residual Risk Score:** 25
**Residual Risk Level:** Critical
**Justification:** Audit log review is absent meaning credential 
sharing goes undetected. The Acceptable Use Policy is unenforced and 
management reinforcement is absent. Active credential sharing is 
already confirmed as an established practice through the Senior Product 
Operations Manager interview. Existing controls provide zero protective 
value. Residual risk equals inherent risk.

---

### Risk 14: Security Behavior Degradation Between Training Cycles
**Inherent Risk Score:** 15
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 15 × (1 − 0.25) = 11.25, rounded to 11
**Residual Risk Score:** 11
**Residual Risk Level:** High
**Justification:** Annual training provides minimal foundation but 
behavioral degradation between cycles is already confirmed by the 
policy violations identified during stakeholder interviews. Continuous 
awareness communications and management reinforcement are both absent. 
The overall control effectiveness is rated Low reflecting the minimal 
foundation provided by annual training. Residual risk reduces from 
critical to high, making this one of three risks at the high residual 
level alongside Risks 8 and 11.

---

### Risk 15: Normalised Policy Violations Through Absent Management Accountability
**Inherent Risk Score:** 20
**Overall Control Effectiveness:** Ineffective
**Residual Risk Calculation:** 20 × (1 − 0) = 20
**Residual Risk Score:** 20
**Residual Risk Level:** Critical
**Justification:** Management accountability is completely absent and 
the Acceptable Use Policy is unenforced. Active policy violations are 
already normalised across the operations team, confirmed through the 
Senior Product Operations Manager interview. Existing controls provide 
zero protective value against this risk. Residual risk equals inherent 
risk.

---

## Area 4: Governance and Policy Posture

### Risk 16: Regulatory Non-Compliance Due to Outdated or Absent Policies
**Inherent Risk Score:** 20
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 20 × (1 − 0.25) = 15
**Residual Risk Score:** 15
**Residual Risk Level:** Critical
**Justification:** The policy review cycle provides minimal governance 
oversight but is operating far below the standard needed to maintain 
regulatory compliance. The policy approval governance control is 
absent. Residual risk remains critical reflecting the confirmed absence 
of two key policies against documented governance framework requirements.

---

### Risk 17: Escalated Regulatory Findings Due to Overdue Remediation
**Inherent Risk Score:** 20
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 20 × (1 − 0.25) = 15
**Residual Risk Score:** 15
**Residual Risk Level:** Critical
**Justification:** The remediation tracker provides minimal visibility 
into open CBN examination findings but is not driving timely 
remediation action. Two of three open findings have already exceeded 
their target remediation deadlines. Residual risk remains critical 
given the confirmed overdue status of open regulatory commitments.

---

### Risk 18: Supply Chain Attack Through Unassessed Third Party Vendors
**Inherent Risk Score:** 20
**Overall Control Effectiveness:** Ineffective
**Residual Risk Calculation:** 20 × (1 − 0) = 20
**Residual Risk Score:** 20
**Residual Risk Level:** Critical
**Justification:** Third party risk management is completely absent 
in operational form. The Acceptable Use Policy is unenforced against 
unapproved tool use. An unapproved vendor is already confirmed as 
processing customer reference data without assessment or data 
processing agreement, evidenced through the Senior Product Operations 
Manager interview. Existing controls provide zero protective value. 
Residual risk equals inherent risk.

---

### Risk 19: Governance Failure Due to Absent Policy Approval Process
**Inherent Risk Score:** 20
**Overall Control Effectiveness:** Low
**Residual Risk Calculation:** 20 × (1 − 0.25) = 15
**Residual Risk Score:** 15
**Residual Risk Level:** Critical
**Justification:** The policy review cycle provides minimal governance 
oversight but does not include a formal approval timeline or escalation 
process. The primary control needed to address this risk is completely 
absent. The overall control effectiveness is rated Low reflecting the 
minimal protection provided by the policy review cycle. Residual risk 
remains critical reflecting the confirmed six-month stall of the draft 
data classification framework in the approval process.

---

## Stage 7 Summary

| Residual Risk Level | Number of Risks | Percentage |
|---|---|---|
| Critical (15-25) | 16 | 84% |
| High (10-14) | 3 | 16% |
| Medium (5-9) | 0 | 0% |
| Low (1-4) | 0 | 0% |
| **Total** | **19** | **100%** |

Sixteen of nineteen risks remain at critical residual risk level after 
accounting for the protective value of existing controls. Three risks 
have reduced from critical to high at the residual level: Risk 8, 
Customer Data Interception Through Inadequate Encryption; Risk 11, 
Unverified Security Behavior Due to Absent Knowledge Assessment; and 
Risk 14, Security Behavior Degradation Between Training Cycles. This 
reduction reflects the minimal protection provided by annual 
cybersecurity training and some encryption capability within Azure 
infrastructure. No risks have reduced to medium or low, confirming 
that existing controls provide insufficient protection across all four 
scope areas.

The maximum risk reduction applied under the Stage 7 methodology is 
25%, because no overall control effectiveness rating was assessed as 
High or Moderate. Nine risks show zero reduction between inherent and 
residual risk because their controls were rated as Ineffective, 
reflecting the complete absence of meaningful protective controls 
against those specific risks.

This residual risk profile reflects Paraclete's current risk 
exposure before remediation. It is presented honestly to establish 
the baseline from which remediation must start and is not presented 
as an acceptable risk position. The target residual risk after full 
implementation of all treatment plans in Stage 8 represents the 
intended risk position against which Paraclete's risk appetite 
should be measured. No risk in this register will be considered within 
acceptable boundaries until it reaches its target level defined in 
Stage 8.
