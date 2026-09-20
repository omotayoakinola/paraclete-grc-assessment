# Paraclete
## Stage 5: Inherent Risk Assessment
**Confidential | Internal Use Only**

## Purpose

This document rates the inherent risk of each of the nineteen risks 
identified in Stage 4. Inherent risk represents the raw risk level 
that exists purely because of the threat and vulnerability, before 
any controls are considered. Every risk is rated across two dimensions: 
likelihood and impact, each scored on a scale of one to five. The 
inherent risk score is calculated by multiplying likelihood by impact 
and mapped to a risk level of low, medium, high, or critical.

## Why Inherent Risk Is Calculated Before Controls

Inherent risk must be calculated before controls are considered because 
it provides an honest baseline of how dangerous each risk actually is 
in its own right. Skipping straight to residual risk creates false 
assurance. If controls are weak or absent, factoring them into the 
risk rating produces a number that looks lower than the actual danger. 
The inherent risk baseline prevents this by forcing an honest assessment 
of raw danger before any mitigating factors are introduced.

## Rating Scales

### Likelihood
| Score | Label | Definition |
|---|---|---|
| 1 | Rare | Very unlikely to occur |
| 2 | Unlikely | Could occur but not expected |
| 3 | Possible | Might occur at some point |
| 4 | Likely | Vulnerability confirmed and conditions for exploitation exist |
| 5 | Almost Certain | Already confirmed as occurring or virtually guaranteed |

### Impact
| Score | Label | Definition |
|---|---|---|
| 1 | Negligible | Minimal consequences easily managed |
| 2 | Minor | Some consequences but limited damage |
| 3 | Moderate | Significant consequences requiring management attention |
| 4 | Major | Serious consequences affecting operations or reputation |
| 5 | Severe | Catastrophic consequences threatening organisational survival or licence |

### Risk Level
| Score | Level |
|---|---|
| 1 to 4 | Low |
| 5 to 9 | Medium |
| 10 to 14 | High |
| 15 to 25 | Critical |

**Formula:** Likelihood x Impact = Inherent Risk Score

---

## Area 1: Identity and Access Management

### Risk 1: Unauthorised Access by Former Staff
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by interview findings. HR notification 
to IT takes three to five business days against a documented 24-hour 
requirement and no confirmation loop exists to verify deactivation. 
Former staff accounts are already confirmed as remaining active after 
exit. This condition is currently occurring at Verdant Pay.

**Impact:** 5 — Severe
**Justification:** Unauthorized access by a former staff member could 
result in customer financial data exfiltration, internal HR record 
exposure, compliance documentation manipulation, regulatory fines under 
NDPA 2023 and CBN Cybersecurity Framework, potential PSSP licence 
revocation, and material damage to the Series B fundraising round.

**Inherent Risk Score:** 25
**Risk Level:** Critical

---

### Risk 2: Authentication Bypass Through Weak Conditional Access
**Likelihood:** 4 — Likely
**Justification:** Conditional access policies are confirmed as not 
fully operational by the CISO, creating a realistic attack surface for 
Legacy Authentication Abuse and AiTM attacks targeting a fintech 
processing NGN 2.1 billion monthly. However no confirmed evidence 
exists of active exploitation through these specific techniques at 
this time.

**Impact:** 5 — Severe
**Justification:** A successful authentication bypass would grant an 
external attacker persistent unauthorized access to Paraclete's M365 
environment, enabling customer financial data access, compliance record 
manipulation, PCI-DSS non-compliance, adverse CBN examination findings, 
and significant reputational and financial consequences ahead of the 
Series B process.

**Inherent Risk Score:** 20
**Risk Level:** Critical

---

### Risk 3: Privilege Escalation Through Ungoverned Privileged Access
**Likelihood:** 4 — Likely
**Justification:** The complete absence of a formal privileged access 
management process is confirmed by the CISO, meaning conditions for 
privilege escalation exist continuously for all current staff and 
contractors with any level of system access. However no confirmed 
evidence exists of active exploitation at this time.

**Impact:** 5 — Severe
**Justification:** Successful privilege escalation could enable an 
insider to access Azure cloud infrastructure, M365 administrator 
accounts, and customer financial data beyond their legitimate scope, 
resulting in significant data breach, regulatory sanction under NDPA 
2023 and CBN Cybersecurity Framework, and potential licence 
implications for Paraclete as a PSSP.

**Inherent Risk Score:** 20
**Risk Level:** Critical

---

### Risk 4: Undetected Permission Creep Through Infrequent Access Reviews
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by Cloud Administrator interview. The last 
formal access review was conducted eight months ago against a quarterly 
requirement and was neither formally documented nor signed off. 
Permission creep is therefore already occurring at Paraclete as 
permissions accumulate without review or correction.

**Impact:** 4 — Major
**Justification:** Unreviewed and accumulated permissions amplify the 
impact of any security incident by giving attackers broader access than 
intended. However the harm is primarily an enabler of other risks rather 
than a standalone catastrophic event, making major rather than severe 
the appropriate impact rating.

**Inherent Risk Score:** 20
**Risk Level:** Critical

---

## Area 2: Customer Data Handling

### Risk 5: Unprotected Customer Data Due to Absent Data Classification
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by DPO interview. No approved data 
classification policy exists in operational form. Staff are confirmed 
as treating all data the same regardless of sensitivity. This condition 
is currently occurring at Paraclete and affects every interaction 
with customer financial data daily.

**Impact:** 5 — Severe
**Justification:** Without data classification, sensitive customer 
financial data is unprotected proportionate to its sensitivity, 
creating conditions for a data breach that would trigger NDPA 2023 
Section 24 sanctions, adverse CBN examination findings, PCI-DSS 
non-compliance, and reputational damage that could materially impact 
the Series B fundraising round.

**Inherent Risk Score:** 25
**Risk Level:** Critical

---

### Risk 6: Customer Data Exposure Through Policy Violations
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by Senior Product Operations Manager 
interview. Active violations are already occurring including personal 
WhatsApp groups being used for customer data communications and personal 
OneDrive folders being used for customer dispute records. This is not 
a future risk, it is a current confirmed condition.

**Impact:** 5 — Severe
**Justification:** Customer personal and financial data being shared 
through unapproved channels outside IT visibility creates direct NDPA 
2023 exposure, significant likelihood of unauthorized data access or 
accidental disclosure, and permanent data loss risk through unprotected 
personal devices that Paraclete cannot monitor, recover, or audit.

**Inherent Risk Score:** 25
**Risk Level:** Critical

---

### Risk 7: Unauthorized Access to Customer Data Through Expanded Permissions
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by Cloud Administrator interview and Q1 
2026 compliance review. SharePoint permissions have already expanded 
beyond originally intended boundaries without detection and the last 
formal permission review was eight months ago. This condition is 
currently confirmed as existing at Paraclete.

**Impact:** 5 — Severe
**Justification:** Expanded and unverified permissions enable both 
internal actors and external attackers to access customer financial 
data beyond legitimate scope, resulting in unauthorized data access, 
regulatory sanction under NDPA 2023 and CBN Cybersecurity Framework, 
loss of customer trust, and adverse findings during the Q4 2026 CBN 
examination.

**Inherent Risk Score:** 25
**Risk Level:** Critical

---

### Risk 8: Customer Data Interception Through Inadequate Encryption
**Likelihood:** 3 — Possible
**Justification:** No documented encryption standard exists within 
the absent data classification policy. However active exploitation of 
inadequate encryption through data interception or ransomware targeting 
Paraclete's Azure environment specifically has not been confirmed. 
The likelihood is possible rather than likely because exploitation 
requires deliberate external targeting of a specific technical weakness 
not yet technically verified.

**Impact:** 5 — Severe
**Justification:** Customer financial data intercepted or exposed 
through inadequate encryption would create significant PCI-DSS 
non-compliance exposure, NDPA 2023 sanctions, potential financial 
liability to affected customers, and reputational consequences that 
would materially affect both the Series B process and the CBN 
examination outcome.

**Inherent Risk Score:** 15
**Risk Level:** Critical

---

### Risk 9: Regulatory Sanction Due to Absent Breach Notification Procedure
**Likelihood:** 4 — Likely
**Justification:** No operational breach notification procedure exists, 
confirmed by inference from DPO interview and the overall governance 
posture assessment. Given the confirmed existence of multiple high 
severity risks across all four scope areas, the probability of a breach 
occurring that would require notification is high. The absence of a 
notification procedure means regulatory sanction following any breach 
is highly likely.

**Impact:** 5 — Severe
**Justification:** Failure to meet the NDPA 2023 72-hour breach 
notification requirement would convert a manageable security incident 
into a compounded regulatory violation with potential for substantial 
fines, enforcement action, and licence review by CBN, in addition to 
the reputational consequences of a delayed and uncoordinated breach 
response.

**Inherent Risk Score:** 20
**Risk Level:** Critical

---

## Area 3: Cybersecurity Awareness and Human Risk

### Risk 10: Staff Susceptibility to Phishing and Social Engineering
**Likelihood:** 4 — Likely
**Justification:** Annual training exists but knowledge retention is 
unverified. At a fintech processing NGN 2.1 billion monthly, staff are 
attractive targets for external phishing campaigns. The combination of 
unverified training effectiveness and high target value makes phishing 
exploitation likely, though no confirmed incident has been reported.

**Impact:** 5 — Severe
**Justification:** A successful phishing attack could result in 
credential compromise, unauthorized system access, fraudulent 
transactions, and customer data breaches, with severe regulatory, 
financial, and reputational consequences for Paraclete given its 
transaction volumes and regulatory obligations.

**Inherent Risk Score:** 20
**Risk Level:** Critical

---

### Risk 11: Unverified Security Behavior Due to Absent Knowledge Assessment
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by HR interview. No formal knowledge 
assessment exists at the end of training. This condition is currently 
confirmed as existing at Paraclete, meaning security behavior across 
all staff is unverified right now.

**Impact:** 3 — Moderate
**Justification:** The absence of knowledge assessment is primarily a 
governance and compliance gap rather than a direct operational threat. 
Its impact is moderate because it weakens Paraclete's ability to 
demonstrate training effectiveness to a CBN examiner but does not 
directly cause a data breach or financial loss on its own.

**Inherent Risk Score:** 15
**Risk Level:** Critical

---

### Risk 12: Undetected Phishing Susceptibility Across Staff
**Likelihood:** 4 — Likely
**Justification:** No phishing simulation program exists, confirmed 
across all seven stakeholder interviews. Staff susceptibility has never 
been tested or measured. Given Paraclete's transaction volumes and 
the confirmed absence of knowledge retention assessment, phishing 
susceptibility is likely across at least a portion of the staff 
population.

**Impact:** 5 — Severe
**Justification:** Undetected phishing susceptibility at a fintech 
processing NGN 2.1 billion monthly creates significant financial fraud 
risk, potential large scale customer data exposure, and regulatory 
consequences if a successful phishing attack results in a breach that 
Paraclete cannot demonstrate it took reasonable preventive measures 
against.

**Inherent Risk Score:** 20
**Risk Level:** Critical

---

### Risk 13: Fraudulent Access Through Undetected Credential Sharing
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by Senior Product Operations Manager 
interview. Credential sharing during peak processing periods is an 
established practice at Paraclete. This is not a future risk, it 
is a current confirmed condition occurring regularly.

**Impact:** 5 — Severe
**Justification:** Shared credentials eliminate individual 
accountability for system access during peak periods. A malicious 
actor exploiting shared credentials could execute fraudulent 
transactions, access customer financial data, or manipulate 
transaction records, with Paraclete unable to attribute actions 
to a specific individual during any subsequent investigation or 
regulatory inquiry.

**Inherent Risk Score:** 25
**Risk Level:** Critical

---

### Risk 14: Security Behavior Degradation Between Training Cycles
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by HR interview and Senior Product 
Operations Manager interview. Annual training with no reinforcement 
between cycles is confirmed. Security behavior degradation between 
cycles is therefore a current confirmed condition evidenced by the 
policy violations already identified during interviews.

**Impact:** 3 — Moderate
**Justification:** Security behavior degradation is a gradual process 
that increases susceptibility over time rather than causing immediate 
catastrophic harm. Its impact is moderate because it is an enabling 
condition for other risks rather than a standalone catastrophic event.

**Inherent Risk Score:** 15
**Risk Level:** Critical

---

### Risk 15: Normalised Policy Violations Through Absent Management Accountability
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by Senior Product Operations Manager 
interview. Policy violations including WhatsApp use for customer data 
communications and credential sharing during peak periods are already 
normalised and ongoing without management challenge or correction.

**Impact:** 4 — Major
**Justification:** Normalised policy violations create a security 
culture gap that progressively increases the likelihood of data 
breaches and regulatory violations. The impact is major rather than 
severe because the harm is cumulative and enabling rather than 
immediately catastrophic, though it significantly weakens Paraclete's 
compliance posture ahead of the Q4 2026 CBN examination.

**Inherent Risk Score:** 20
**Risk Level:** Critical

---

## Area 4: Governance and Policy Posture

### Risk 16: Regulatory Non-Compliance Due to Outdated or Absent Policies
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by CCO interview. Two key policies, data 
classification and third-party risk management, are either absent or 
inactive. This condition is currently confirmed as existing at Paraclete
and directly affects the organization's regulatory standing right now.

**Impact:** 4 — Major
**Justification:** Outdated or absent policies leave Paraclete 
operating without adequate governance guardrails, increasing the 
likelihood of adverse CBN examination findings in Q4 2026. The impact 
is major rather than severe because the immediate consequence is 
regulatory attention and examination findings rather than immediate 
licence revocation, though escalation remains a realistic outcome if 
findings are not addressed.

**Inherent Risk Score:** 20
**Risk Level:** Critical

---

### Risk 17: Escalated Regulatory Findings Due to Overdue Remediation
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by CCO interview. Two of three open CBN 
examination findings have already exceeded their target remediation 
deadlines. This condition is currently confirmed and worsening as the 
Q4 2026 examination approaches.

**Impact:** 4 — Major
**Justification:** Open examination findings exceeding remediation 
deadlines signal governance weakness to CBN examiners, significantly 
increasing the risk of escalated findings and formal enforcement action. 
The impact is major rather than severe because formal enforcement action 
and licence review remain probable rather than certain outcomes at 
this stage.

**Inherent Risk Score:** 20
**Risk Level:** Critical

---

### Risk 18: Supply Chain Attack Through Unassessed Third Party Vendors
**Likelihood:** 4 — Likely
**Justification:** The Third Party Risk Management Policy is confirmed 
as absent in operational form by the CCO interview. Several vendors 
have never been assessed including an unapproved external document 
conversion tool already confirmed as processing customer reference data. 
The conditions for supply chain exploitation exist but active 
exploitation has not been confirmed.

**Impact:** 5 — Severe
**Justification:** An unassessed vendor introducing a supply chain 
vulnerability could bypass all internal security controls, resulting 
in a large scale data breach, NDPA 2023 violation, and CBN examination 
finding that Paraclete cannot defend against because no vendor risk 
assessment was ever conducted, while simultaneously exposing the 
organization to liability for customer data processed without a data 
processing agreement.

**Inherent Risk Score:** 20
**Risk Level:** Critical

---

### Risk 19: Governance Failure Due to Absent Policy Approval Process
**Likelihood:** 5 — Almost Certain
**Justification:** Confirmed by DPO interview. The draft data 
classification framework has sat unapproved for six months with no 
escalation or resolution. The policy approval process is confirmed 
as non-functional at Paraclete right now.

**Impact:** 4 — Major
**Justification:** The absence of a functioning policy approval process 
means critical governance gaps remain unresolved indefinitely. The 
impact is major rather than severe because the immediate consequence 
is compounding governance weakness and regulatory exposure rather than 
immediate catastrophic operational failure, though the cascading effect 
on other risks makes this a high priority remediation item.

**Inherent Risk Score:** 20
**Risk Level:** Critical

---

## Stage 5 Summary

| Risk Level | Number of Risks | Percentage |
|---|---|---|
| Critical (15-25) | 19 | 100% |
| High (10-14) | 0 | 0% |
| Medium (5-9) | 0 | 0% |
| Low (1-4) | 0 | 0% |
| **Total** | **19** | **100%** |

Every one of Paraclete's nineteen identified risks has been rated 
as critical at the inherent risk level. This exceptional finding 
reflects the severity and systemic nature of the control gaps 
identified across all four scope areas in Stage 3.

The concentration of critical risks is explained by three factors. 
First, ten of the nineteen risks carry a likelihood rating of five, 
meaning the conditions driving those risks are already confirmed as 
occurring at Paraclete right now rather than being future 
possibilities. Second, fifteen of the nineteen risks carry an impact 
rating of five, reflecting the severe regulatory, financial, and 
reputational consequences that any significant security incident would 
have for a PSSP processing NGN 2.1 billion monthly with a CBN 
examination in Q4 2026 and a planned Series B fundraising round. 
Third, the complete absence of strong controls across all four scope 
areas means there are no effective mitigating factors to reduce 
inherent risk ratings below critical for any identified risk.

All nineteen critical risks will be carried forward into Stage 6 
where existing controls will be formally assessed, and Stage 7 where 
residual risk will be calculated after accounting for the actual 
protective value of existing controls.
