# Paraclete
## Stage 8: Risk Register with Treatment Plans and Recommendations
**Confidential | Internal Use Only**

## Purpose

This risk register consolidates all findings from Stages 4 through 7 
into a single actionable governance document. For each of the nineteen 
identified risks it presents the risk description, inherent risk rating, 
existing controls and their effectiveness, residual risk rating, risk 
owner, treatment plan, and target residual risk after treatment. This 
document is the primary governance artifact supporting Paraclete's 
remediation planning ahead of the Q4 2026 CBN examination and the 
planned Series B fundraising round.

## Risk Register Key

| Field | Definition |
|---|---|
| Likelihood and Impact | Rated 1 to 5 |
| Inherent and Residual Risk Score | Likelihood multiplied by Impact |
| Risk Level | 1 to 4 Low, 5 to 9 Medium, 10 to 14 High, 15 to 25 Critical |
| Control Effectiveness | High, Moderate, Low, Ineffective, Absent |
| Accountable Owner | Single person ultimately answerable for this risk per RACI principles |
| Responsible Party | Person executing specific treatment actions within their function |
| Treatment Priority | Immediate within 30 days, Short term within 90 days, Medium term within 180 days |

## Note on Risk Ownership

Risk ownership in this register follows RACI principles. One person 
is Accountable, meaning ultimately answerable to the board if the risk 
materializes. Others may be Responsible for executing specific treatment 
actions within their function. The question used to determine the 
Accountable owner for each risk was: who would the board hold ultimately 
answerable if this risk materialized?

## Note on Residual Risk and Risk Appetite

The residual risk scores presented in this register reflect Paraclete's 
current risk exposure with existing controls in place. They are 
presented honestly to establish the baseline from which remediation 
must start and are not presented as an acceptable risk position. The 
target residual risk after treatment represents the intended risk 
position after all treatment plans are fully implemented. This is the 
level against which Paraclete's risk appetite should be measured. 
No risk in this register will be considered within acceptable 
boundaries until it reaches its defined target level.

---

## RISK 1: Unauthorised Access by Former Staff

**Scope Area:** Identity and Access Management
**Accountable Owner:** Head of People Operations
**Responsible Party:** Head of IT Infrastructure
**Threat:** Human internal. Disgruntled former staff member retaining 
active M365 access after exit.
**Vulnerability:** HR notification to IT takes three to five business 
days against a documented 24-hour requirement. No confirmation loop 
exists between HR and IT to verify that account deactivation was 
completed following notification.
**Asset at Risk:** M365 environment, customer financial data, internal 
HR records, compliance documentation.
**Inherent Risk:** Likelihood 5, Impact 5, Score 25, Level Critical
**Existing Controls:** Offboarding access deprovisioning process, Low 
effectiveness. Conditional access policies, Ineffective. Privileged 
access management, Absent. Periodic access reviews, Ineffective.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 19, Level Critical

**Treatment Plan:**

Immediate within 30 days: Update the HR Offboarding SOP to formally 
require IT notification within 24 hours of a staff member's confirmed 
exit date. Add a mandatory IT confirmation step requiring IT to 
acknowledge receipt and confirm access deactivation within the same 
24-hour window. Conduct an immediate audit of all current M365 accounts 
against the HR active staff list and deactivate any former staff 
accounts identified as still active.

Short term within 90 days: Integrate the HR system with the IT 
helpdesk platform so that offboarding triggers an automatic access 
revocation ticket in IT's queue, removing dependency on manual email 
notification. Implement a formal offboarding checklist jointly owned 
by HR and IT that must be completed and signed off before an employee's 
exit is considered fully processed.

Medium term within 180 days: Establish a monthly automated account 
reconciliation process comparing active M365 accounts against the HR 
active staff list. Implement quarterly access reviews with formal 
documentation and sign-off from both the IT Manager and Head of People 
Operations to detect any accounts that slip through the offboarding 
process.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 5, 
Score 10, Level High
**Rationale:** Treatment eliminates the notification delay and 
confirmation gap through process and system improvements. Impact 
remains high because customer financial data exposure through any 
unauthorized access at a PSSP carries inherent severity regardless 
of control improvements.

---

## RISK 2: Authentication Bypass Through Weak Conditional Access

**Scope Area:** Identity and Access Management
**Accountable Owner:** Head of IT Infrastructure
**Responsible Party:** Cloud Administrator
**Threat:** Legacy Authentication Abuse, Adversary-in-the-Middle 
attack, human internal insider threat.
**Vulnerability:** Conditional access policies exist in documentation 
but are not confirmed as fully operational. Legacy authentication 
protocols and session token interception create realistic bypass 
opportunities.
**Asset at Risk:** M365 environment, Azure cloud infrastructure, 
customer financial data, privileged system access.
**Inherent Risk:** Likelihood 4, Impact 5, Score 20, Level Critical
**Existing Controls:** Conditional access policies, Low effectiveness. 
Privileged access management, Absent. Periodic access reviews, 
Ineffective.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 15, Level Critical

**Treatment Plan:**

Immediate within 30 days: Conduct a full technical review of all 
conditional access policies in the M365 admin center to confirm which 
policies are active, correctly configured, and enforcing as intended. 
Immediately block all legacy authentication protocols including POP3, 
IMAP, and basic SMTP across the M365 environment. Enable MFA 
enforcement for all user accounts without exception including shared 
and service accounts.

Short term within 90 days: Implement session token protection through 
Microsoft Entra ID sign-in frequency and persistent browser session 
controls to reduce AiTM attack exposure. Deploy named location policies 
restricting access to approved IP ranges where operationally feasible. 
Establish a quarterly conditional access policy review process with 
documented sign-off.

Medium term within 180 days: Implement a continuous access evaluation 
policy to revoke sessions in real time when risk is detected. Conduct 
penetration testing focused on authentication controls to verify that 
legacy authentication blocking and conditional access policies are 
operating as intended against real-world attack techniques.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 5, 
Score 10, Level High
**Rationale:** Treatment eliminates legacy authentication pathways and 
strengthens session controls, significantly reducing the likelihood of 
successful authentication bypass. Impact remains high given the 
severity of potential unauthorized access to customer financial data.

---

## RISK 3: Privilege Escalation Through Ungoverned Privileged Access

**Scope Area:** Identity and Access Management
**Accountable Owner:** CISO
**Responsible Party:** Head of IT Infrastructure
**Threat:** Human internal. Current staff member or contractor 
exploiting absence of privileged access governance to accumulate 
permissions beyond legitimate scope.
**Vulnerability:** No formal privileged access management process 
exists. Privileged accounts are not inventoried, reviewed, or governed.
**Asset at Risk:** Azure cloud infrastructure, M365 administrator 
accounts, customer financial data, compliance documentation.
**Inherent Risk:** Likelihood 4, Impact 5, Score 20, Level Critical
**Existing Controls:** Privileged access management, Absent. Periodic 
access reviews, Ineffective. Conditional access policies, Ineffective.
**Overall Control Effectiveness:** Ineffective
**Residual Risk:** Score 20, Level Critical

**Treatment Plan:**

Immediate within 30 days: Conduct an immediate audit of all accounts 
across M365 and Azure to identify every account holding elevated or 
administrative permissions. Document a complete privileged account 
inventory listing account name, role, permission level, business 
justification, and account owner. Remove any elevated permissions that 
cannot be justified by a documented business need.

Short term within 90 days: Implement a formal Privileged Access 
Management policy defining how privileged accounts are requested, 
approved, assigned, reviewed, and revoked. Apply the principle of 
least privilege across all privileged accounts. Implement just-in-time 
access for highly privileged operations where users request temporary 
elevated access for specific tasks rather than holding permanent 
elevated permissions.

Medium term within 180 days: Deploy a Privileged Access Workstation 
solution for all administrative activities. Establish quarterly 
privileged access reviews with formal documentation and CISO sign-off. 
Implement privileged session monitoring and recording for all 
administrative activities across Azure and M365.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 4, 
Score 8, Level Medium
**Rationale:** Treatment establishes a complete privileged access 
governance framework eliminating the primary vulnerability. Both 
likelihood and impact reduce as privileged accounts become inventoried, 
governed, and monitored.

---

## RISK 4: Undetected Permission Creep Through Infrequent Access Reviews

**Scope Area:** Identity and Access Management
**Accountable Owner:** Head of IT Infrastructure
**Responsible Party:** Cloud Administrator
**Threat:** Human internal insider threat exploiting accumulated 
permissions, Legacy Authentication Abuse, Adversary-in-the-Middle 
attack.
**Vulnerability:** Last formal access review conducted eight months 
ago against a quarterly requirement. Review was manual, undocumented, 
and unsigned.
**Asset at Risk:** M365 environment, SharePoint document libraries, 
customer financial data, internal compliance records.
**Inherent Risk:** Likelihood 5, Impact 4, Score 20, Level Critical
**Existing Controls:** Periodic access reviews, Low effectiveness. 
Conditional access policies, Ineffective. Privileged access management, 
Absent.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 15, Level Critical

**Treatment Plan:**

Immediate within 30 days: Conduct an immediate comprehensive access 
review across all M365 and SharePoint environments comparing current 
permission assignments against intended permission structures. Revoke 
all permissions identified as expanded beyond intended boundaries. 
Document findings and obtain formal sign-off from the IT Manager and 
Head of IT Infrastructure.

Short term within 90 days: Establish a formal quarterly access review 
process with a defined methodology, documented output template, and 
mandatory sign-off from the IT Manager and a compliance representative. 
Implement automated permission reporting through the M365 admin center 
to generate quarterly permission reports without reliance on manual 
export processes.

Medium term within 180 days: Implement Microsoft Entra ID Access 
Reviews to automate the access review process, sending review requests 
directly to resource owners and managers on a quarterly schedule. 
Establish an access certification process requiring managers to formally 
certify that their team members' access assignments remain appropriate 
on a quarterly basis.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 4, 
Score 8, Level Medium
**Rationale:** Treatment establishes a formal, automated, and 
documented quarterly access review process eliminating the primary 
vulnerability of infrequent and undocumented reviews.

---

## RISK 5: Unprotected Customer Data Due to Absent Data Classification

**Scope Area:** Customer Data Handling
**Accountable Owner:** Data Protection Officer
**Responsible Party:** Chief Compliance Officer
**Threat:** Human external attacker, human internal insider threat, 
organisational human error.
**Vulnerability:** No approved data classification policy exists in 
operational form despite a draft framework awaiting approval for six 
months. Staff have no framework for determining how sensitive customer 
financial data should be stored, shared, or protected.
**Asset at Risk:** Customer personal and financial data including 
account information, transaction records, and payment details.
**Inherent Risk:** Likelihood 5, Impact 5, Score 25, Level Critical
**Existing Controls:** Data classification policy, Absent. Acceptable 
use guidelines, Ineffective. Access restriction to customer data, Low 
effectiveness. Encryption of customer data, Low effectiveness.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 19, Level Critical

**Treatment Plan:**

Immediate within 30 days: Fast-track formal approval of the DPO's 
existing draft data classification framework through an emergency board 
review. Communicate the approved framework to all staff immediately 
with clear guidance on how each data category must be handled, stored, 
and shared. Assign data classification responsibilities to department 
heads with a 30-day deadline for classifying all data assets within 
their function.

Short term within 90 days: Implement technical controls enforcing 
data classification requirements including Microsoft Purview Information 
Protection labels applied to all documents containing customer financial 
data. Train all staff on data classification requirements and their 
obligations under NDPA 2023 with knowledge assessment to verify 
understanding.

Medium term within 180 days: Conduct a full data inventory audit 
across all systems confirming that all customer financial data has been 
classified, labeled, and protected proportionate to its sensitivity. 
Establish an annual data classification review process to ensure the 
framework remains current as Paraclete's data environment evolves.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 4, 
Score 8, Level Medium
**Rationale:** Treatment establishes the foundational data 
classification framework that all other customer data handling controls 
depend on. Once classification is operational and enforced, the 
likelihood of unprotected customer data exposure reduces significantly.

---

## RISK 6: Customer Data Exposure Through Policy Violations

**Scope Area:** Customer Data Handling
**Accountable Owner:** Chief Compliance Officer
**Responsible Party:** Senior Product Operations Manager
**Threat:** Human internal insider threat, organisational human error.
**Vulnerability:** Acceptable Use Policy exists but has no monitoring 
or enforcement mechanism. Active violations confirmed through the 
Senior Product Operations Manager interview including WhatsApp use 
for customer data and personal OneDrive storage for dispute records.
**Asset at Risk:** Customer personal and financial data, transaction 
records, customer dispute information.
**Inherent Risk:** Likelihood 5, Impact 5, Score 25, Level Critical
**Existing Controls:** Acceptable use guidelines, Ineffective. Data 
classification policy, Absent. Management reinforcement of security 
behaviors, Absent.
**Overall Control Effectiveness:** Ineffective
**Residual Risk:** Score 25, Level Critical

**Treatment Plan:**

Immediate within 30 days: Block access to WhatsApp and personal cloud 
storage domains including personal OneDrive and Google Drive on the 
corporate network. Implement Data Loss Prevention policies in Microsoft 
Purview to prevent customer financial data from being transmitted to 
personal email addresses or unapproved external platforms. Issue a 
formal written communication to all operations staff confirming that 
use of personal messaging platforms and personal cloud storage for 
business purposes constitutes a policy violation with defined 
consequences.

Short term within 90 days: Deploy approved secure alternatives for 
operational communication and file sharing, ensuring staff have 
convenient compliant tools that remove the operational pressure driving 
policy violations. Add security behavior accountability to manager job 
descriptions and performance review criteria, making managers formally 
responsible for policy compliance within their teams. Conduct a formal 
disciplinary review of confirmed policy violations identified during 
the assessment.

Medium term within 180 days: Implement a continuous monitoring program 
using Microsoft Defender for Cloud Apps to detect and alert on policy 
violations in real time. Establish a quarterly compliance audit of 
operational data handling practices to verify that violations have not 
recurred. Tie operational team performance metrics to security behavior 
compliance to reinforce culture change at the management level.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 4, 
Score 8, Level Medium
**Rationale:** Treatment combines technical blocking controls, approved 
alternatives, management accountability, and continuous monitoring to 
address both the technical and behavioral dimensions of this risk.

---

## RISK 7: Unauthorized Access to Customer Data Through Expanded Permissions

**Scope Area:** Customer Data Handling
**Accountable Owner:** Data Protection Officer
**Responsible Party:** Cloud Administrator
**Threat:** Human internal insider threat, human external attacker, 
Legacy Authentication Abuse, Adversary-in-the-Middle attack.
**Vulnerability:** SharePoint permissions have expanded beyond 
originally intended boundaries without detection. Last formal 
permission review was eight months ago.
**Asset at Risk:** Customer financial data stored in SharePoint 
document libraries and Azure cloud storage.
**Inherent Risk:** Likelihood 5, Impact 5, Score 25, Level Critical
**Existing Controls:** Access restriction to customer data, Low 
effectiveness. Periodic access reviews, Ineffective. Data 
classification policy, Absent.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 19, Level Critical

**Treatment Plan:**

Immediate within 30 days: Export the full SharePoint permission report 
and compare it against the original permission design documentation. 
Immediately revert all permissions identified as expanded beyond 
originally intended boundaries. Document all permission changes made 
with sign-off from the Cloud Administrator and Head of IT Infrastructure.

Short term within 90 days: Implement a formal SharePoint governance 
policy defining who has authority to grant, modify, or revoke 
permissions and requiring documented approval for any permission change. 
Enable SharePoint audit logging to capture all permission changes in 
real time. Implement Microsoft Entra ID Access Reviews for all 
SharePoint document libraries containing customer financial data on 
a quarterly basis.

Medium term within 180 days: Implement sensitivity labels through 
Microsoft Purview on all SharePoint document libraries containing 
customer financial data, automatically restricting access to authorized 
users only. Establish a formal data access request process requiring 
business justification and approval before any new permission is granted 
to customer financial data repositories.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 4, 
Score 8, Level Medium
**Rationale:** Treatment establishes formal permission governance, 
automated reviews, and technical access controls that eliminate the 
conditions allowing permission expansion to go undetected.

---

## RISK 8: Customer Data Interception Through Inadequate Encryption

**Scope Area:** Customer Data Handling
**Accountable Owner:** Data Protection Officer
**Responsible Party:** Cloud Administrator
**Threat:** Human external attacker, technical threat including 
ransomware and data interception.
**Vulnerability:** No documented encryption standard exists. No formal 
encryption requirement defined for different categories of customer 
data across Azure storage services.
**Asset at Risk:** Customer personal and financial data stored across 
Azure storage services and transmitted between internal systems.
**Inherent Risk:** Likelihood 3, Impact 5, Score 15, Level Critical
**Existing Controls:** Encryption of customer data, Low effectiveness. 
Data classification policy, Absent. Access restriction to customer 
data, Low effectiveness.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 11, Level High

**Treatment Plan:**

Immediate within 30 days: Conduct a full encryption audit across all 
Azure storage services to confirm current encryption status for all 
storage accounts holding customer financial data. Enable encryption 
at rest for any storage service identified as not currently encrypted. 
Enable HTTPS enforcement for all data in transit across Azure services.

Short term within 90 days: Define and document a formal encryption 
standard as part of the data classification framework being fast-tracked 
for approval under Risk 5 treatment. The standard should specify minimum 
encryption requirements for each data classification category 
proportionate to sensitivity and PCI-DSS requirements. Implement Azure 
Key Vault for centralized encryption key management across all customer 
data storage services.

Medium term within 180 days: Conduct annual encryption audits to 
verify that encryption standards are being consistently applied across 
all storage services as Paraclete's cloud environment evolves. 
Implement automated policy enforcement through Azure Policy to prevent 
the creation of unencrypted storage resources holding customer data.

**Target Residual Risk After Treatment:** Likelihood 1, Impact 5, 
Score 5, Level Medium
**Rationale:** Treatment establishes comprehensive encryption across 
all customer data storage services. Likelihood reduces significantly 
as encryption becomes systematically applied and technically enforced 
through Azure Policy. Impact remains high given the inherent sensitivity 
of customer financial data. This is one of three risks that reduces 
from critical to high at the residual level, alongside Risks 11 and 14.

---

## RISK 9: Regulatory Sanction Due to Absent Breach Notification Procedure

**Scope Area:** Customer Data Handling
**Accountable Owner:** Data Protection Officer
**Responsible Party:** Chief Compliance Officer
**Threat:** Organisational threat and regulatory risk.
**Vulnerability:** No operational breach notification procedure exists. 
Organization cannot determine what constitutes a notifiable breach or 
meet NDPA 2023 72-hour notification requirement.
**Asset at Risk:** Paraclete's regulatory standing, PSSP licence, 
and customer trust.
**Inherent Risk:** Likelihood 4, Impact 5, Score 20, Level Critical
**Existing Controls:** Breach notification procedure, Absent. Data 
classification policy, Absent. Remediation tracking control, 
Ineffective.
**Overall Control Effectiveness:** Ineffective
**Residual Risk:** Score 20, Level Critical

**Treatment Plan:**

Immediate within 30 days: Draft and obtain emergency board approval 
for a Breach Notification Procedure defining what constitutes a 
notifiable breach under NDPA 2023 and PCI-DSS, the internal escalation 
chain from discovery to notification decision, the 72-hour notification 
timeline and process for notifying the Nigeria Data Protection 
Commission, and the customer communication protocol following a 
confirmed breach.

Short term within 90 days: Conduct a tabletop breach simulation 
exercise involving the DPO, CCO, CISO, and Head of IT Infrastructure 
to test the breach notification procedure under realistic conditions 
and identify any gaps before a real incident occurs. Assign a named 
Breach Response Coordinator responsible for managing the notification 
process in the event of an incident.

Medium term within 180 days: Integrate the breach notification 
procedure with the incident response plan to ensure seamless escalation 
from incident detection to breach assessment to regulatory notification. 
Conduct annual breach notification drills to maintain organizational 
readiness and demonstrate to CBN examiners that the procedure is 
operational and tested.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 3, 
Score 6, Level Medium
**Rationale:** Treatment establishes a complete, tested breach 
notification procedure eliminating the primary vulnerability. Both 
likelihood of regulatory sanction and impact reduce significantly as 
the organization gains the capability to respond to breaches in a 
structured and timely manner.

---

## RISK 10: Staff Susceptibility to Phishing and Social Engineering

**Scope Area:** Cybersecurity Awareness and Human Risk
**Accountable Owner:** Chief Compliance Officer
**Responsible Party:** Head of People Operations
**Threat:** Human external attacker using phishing emails, spear 
phishing, and social engineering.
**Vulnerability:** Training occurs annually without knowledge retention 
assessment. Three supporting controls are completely absent.
**Asset at Risk:** M365 environment, staff credentials, customer 
financial data, payment processing infrastructure.
**Inherent Risk:** Likelihood 4, Impact 5, Score 20, Level Critical
**Existing Controls:** Cybersecurity awareness training program, Low 
effectiveness. Formal knowledge assessment, Absent. Phishing simulation 
program, Absent. Continuous security awareness communications, Absent.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 15, Level Critical

**Treatment Plan:**

Immediate within 30 days: Launch an emergency phishing awareness 
communication to all staff highlighting current phishing threats 
targeting Nigerian fintechs, with specific guidance on identifying and 
reporting suspicious emails. Enable Microsoft Defender for Office 365 
anti-phishing policies across the M365 environment to provide technical 
filtering against known phishing techniques.

Short term within 90 days: Implement a phishing simulation program 
using Microsoft Attack Simulator, conducting monthly simulated phishing 
campaigns to measure staff susceptibility across departments. Add a 
formal knowledge assessment to the annual cybersecurity training program 
requiring staff to achieve a minimum passing score before training is 
considered complete. Establish a monthly security awareness newsletter 
distributed to all staff covering current threats, recent incidents in 
the fintech sector, and practical security guidance.

Medium term within 180 days: Use phishing simulation results to 
identify high-risk staff and departments requiring targeted additional 
training. Implement a Security Champions program identifying one 
security-aware staff member per department to promote security culture 
and serve as a first point of contact for security concerns within 
their team.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 4, 
Score 8, Level Medium
**Rationale:** Treatment combines technical anti-phishing controls, 
regular simulation testing, and continuous awareness communications 
to significantly reduce staff susceptibility.

---

## RISK 11: Unverified Security Behavior Due to Absent Knowledge Assessment

**Scope Area:** Cybersecurity Awareness and Human Risk
**Accountable Owner:** Head of People Operations
**Responsible Party:** Chief Compliance Officer
**Threat:** Organisational human error from staff who completed 
training without retaining knowledge.
**Vulnerability:** No formal assessment exists at end of training. 
Organization cannot verify whether training produced behavioral change.
**Asset at Risk:** Customer financial data, M365 environment, and 
Paraclete's compliance posture.
**Inherent Risk:** Likelihood 5, Impact 3, Score 15, Level Critical
**Existing Controls:** Formal knowledge assessment, Absent. 
Cybersecurity awareness training program, Low effectiveness.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 11, Level High

**Treatment Plan:**

Immediate within 30 days: Design and implement a formal post-training 
knowledge assessment of a minimum of 15 questions covering key security 
topics including phishing identification, data handling, password 
security, and acceptable use. Require all staff to achieve a minimum 
passing score of 80% before training completion is recorded. Staff who 
do not pass must complete remedial training and reassessment.

Short term within 90 days: Integrate knowledge assessment results into 
the HR training records system so that compliance reporting to CBN can 
demonstrate not just training completion but verified knowledge 
retention. Establish a process for sharing anonymized assessment results 
with department heads so managers can identify knowledge gaps within 
their teams.

Medium term within 180 days: Implement quarterly micro-assessments of 
five to ten questions covering recent security topics to maintain 
knowledge currency between annual training cycles. Use assessment 
results to continuously refine training content ensuring it addresses 
actual knowledge gaps.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 3, 
Score 6, Level Medium
**Rationale:** Treatment establishes formal knowledge verification 
eliminating the inability to confirm training effectiveness. Likelihood 
reduces as staff are required to demonstrate understanding rather than 
just complete training. This is one of three risks that reduces from 
critical to high at the residual level, alongside Risks 8 and 14.

---

## RISK 12: Undetected Phishing Susceptibility Across Staff

**Scope Area:** Cybersecurity Awareness and Human Risk
**Accountable Owner:** CISO
**Responsible Party:** Head of People Operations
**Threat:** Human external attacker using targeted phishing campaigns.
**Vulnerability:** No phishing simulation program exists. Staff 
susceptibility has never been tested or measured.
**Asset at Risk:** Staff credentials, customer financial data, payment 
processing systems, operational continuity.
**Inherent Risk:** Likelihood 4, Impact 5, Score 20, Level Critical
**Existing Controls:** Phishing simulation program, Absent. 
Cybersecurity awareness training program, Low effectiveness. Formal 
knowledge assessment, Absent.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 15, Level Critical

**Treatment Plan:**

Immediate within 30 days: Implement Microsoft Defender for Office 365 
Attack Simulator to begin monthly phishing simulation campaigns across 
all staff. Establish a baseline susceptibility measurement in the first 
simulation campaign to understand current risk exposure before training 
interventions are applied.

Short term within 90 days: Use baseline simulation results to identify 
high-risk staff and departments. Design targeted phishing awareness 
training for high-risk groups addressing the specific phishing 
techniques they failed to identify in simulations. Establish a clear 
process for staff to report suspected phishing attempts with a named 
point of contact and a maximum four-hour response time commitment.

Medium term within 180 days: Track phishing simulation susceptibility 
rates monthly, setting a target of reducing organization-wide 
susceptibility to below 5% within 12 months of program launch. Report 
simulation results quarterly to the CISO and board as a key human risk 
metric.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 4, 
Score 8, Level Medium
**Rationale:** Treatment establishes a continuous measurement and 
improvement cycle for phishing susceptibility, transforming an 
unmeasured risk into a tracked and managed metric with a defined target.

---

## RISK 13: Fraudulent Access Through Undetected Credential Sharing

**Scope Area:** Cybersecurity Awareness and Human Risk
**Accountable Owner:** Head of IT Infrastructure
**Responsible Party:** Senior Product Operations Manager
**Threat:** Human internal insider threat exploiting shared credentials, 
human external attacker obtaining shared credentials.
**Vulnerability:** Audit logs not regularly reviewed. Credential 
sharing already confirmed as established practice during peak periods 
through the Senior Product Operations Manager interview.
**Asset at Risk:** Operations dashboard, customer transaction records, 
customer financial data, transaction processing integrity.
**Inherent Risk:** Likelihood 5, Impact 5, Score 25, Level Critical
**Existing Controls:** Credential sharing detection, Absent. Acceptable 
use guidelines, Ineffective. Management reinforcement of security 
behaviors, Absent.
**Overall Control Effectiveness:** Ineffective
**Residual Risk:** Score 25, Level Critical

**Treatment Plan:**

Immediate within 30 days: Enable and configure Microsoft Entra ID 
sign-in logs and audit logs for active monitoring. Assign a named IT 
staff member responsible for reviewing sign-in logs weekly for 
impossible travel patterns, concurrent sessions, and unusual activity 
volumes. Issue a formal written directive to all operations staff and 
managers that credential sharing constitutes a serious policy violation 
with immediate disciplinary consequences.

Short term within 90 days: Implement individual authentication for 
the operations dashboard, removing any shared account access and 
ensuring every user authenticates with their own credentials. Deploy 
Microsoft Entra ID Conditional Access policies requiring MFA for all 
operations dashboard access. Address the operational pressure driving 
credential sharing by reviewing and optimizing the authentication 
process to reduce login time during peak periods.

Medium term within 180 days: Implement User and Entity Behavior 
Analytics through Microsoft Sentinel to automatically detect and alert 
on credential sharing patterns without relying on manual log review. 
Establish a formal incident response process for credential sharing 
violations including investigation, disciplinary action, and password 
reset procedures. Conduct quarterly audit log reviews with documented 
findings reported to the CISO.

**Target Residual Risk After Treatment:** Likelihood 1, Impact 4, 
Score 4, Level Low
**Rationale:** Treatment combines technical enforcement of individual 
authentication, active monitoring, and management accountability to 
eliminate the conditions enabling credential sharing. Likelihood reduces 
to rare as individual authentication becomes technically enforced and 
active monitoring creates strong deterrence.

---

## RISK 14: Security Behavior Degradation Between Training Cycles

**Scope Area:** Cybersecurity Awareness and Human Risk
**Accountable Owner:** Chief Compliance Officer
**Responsible Party:** Head of People Operations
**Threat:** Organisational human error, human external attacker 
exploiting widening awareness gaps.
**Vulnerability:** Security awareness limited to annual training with 
no reinforcement between cycles. Behavioral degradation already 
confirmed by interview findings.
**Asset at Risk:** Staff security behavior, customer financial data, 
human layer risk posture.
**Inherent Risk:** Likelihood 5, Impact 3, Score 15, Level Critical
**Existing Controls:** Continuous security awareness communications, 
Absent. Cybersecurity awareness training program, Low effectiveness. 
Management reinforcement of security behaviors, Absent.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 11, Level High

**Treatment Plan:**

Immediate within 30 days: Launch a monthly security awareness 
newsletter distributed to all staff covering current threats, recent 
fintech sector incidents, practical security tips, and reminders of 
key policy requirements.

Short term within 90 days: Establish a Security Champions program with 
one nominated champion per department responsible for promoting security 
awareness within their team and escalating security concerns. Implement 
a quarterly security briefing for all managers covering current threat 
trends, recent internal policy violations, and their accountability for 
security behavior within their teams.

Medium term within 180 days: Develop a security awareness calendar 
covering the full year with planned communications, training refreshers, 
simulation exercises, and awareness events timed to reinforce key 
security behaviors throughout the year rather than concentrating all 
security activity in the annual training window.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 3, 
Score 6, Level Medium
**Rationale:** Treatment establishes continuous security awareness 
reinforcement eliminating the annual training only approach. Likelihood 
reduces as security behaviors are consistently reinforced throughout 
the year. This is one of three risks that reduces from critical to high 
at the residual level, alongside Risks 8 and 11.

---

## RISK 15: Normalised Policy Violations Through Absent Management Accountability

**Scope Area:** Cybersecurity Awareness and Human Risk
**Accountable Owner:** Chief Compliance Officer
**Responsible Party:** Senior Product Operations Manager
**Threat:** Organisational human error, human internal insider threat 
in environment where violations are tolerated.
**Vulnerability:** Management not actively reinforcing security 
behaviors. Policy violations confirmed as normalised without challenge 
or correction through the Senior Product Operations Manager interview.
**Asset at Risk:** Customer financial data, acceptable use policy 
compliance posture, security culture.
**Inherent Risk:** Likelihood 5, Impact 4, Score 20, Level Critical
**Existing Controls:** Management reinforcement of security behaviors, 
Absent. Acceptable use guidelines, Ineffective. Continuous security 
awareness communications, Absent.
**Overall Control Effectiveness:** Ineffective
**Residual Risk:** Score 20, Level Critical

**Treatment Plan:**

Immediate within 30 days: Issue a formal management directive from 
the CCO and Senior Product Operations Manager jointly confirming that 
security policy compliance is a management responsibility and that 
known violations must be addressed immediately. Conduct a formal 
briefing with all operations managers confirming their accountability 
for security behavior within their teams and the consequences of 
continued policy violations.

Short term within 90 days: Update all manager job descriptions to 
include formal security behavior accountability responsibilities. 
Incorporate security compliance metrics into manager performance 
reviews and promotion criteria. Establish a quarterly management 
security compliance report reviewed by the CCO showing policy violation 
rates by department and manager.

Medium term within 180 days: Implement a formal security culture 
assessment annually measuring staff and management attitudes toward 
security compliance. Use assessment results to identify departments 
or managers requiring additional support or intervention. Recognize 
and reward teams demonstrating strong security compliance to reinforce 
positive security culture alongside the disciplinary framework.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 3, 
Score 6, Level Medium
**Rationale:** Treatment establishes formal management accountability 
for security behavior, transforming compliance from an individual 
responsibility to a management performance metric.

---

## RISK 16: Regulatory Non-Compliance Due to Outdated or Absent Policies

**Scope Area:** Governance and Policy Posture
**Accountable Owner:** Chief Compliance Officer
**Responsible Party:** Not applicable, single owner sufficient
**Threat:** Regulatory risk, organisational human error.
**Vulnerability:** Two key policies absent or inactive. Policy review 
cycle not operating on schedule.
**Asset at Risk:** Paraclete's regulatory standing, PSSP licence, 
governance posture.
**Inherent Risk:** Likelihood 5, Impact 4, Score 20, Level Critical
**Existing Controls:** Policy review and management control, Low 
effectiveness. Policy approval governance control, Absent. Remediation 
tracking control, Low effectiveness.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 15, Level Critical

**Treatment Plan:**

Immediate within 30 days: Fast-track board approval of the data 
classification policy and third-party risk management policy as the 
two highest priority absent policies. Conduct an immediate audit of 
all policies against the governance framework requirements to identify 
every policy that is absent, inactive, or overdue for review. Produce 
a complete policy status register with current version, last review 
date, next review date, and responsible owner for every policy.

Short term within 90 days: Establish a formal Policy Governance 
Framework defining the policy lifecycle from drafting through approval, 
communication, review, and retirement. Assign a named policy owner to 
every policy with formal accountability for keeping their policy 
current. Implement a policy review calendar in the compliance tracking 
system with automated reminders sent to policy owners 60 days before 
each policy's review date.

Medium term within 180 days: Conduct a full policy suite review 
ensuring all policies are aligned with current CBN Cybersecurity 
Framework requirements, NDPA 2023 obligations, and PCI-DSS standards 
ahead of the Q4 2026 CBN examination. Present the completed policy 
register and governance framework to the board as evidence of 
regulatory readiness.

**Target Residual Risk After Treatment:** Likelihood 1, Impact 3, 
Score 3, Level Low
**Rationale:** Treatment establishes a complete policy governance 
framework with formal ownership, scheduled reviews, and board 
accountability. Likelihood reduces to rare as the policy approval 
and review process becomes systematic and tracked.

---

## RISK 17: Escalated Regulatory Findings Due to Overdue Remediation

**Scope Area:** Governance and Policy Posture
**Accountable Owner:** Chief Compliance Officer
**Responsible Party:** Not applicable, single owner sufficient
**Threat:** Regulatory risk from open CBN examination findings 
exceeding remediation deadlines.
**Vulnerability:** Two of three open CBN findings have exceeded target 
remediation deadlines. Remediation tracker not driving timely action.
**Asset at Risk:** Paraclete's regulatory standing, PSSP licence, 
CBN relationship.
**Inherent Risk:** Likelihood 5, Impact 4, Score 20, Level Critical
**Existing Controls:** Remediation tracking control, Low effectiveness. 
Policy review and management control, Ineffective against this specific 
risk.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 15, Level Critical

**Treatment Plan:**

Immediate within 30 days: Convene an emergency remediation review 
meeting with the CCO, CISO, and relevant stakeholders to assess the 
current status of all three open CBN examination findings. Produce a 
revised remediation plan for each open finding with specific action 
owners, weekly milestones, and a revised target closure date. Assign 
a dedicated remediation coordinator responsible for tracking progress 
against the revised plan on a weekly basis.

Short term within 90 days: Close all three open CBN examination 
findings within the revised remediation timelines. Produce formal 
closure evidence for each finding documenting the remediation action 
taken, the date completed, and the evidence demonstrating the finding 
has been addressed. Submit closure evidence to CBN proactively ahead 
of the Q4 2026 examination to demonstrate remediation discipline.

Medium term within 180 days: Implement a formal regulatory finding 
management process requiring that all future examination findings are 
assigned an owner, a remediation plan, and a target closure date within 
five business days of receipt. Establish monthly remediation progress 
reporting to the board so that overdue remediation commitments are 
escalated to board level before they exceed deadlines.

**Target Residual Risk After Treatment:** Likelihood 1, Impact 3, 
Score 3, Level Low
**Rationale:** Treatment closes all open findings before the Q4 2026 
examination and establishes a formal management process preventing 
future findings from exceeding remediation deadlines.

---

## RISK 18: Supply Chain Attack Through Unassessed Third Party Vendors

**Scope Area:** Governance and Policy Posture
**Accountable Owner:** Chief Compliance Officer
**Responsible Party:** Head of IT Infrastructure
**Threat:** Human external attacker exploiting third party vendor 
access, supply chain attack, organisational human error through 
unapproved tool use.
**Vulnerability:** Third Party Risk Management Policy in draft form 
and never operationalized. Several vendors never assessed including 
unapproved external document conversion tool confirmed as processing 
customer reference data through the Senior Product Operations Manager 
interview.
**Asset at Risk:** Customer financial data, Azure cloud infrastructure, 
overall security perimeter.
**Inherent Risk:** Likelihood 4, Impact 5, Score 20, Level Critical
**Existing Controls:** Third party risk management, Absent. Acceptable 
use guidelines, Ineffective. Policy approval governance control, Absent.
**Overall Control Effectiveness:** Ineffective
**Residual Risk:** Score 20, Level Critical

**Treatment Plan:**

Immediate within 30 days: Immediately block the unapproved external 
document conversion tool identified during the Senior Product Operations 
Manager interview and provide staff with an approved internal 
alternative. Produce a full inventory of all third party vendors and 
tools currently in use across Paraclete including those not formally 
approved by IT. Fast-track board approval of the Third Party Risk 
Management Policy currently in draft form.

Short term within 90 days: Conduct a retrospective security assessment 
of all vendors identified in the inventory using a standardized vendor 
risk assessment questionnaire covering security controls, data handling 
practices, regulatory compliance, and incident response capability. 
Establish data processing agreements with all vendors confirmed as 
processing Paraclete customer personal data, as required under NDPA 
2023. Implement a formal vendor onboarding process requiring IT security 
approval and risk assessment before any new vendor is engaged.

Medium term within 180 days: Establish an annual vendor risk review 
process reassessing all active vendors against current security 
standards. Implement a vendor security monitoring program for high-risk 
vendors with access to or adjacency to Paraclete's cloud environment. 
Include third party risk management as a standing agenda item in 
quarterly board risk reporting.

**Target Residual Risk After Treatment:** Likelihood 2, Impact 4, 
Score 8, Level Medium
**Rationale:** Treatment establishes a complete vendor risk management 
lifecycle from onboarding assessment through annual review and 
continuous monitoring. Likelihood reduces significantly as all vendors 
are formally assessed and unapproved tools are blocked.

---

## RISK 19: Governance Failure Due to Absent Policy Approval Process

**Scope Area:** Governance and Policy Posture
**Accountable Owner:** Chief Compliance Officer
**Responsible Party:** Chief Executive Officer
**Threat:** Regulatory risk, organisational human error from 
non-functional policy governance.
**Vulnerability:** No formal policy approval timeline or escalation 
process exists. DPO's draft data classification framework has sat 
unapproved for six months.
**Asset at Risk:** Paraclete's governance posture, regulatory 
standing, operational security controls dependent on approved policies.
**Inherent Risk:** Likelihood 5, Impact 4, Score 20, Level Critical
**Existing Controls:** Policy approval governance control, Absent. 
Policy review and management control, Low effectiveness. Remediation 
tracking control, Ineffective.
**Overall Control Effectiveness:** Low
**Residual Risk:** Score 15, Level Critical

**Treatment Plan:**

Immediate within 30 days: Establish a formal Policy Approval Committee 
comprising the CCO, CISO, DPO, and a board representative with a 
defined meeting cadence of at minimum monthly and a mandatory maximum 
five business day turnaround for policy approval decisions. Immediately 
escalate the DPO's draft data classification framework to the Policy 
Approval Committee for review and approval as the highest priority 
pending policy.

Short term within 90 days: Define and document a formal Policy Approval 
Process covering submission requirements, review timelines, approval 
authority levels, escalation procedures for stalled approvals, and 
communication requirements for approved policies. Implement a policy 
approval tracking register in the compliance system showing the status 
of every policy in the approval pipeline with age, responsible reviewer, 
and escalation trigger date.

Medium term within 180 days: Conduct a quarterly Policy Approval 
Committee review of the policy pipeline ensuring no policy remains in 
draft status beyond 60 days without a documented reason and board-level 
escalation. Report policy approval cycle times to the board quarterly 
as a governance health metric, with a target of zero policies remaining 
unapproved beyond 60 days from submission.

**Target Residual Risk After Treatment:** Likelihood 1, Impact 3, 
Score 3, Level Low
**Rationale:** Treatment establishes a formal Policy Approval Committee 
with defined timelines, escalation procedures, and board-level 
oversight, eliminating the governance vacuum that allowed the data 
classification policy to remain unapproved for six months.

---

## Risk Register Overview

| Risk | Description | Inherent Score | Inherent Level | Residual Score | Residual Level | Target Score | Target Level |
|---|---|---|---|---|---|---|---|
| R1 | Unauthorised Access by Former Staff | 25 | Critical | 19 | Critical | 10 | High |
| R2 | Authentication Bypass Through Weak Conditional Access | 20 | Critical | 15 | Critical | 10 | High |
| R3 | Privilege Escalation Through Ungoverned Privileged Access | 20 | Critical | 20 | Critical | 8 | Medium |
| R4 | Undetected Permission Creep Through Infrequent Access Reviews | 20 | Critical | 15 | Critical | 8 | Medium |
| R5 | Unprotected Customer Data Due to Absent Data Classification | 25 | Critical | 19 | Critical | 8 | Medium |
| R6 | Customer Data Exposure Through Policy Violations | 25 | Critical | 25 | Critical | 8 | Medium |
| R7 | Unauthorized Access to Customer Data Through Expanded Permissions | 25 | Critical | 19 | Critical | 8 | Medium |
| R8 | Customer Data Interception Through Inadequate Encryption | 15 | Critical | 11 | High | 5 | Medium |
| R9 | Regulatory Sanction Due to Absent Breach Notification Procedure | 20 | Critical | 20 | Critical | 6 | Medium |
| R10 | Staff Susceptibility to Phishing and Social Engineering | 20 | Critical | 15 | Critical | 8 | Medium |
| R11 | Unverified Security Behavior Due to Absent Knowledge Assessment | 15 | Critical | 11 | High | 6 | Medium |
| R12 | Undetected Phishing Susceptibility Across Staff | 20 | Critical | 15 | Critical | 8 | Medium |
| R13 | Fraudulent Access Through Undetected Credential Sharing | 25 | Critical | 25 | Critical | 4 | Low |
| R14 | Security Behavior Degradation Between Training Cycles | 15 | Critical | 11 | High | 6 | Medium |
| R15 | Normalised Policy Violations Through Absent Management Accountability | 20 | Critical | 20 | Critical | 6 | Medium |
| R16 | Regulatory Non-Compliance Due to Outdated or Absent Policies | 20 | Critical | 15 | Critical | 3 | Low |
| R17 | Escalated Regulatory Findings Due to Overdue Remediation | 20 | Critical | 15 | Critical | 3 | Low |
| R18 | Supply Chain Attack Through Unassessed Third Party Vendors | 20 | Critical | 20 | Critical | 8 | Medium |
| R19 | Governance Failure Due to Absent Policy Approval Process | 20 | Critical | 15 | Critical | 3 | Low |

---

## Remediation Priority Summary

Given the volume of critical risks and the Q4 2026 CBN examination 
timeline, remediation must be prioritized strategically. Prioritization 
follows three filters applied simultaneously: residual risk score, 
regulatory and business deadline implications, and whether fixing one 
risk reduces other risks simultaneously.

### Priority 1: Immediate Action Within 30 Days
Risks with residual scores of 25, meaning existing controls provide 
zero protection. These require immediate action before any other 
remediation activity.

- Risk 6: Customer Data Exposure Through Policy Violations. 
  Residual score 25.
- Risk 13: Fraudulent Access Through Undetected Credential Sharing. 
  Residual score 25.

### Priority 2: Critical Risks With Regulatory Examination Implications
These risks directly affect Paraclete's CBN examination readiness 
and must be substantially remediated before Q4 2026.

- Risk 1: Unauthorised Access by Former Staff
- Risk 5: Unprotected Customer Data Due to Absent Data Classification
- Risk 9: Regulatory Sanction Due to Absent Breach Notification 
  Procedure
- Risk 16: Regulatory Non-Compliance Due to Outdated or Absent Policies
- Risk 17: Escalated Regulatory Findings Due to Overdue Remediation
- Risk 19: Governance Failure Due to Absent Policy Approval Process

### Priority 3: Remaining Critical and High Risks
All remaining risks should be substantially remediated within 180 days.

- Risk 2, Risk 3, Risk 4, Risk 7, Risk 10, Risk 12, Risk 15, Risk 18

### Priority 4: High Risks With Ongoing Management
These risks reduce to high at the residual level and require ongoing 
management through the treatment plans defined above.

- Risk 8, Risk 11, Risk 14

---

## Target Risk Profile After Full Remediation

| Target Risk Level | Number of Risks | Percentage |
|---|---|---|
| Low | 4 | 21% |
| Medium | 13 | 68% |
| High | 2 | 11% |
| Critical | 0 | 0% |
| **Total** | **19** | **100%** |

Full implementation of all treatment plans would reduce Paraclete's 
risk profile from nineteen critical risks to an acceptable level, with 
thirteen risks at medium level, four at low level, and two remaining 
at high level. This target profile represents the intended residual 
risk position against which Paraclete's risk appetite should be 
measured. It reflects a defensible security posture appropriate for 
a regulated PSSP operating under CBN oversight, NDPA 2023 obligations, 
and PCI-DSS requirements.

---

## Conclusion

This risk register represents a complete, evidence-based assessment 
of Paraclete's cyber risk posture across four defined scope areas. 
Every risk has been identified from confirmed control gaps, rated using 
a consistent likelihood and impact methodology, assessed against 
existing control effectiveness, and assigned a specific, actionable 
treatment plan with defined owners, timelines, and target risk levels.

The consistent finding across all nineteen risks is that Paraclete's 
current security posture reflects an organization that has grown rapidly 
without proportionate investment in security governance, policy 
development, and control implementation. The remediation roadmap 
defined in this register provides a structured, prioritized pathway 
to transform that posture into one that is defensible, compliant, and 
appropriate for a regulated fintech approaching both a Series B 
fundraising round and a CBN regulatory examination in Q4 2026.
