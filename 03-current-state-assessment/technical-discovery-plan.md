# Verdant Pay Limited
## Stage 3, Part 3: Technical Discovery Plan
**Confidential | Internal Use Only**

## Purpose

Technical discovery is the verification layer of the assessment. 
Its purpose is to confirm or contradict what stakeholders said and 
what documentation claims, by examining what is actually configured 
and operating in Verdant Pay's technical environment. Every technical 
check in this plan traces back to a specific interview finding, 
documentation gap, or flagged incident. Nothing is checked randomly.

## The Golden Rule of Technical Discovery

Every finding must have three components to be defensible:

- **What was checked:** The specific system, report, or log reviewed
- **What was found:** The specific evidence or variance identified
- **Why it matters:** Which scope area, framework requirement, or 
  flagged incident it connects to

A finding without all three components is not a finding. It is an 
observation. Observations do not belong in a risk register. Findings do.

## Note on Scope

Verdant Pay is a cloud-native organization. Physical infrastructure 
and on-premises hardware are explicitly out of scope. Technical 
discovery is therefore entirely cloud-focused, covering configurations, 
permissions, logs, and settings within Azure and M365.

---

## Area 1: M365 and Azure Access Control Review

**What drives it:** Former staff accounts remaining active after 
offboarding, flagged in Q1 2026 and confirmed as a process gap between 
HR and IT in stakeholder interviews.

**What is being checked:** The full M365 user list cross-referenced 
against the HR active staff list. For each account, three specific 
data points are checked:

- **Account status:** Whether the account is enabled or disabled. 
  An active account belonging to someone who left should have been 
  disabled on exit.
- **Last sign-in date:** Whether any account shows activity after 
  the associated staff member's exit date.
- **License assignment:** Whether former staff accounts have had 
  their M365 licenses removed as required on offboarding.

SharePoint permission structures will also be reviewed by comparing 
current permission assignments against the original design documentation, 
with any expansion beyond originally intended access boundaries flagged 
as a finding.

**What a finding looks like:** An enabled, licensed, or recently active 
account belonging to someone no longer on the HR active staff list. A 
SharePoint folder showing more users with access than the original 
design document specified.

---

## Area 2: Audit Log Review

**What drives it:** Two separate interview findings. The IT Head 
confirmed that account revocation is sometimes delayed. The Senior 
Product Operations Manager disclosed that staff share credentials 
during peak processing periods.

**What is being checked:** M365 unified audit log and Azure Active 
Directory sign-in logs for two specific categories:

**Former employee account activity:** Sign-in logs reviewed to 
identify any access activity occurring after an employee's confirmed 
exit date, establishing whether terminated accounts were used after 
offboarding and for how long.

**Credential sharing detection:** Sign-in logs and activity logs 
reviewed for indicators of multiple individuals operating under a 
single account identity, specifically:

- **Impossible travel:** The same account showing sign-in activity 
  from two geographically distant locations within an implausibly 
  short timeframe
- **Concurrent sessions:** The same account active simultaneously 
  from different IP addresses
- **Unusual activity volumes:** Patterns inconsistent with a single 
  user operating during normal business hours

**What a finding looks like:** Sign-in activity on a terminated account 
after the employee's exit date. The same account showing simultaneous 
active sessions from two different IP addresses. An account showing 
continuous transaction processing activity inconsistent with a single 
user's working pattern.

---

## Area 3: Configuration Baseline Assessment

**What drives it:** The Cloud Administrator's admission that the last 
formal configuration review was eight months ago against a quarterly 
requirement, and the CISO's acknowledgment that several controls 
documented as active are not operating effectively.

**What is being checked:** Three specific configuration areas in the 
M365 admin center and Azure portal, compared against the documented 
configuration baseline:

- **Conditional access policies:** Whether access restrictions are 
  configured as documented, including whether policies enforcing 
  location-based or device-based access controls are active and 
  functioning.
- **MFA enforcement settings:** Whether multi-factor authentication 
  is enabled and enforced for all user accounts, including privileged 
  accounts, consistent with both the documented baseline and CBN 
  Cybersecurity Framework requirements.
- **SharePoint external sharing settings:** Whether sharing 
  permissions are restricted to internally approved boundaries and 
  whether any external sharing configurations exist that were not 
  formally authorized.

**What a finding looks like:** MFA not enforced for one or more user 
accounts despite the baseline requiring universal enforcement. An 
external sharing setting in SharePoint configured more permissively 
than the baseline specifies. A conditional access policy documented 
as active that is in fact disabled or misconfigured.

---

## Area 4: Data Handling and Storage Verification

**What drives it:** The DPO's confirmation that no data classification 
policy exists in operational form, and the Senior Product Operations 
Manager's disclosure of customer data being stored in personal OneDrive 
folders and processed through an unapproved external document conversion 
tool.

**What is being checked:**

- **Azure storage service configurations:** Which specific Azure 
  storage services currently hold customer data, to establish a 
  complete picture of where sensitive data resides and whether any 
  storage locations exist outside officially sanctioned systems.
- **Encryption settings:** Whether data is encrypted at rest and 
  in transit across each identified storage service, in line with 
  PCI-DSS requirements and NDPA 2023 obligations.
- **Data flow verification:** Whether customer data moves outside 
  approved cloud systems into unapproved channels or third-party 
  tools, drawing directly on the findings from the Senior Product 
  Operations Manager interview.

**What a finding looks like:** Customer financial data stored in an 
Azure storage container without encryption at rest enabled. Evidence 
of customer data existing in personal OneDrive accounts outside 
IT-governed storage. A storage service holding customer data that 
does not appear in any official data inventory or classification 
register.

---

## How to Approach Technical Discovery: The Four-Step Formula

For every technical discovery area, the following four steps apply:

**Step 1: Anchor to a finding or gap.**
Before running any technical check, identify the specific interview 
finding, documentation gap, or flagged incident driving it. Never 
check something without knowing why.

**Step 2: Identify the data source.**
Know where to look before starting. M365 admin center for access 
control reviews. M365 unified audit log and Azure AD sign-in logs 
for audit log reviews. M365 admin center security settings and Azure 
portal for configuration baseline assessment. Azure storage account 
configurations for data handling verification.

**Step 3: Define what a finding looks like before reviewing.**
Set the expectation before opening the data. This prevents seeing 
what you want to see rather than what is actually there.

**Step 4: Document what you find, including what you do not find.**
A clean result is also a finding. If a review confirms controls are 
operating as intended, that is evidence of control effectiveness and 
should be recorded as such.
