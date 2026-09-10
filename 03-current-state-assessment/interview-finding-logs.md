# Verdant Pay Limited
## Stage 3, Part 2: Interview Finding Logs
**Confidential | Internal Use Only**

## Purpose

This document records the findings from all seven stakeholder interviews 
conducted during the Verdant Pay cyber risk assessment. Each log 
documents what the stakeholder said, what existing documentation states, 
any variance identified between the two, the risk implication of that 
variance, and any follow-up documentation requested as a result.

Variances between documented procedure and actual practice represent 
the most valuable finding source in the assessment. They are the 
evidence base from which risks are identified and justified in 
subsequent stages.

---

## Interview Log 1: Head of IT Infrastructure
**Date of Interview:** 14 March 2026
**Interviewed by:** Omotayo Akinola, GRC Analyst
**Interview Duration:** 50 minutes

### Finding 1
**Question asked:** When an employee leaves Verdant Pay, at what point 
do you revoke their privileged access and how quickly does that happen?

**What the stakeholder said:** IT revokes access once a notification 
is received from HR. However the notification does not always come 
through promptly. When it does arrive, the team typically processes 
the revocation within a few hours but there have been instances where 
the helpdesk ticket sat unassigned for a day or two, especially during 
busy periods.

**What existing documentation states:** The IT Access Management Policy 
states that access must be revoked within 24 hours of receiving an 
offboarding notification from HR.

**Variance identified:** Yes. While the policy requires revocation 
within 24 hours of notification, actual processing time varies and has 
exceeded this window during periods of high workload. Combined with 
delayed notifications from HR, total time between exit and access 
revocation can extend significantly beyond 24 hours.

**Risk implication:** The 24-hour revocation requirement is not 
consistently met in practice. Combined with delayed HR notifications, 
former staff accounts may remain active for several days or weeks after 
exit, directly consistent with the Q1 2026 flagged incident.

**Follow-up document requested:** IT helpdesk ticket logs for 
offboarding requests over the last 12 months, to measure actual 
revocation turnaround times against the 24-hour policy requirement.

---

### Finding 2
**Question asked:** When a new employee is onboarded, how many days 
or hours does it take to grant them the access they need?

**What the stakeholder said:** Access is typically granted within one 
to two business days of receiving the onboarding request from HR. 
However the level of access granted is based on whatever HR requests, 
and those requests are often vague, saying things like standard access 
without specifying which systems or permission levels are actually 
needed for the role.

**What existing documentation states:** The IT Access Management Policy 
requires that access be granted based on a formally approved access 
request specifying role-based permissions aligned to the principle of 
least privilege.

**Variance identified:** Yes. Access requests from HR are frequently 
vague and do not specify role-based permissions. IT is effectively 
making access decisions that should be driven by the business, which 
may result in over-provisioning or inconsistent access assignments 
across similar roles.

**Risk implication:** Vague onboarding access requests create a risk 
of over-provisioned accounts where staff have access beyond what their 
role requires. This is a direct least-privilege gap and a potential 
contributor to the SharePoint permission expansion identified in Q1 2026.

**Follow-up document requested:** Sample onboarding access request 
forms submitted by HR to IT over the last six months.

---

### Finding 3
**Question asked:** Do you communicate back to HR after onboarding or 
offboarding an employee and do you record that confirmation immediately?

**What the stakeholder said:** IT does not formally confirm back to HR 
when access has been granted or revoked. The team considers the helpdesk 
ticket closure as sufficient confirmation but HR does not have visibility 
into the helpdesk system and would not know when a ticket was closed.

**What existing documentation states:** Neither the HR Offboarding SOP 
nor the IT Access Management Policy specifies a formal confirmation step 
from IT back to HR.

**Variance identified:** No variance between documentation and practice. 
However both reflect an absent control. There is no closed-loop 
confirmation process between IT and HR, meaning HR cannot verify whether 
their access requests have been acted on.

**Risk implication:** The absence of a confirmation loop means access 
changes can be delayed or missed entirely without either party being 
aware. This is a process control gap that directly enables the Q1 2026 
flagged incident to recur.

**Follow-up document requested:** Current IT helpdesk workflow 
documentation showing how offboarding tickets are assigned, tracked, 
and closed.

### Overall Interview Assessment
This interview surfaced three findings across the identity and access 
management scope area. The most significant finding is the combination 
of delayed HR notifications and inconsistent IT processing times, which 
together explain how former staff accounts can remain active for extended 
periods after exit. All three findings will be carried forward into the 
current state assessment report.

---

## Interview Log 2: Cloud Administrator
**Date of Interview:** 15 March 2026
**Interviewed by:** Omotayo Akinola, GRC Analyst
**Interview Duration:** 55 minutes

### Finding 1
**Question asked:** When and how were access permissions last reviewed 
and by whom?

**What the stakeholder said:** The last formal permission review was 
conducted approximately eight months ago. It was done manually by the 
Cloud Administrator by exporting a user list from the M365 admin center 
and cross-checking it against the active staff list from HR. The review 
was not formally documented and no sign-off was obtained from a manager 
or compliance representative.

**What existing documentation states:** The IT Access Management Policy 
requires quarterly permission reviews with documented sign-off from the 
IT Manager.

**Variance identified:** Yes. The last review was conducted eight months 
ago against a quarterly requirement, and it was neither formally 
documented nor signed off. The review process itself was informal and 
manual with no structured methodology.

**Risk implication:** Permission reviews are not occurring at the 
required frequency and lack the documentation needed to serve as 
compliance evidence. The eight-month gap between reviews is a direct 
contributing factor to the Q1 2026 SharePoint permission expansion 
going undetected.

**Follow-up document requested:** Any available output from the last 
permission review, however informal, and the M365 admin center user 
export used during that review.

---

### Finding 2
**Question asked:** When there is a cloud-related incident, what does 
the team do and how quickly is a response initiated?

**What the stakeholder said:** There is no formal cloud incident response 
procedure specific to the Azure or M365 environment. When something goes 
wrong the Cloud Administrator escalates to the IT Manager verbally and 
they decide together how to respond. Response times depend on the 
severity and who is available.

**What existing documentation states:** The Incident Response Policy 
covers general security incidents but does not include a specific 
procedure for cloud environment incidents or defined response time 
requirements for permission or configuration issues.

**Variance identified:** No specific cloud incident response procedure 
exists either in documentation or in practice. The general Incident 
Response Policy does not address cloud-specific scenarios adequately.

**Risk implication:** The absence of a defined cloud incident response 
procedure means response to cloud configuration issues is ad hoc, 
inconsistent, and dependent on individual availability.

**Follow-up document requested:** General Incident Response Policy to 
confirm scope and assess whether cloud-specific scenarios need to be 
incorporated.

---

### Finding 3
**Question asked:** The compliance review in Q1 2026 identified that 
SharePoint permissions had expanded beyond originally intended 
boundaries. When did you first become aware of this and what was your 
response in the first three hours after discovery?

**What the stakeholder said:** The Cloud Administrator became aware of 
the SharePoint permission issue when the compliance team flagged it 
during the Q1 2026 internal review. They had not identified it 
independently prior to that. Upon being notified, they exported the 
current permission structure from SharePoint and identified approximately 
14 folders where permissions had been expanded beyond intended scope. 
In the first three hours they began manually reverting the most sensitive 
folders but did not formally log the incident or notify the CISO until 
the following day.

**What existing documentation states:** The Incident Response Policy 
requires that security incidents be escalated to the CISO within two 
hours of identification.

**Variance identified:** Yes. The CISO was not notified until the 
following day, exceeding the two-hour escalation requirement by 
approximately 22 hours. The incident was also not formally logged at 
the time of discovery.

**Risk implication:** Delayed escalation and failure to formally log 
the incident means the organization's incident record is incomplete 
and the CISO was not able to make informed decisions about containment 
and communication in a timely manner.

**Follow-up document requested:** SharePoint permission export from 
Q1 2026 review and any remediation records showing which folders were 
reverted and when.

### Overall Interview Assessment
This interview surfaced three significant findings across the identity 
and access management and customer data handling scope areas. The most 
critical finding is the combination of infrequent undocumented permission 
reviews and delayed incident escalation. All three findings will be 
carried forward into the current state assessment report.

---

## Interview Log 3: Head of People Operations
**Date of Interview:** 14 March 2026
**Interviewed by:** Omotayo Akinola, GRC Analyst
**Interview Duration:** 45 minutes

### Finding 1
**Question asked:** When an employee is onboarded or offboarded, how 
many hours does it take HR to notify IT about the required change in 
access permissions?

**What the stakeholder said:** HR sends an email notification to the 
IT helpdesk once the employee's exit paperwork has been fully processed 
and signed off. This process typically takes between three and five 
business days after the employee's last working day.

**What existing documentation states:** The HR Offboarding SOP states 
that IT must be notified within 24 hours of an employee's confirmed 
exit date.

**Variance identified:** Yes. There is a significant gap between the 
documented 24-hour notification requirement and the actual three to 
five business day practice. This means former staff accounts may remain 
active for several days beyond their exit date before IT is notified 
to revoke access.

**Risk implication:** Directly supports the Q1 2026 flagged incident 
of former staff accounts remaining active weeks after offboarding. The 
gap originates in the HR notification process, not solely in IT's 
response time.

**Follow-up document requested:** HR exit checklist currently in use, 
to confirm whether IT notification is formally included as a mandatory 
step.

---

### Finding 2
**Question asked:** How does HR confirm that IT has actually acted on 
the notification to revoke access?

**What the stakeholder said:** HR sends the email and assumes IT will 
act on it. There is no formal confirmation step or follow-up check 
from the HR side.

**What existing documentation states:** No confirmation process is 
documented in either the HR Offboarding SOP or the IT Access Management 
Policy.

**Variance identified:** No variance between documentation and practice, 
however both documentation and practice reflect an absent control. There 
is no confirmation loop between HR and IT to verify that access has 
actually been revoked.

**Risk implication:** Even when HR notifies IT promptly, there is no 
mechanism to confirm the notification was received, actioned, or 
completed. A notification sent and ignored would go undetected 
indefinitely.

**Follow-up document requested:** IT helpdesk ticket logs for the last 
six months to check whether offboarding access requests are being 
logged, tracked, and closed within a reasonable timeframe.

---

### Finding 3
**Question asked:** How do you prove that all employees demonstrate 
actual knowledge retention beyond simply completing security training?

**What the stakeholder said:** HR tracks training completion through 
the M365 learning platform and sends reminders to staff who have not 
completed modules. There is no formal assessment or test at the end 
of training. Completion is recorded but retention is not measured.

**What existing documentation states:** The Cybersecurity Awareness 
Policy states that all staff must complete annual security training. 
It does not specify any assessment or knowledge verification requirement.

**Variance identified:** No variance between documentation and practice. 
However both reflect a control gap: completion is tracked but retention 
is not measured, meaning training records alone cannot confirm staff 
actually understood or internalized the content.

**Risk implication:** Security awareness training exists as a preventive 
control but its effectiveness cannot be verified. Staff may complete 
training without genuine knowledge retention, leaving human risk 
exposure higher than training completion rates suggest.

**Follow-up document requested:** Most recent training completion report 
from M365 learning platform, broken down by department.

### Overall Interview Assessment
This interview surfaced three significant findings across identity and 
access management and cybersecurity awareness scope areas. The most 
critical finding is the gap between the documented 24-hour offboarding 
notification requirement and the actual three to five business day 
practice. All three findings will be carried forward into the current 
state assessment report.

---

## Interview Log 4: Data Protection Officer
**Date of Interview:** 16 March 2026
**Interviewed by:** Omotayo Akinola, GRC Analyst
**Interview Duration:** 50 minutes

### Finding 1
**Question asked:** How and when is data classification applied across 
the organization and who is responsible for enforcing it?

**What the stakeholder said:** There is currently no formal data 
classification scheme in operation at Verdant Pay. The DPO has been 
aware of this gap for approximately six months and has drafted a 
proposed classification framework but it has not been formally approved 
or communicated to staff. In practice, staff treat all internal data 
the same way regardless of sensitivity.

**What existing documentation states:** No data classification policy 
currently exists at Verdant Pay. This was confirmed as one of the three 
flagged incidents in the Q1 2026 compliance review.

**Variance identified:** No variance between documentation and practice 
because neither exists. The absence of both policy and practice is 
itself the finding.

**Risk implication:** Without a data classification policy, staff have 
no framework for determining how sensitive customer financial data should 
be stored, shared, or protected. This creates a significant exposure 
under NDPA 2023, which requires organizations to implement appropriate 
technical and organizational measures proportionate to the sensitivity 
of personal data processed.

**Follow-up document requested:** The DPO's draft data classification 
framework, to assess whether it is sufficiently developed to serve as 
the basis for an interim control while formal approval is pursued.

---

### Finding 2
**Question asked:** How do you know and prove that all employees are 
following the acceptable use guidelines in practice?

**What the stakeholder said:** The acceptable use policy exists and was 
distributed to all staff during onboarding. However there is no 
mechanism to monitor compliance with it in practice. The DPO relies 
on staff self-reporting and manager escalation if issues arise. No 
audit of actual data handling practices has been conducted since the 
policy was introduced.

**What existing documentation states:** The Acceptable Use Policy 
requires staff to handle customer data in accordance with its provisions. 
It does not specify a monitoring or enforcement mechanism.

**Variance identified:** No variance between documentation and practice. 
However both reflect an absent control. The policy exists but there is 
no mechanism to verify it is being followed, making it an unenforced 
control.

**Risk implication:** An acceptable use policy with no monitoring or 
enforcement mechanism provides limited actual protection. Staff behaviour 
around customer data handling is effectively unverified, creating a gap 
between stated policy and actual data protection.

**Follow-up document requested:** Current Acceptable Use Policy and 
any staff acknowledgment records held by HR.

---

### Finding 3
**Question asked:** When the compliance team flagged the absence of a 
data classification policy in Q1 2026, what was your assessment of the 
potential regulatory exposure under NDPA 2023?

**What the stakeholder said:** The DPO assessed the regulatory exposure 
as significant. Under NDPA 2023, Verdant Pay as a data controller is 
required to implement appropriate safeguards for personal data 
proportionate to its sensitivity. Without a classification policy, the 
organization cannot demonstrate to the Nigeria Data Protection Commission 
that it understands the sensitivity of the data it processes or that it 
has implemented proportionate controls. In the event of a data breach, 
the absence of a classification policy would likely be treated as an 
aggravating factor in any regulatory investigation.

**What existing documentation states:** NDPA 2023 Section 24 requires 
data controllers to implement appropriate technical and organizational 
measures to ensure data security proportionate to the risk.

**Variance identified:** Not applicable. This finding reflects a 
regulatory gap assessment provided by the DPO rather than a variance 
between documentation and practice.

**Risk implication:** The absence of a data classification policy is 
not merely an internal governance gap. It represents a direct compliance 
exposure under NDPA 2023 that could result in regulatory sanction, 
particularly in the context of a CBN examination or a data breach 
investigation.

**Follow-up document requested:** Any NDPA 2023 compliance assessment 
or gap analysis previously conducted by the DPO.

### Overall Interview Assessment
This interview surfaced three findings across the customer data handling 
scope area. The most significant finding is the complete absence of an 
operational data classification policy despite the DPO having a draft 
framework awaiting approval for six months, suggesting a governance 
process failure around policy approval rather than a knowledge gap. 
All three findings will be carried forward into the current state 
assessment report.

---

## Interview Log 5: Chief Compliance Officer
**Date of Interview:** 17 March 2026
**Interviewed by:** Omotayo Akinola, GRC Analyst
**Interview Duration:** 60 minutes

### Finding 1
**Question asked:** How confident are you personally that Verdant Pay's 
current policies would satisfy a CBN examiner who walked in tomorrow, 
and which policy area concerns you most?

**What the stakeholder said:** The CCO expressed moderate confidence 
overall but identified the data classification and third-party risk 
management policies as the two areas of greatest concern. The data 
classification policy does not exist in an approved form, which is a 
known gap. The third-party risk management policy exists but has not 
been applied consistently, and several vendors providing cloud-adjacent 
services have not been through a formal risk assessment.

**What existing documentation states:** The Governance Policy Framework 
lists data classification and third-party risk management as required 
policies. Neither currently exists in a fully approved and operationally 
active form.

**Variance identified:** Yes. Both policies are listed as requirements 
in the governance framework but neither is fully operational. The gap 
between documented requirements and actual policy existence is a 
governance posture failure.

**Risk implication:** Two of the four key policies required by the 
governance framework are either absent or inactive. This directly 
weakens Verdant Pay's ability to demonstrate a functional compliance 
posture to a CBN examiner and creates specific exposure under the CBN 
Cybersecurity Framework for Payment Service Providers.

**Follow-up document requested:** Current policy register showing 
status, version, and last review date for all active policies.

---

### Finding 2
**Question asked:** Are there any findings from the last CBN examination 
that have not been fully closed yet?

**What the stakeholder said:** Three findings from the last CBN 
examination remain open. The first relates to the absence of a formal 
vendor risk assessment process. The second relates to gaps in the 
incident response plan, specifically around communication protocols 
during a major incident. The third relates to staff cybersecurity 
training, where the examiner noted that completion rates were below the 
required threshold for certain departments. Remediation plans exist for 
all three but progress has been slower than anticipated.

**What existing documentation states:** The CBN examination remediation 
tracker lists all three findings with target closure dates, two of which 
have already passed without full remediation.

**Variance identified:** Yes. Two of the three open findings have 
exceeded their target remediation dates without being closed. This 
represents a compliance commitment that has not been met and creates a 
risk of adverse findings if the same issues appear in the Q4 2026 
examination.

**Risk implication:** Open examination findings that exceed their 
remediation deadlines are a significant regulatory risk. A CBN examiner 
reviewing the same organization in Q4 2026 and finding the same issues 
unresolved is likely to escalate the severity of those findings, 
potentially resulting in formal regulatory action.

**Follow-up document requested:** Full CBN examination remediation 
tracker including current status of all three open findings and 
responsible owners.

---

### Finding 3
**Question asked:** If you could fix one governance gap before Q4 2026, 
what would it be?

**What the stakeholder said:** The CCO identified the third-party risk 
management gap as the single most urgent priority. Several vendors with 
access to or adjacency to Verdant Pay's cloud environment have never 
been formally assessed for security risk. Given that CBN examiners 
increasingly scrutinize third-party risk in fintech environments, and 
given that one of the open examination findings already flags this area, 
the CCO considers it the highest likelihood source of an adverse finding 
in Q4 2026.

**What existing documentation states:** The Third-Party Risk Management 
Policy exists in draft form but has not been formally approved or 
operationalized.

**Variance identified:** Yes. A draft policy exists but is not 
operational, meaning third-party risk assessments are not being 
conducted despite the policy requirement existing in draft form.

**Risk implication:** Vendors with access to cloud systems containing 
customer financial data have not been formally assessed for security 
risk. This creates both a direct security exposure and a compliance 
gap under the CBN Cybersecurity Framework, which requires financial 
institutions to assess and manage third-party risk.

**Follow-up document requested:** Draft Third-Party Risk Management 
Policy and a list of current vendors with access to or adjacency to 
Verdant Pay's cloud environment.

### Overall Interview Assessment
This interview surfaced three findings across the governance and policy 
posture scope area. The most significant finding is the combination of 
two absent or inactive policies and two overdue CBN examination 
remediation commitments, which together paint a picture of a governance 
function that is aware of its gaps but has not been able to close them 
at the required pace. All three findings will be carried forward into 
the current state assessment report.

---

## Interview Log 6: Chief Information Security Officer
**Date of Interview:** 18 March 2026
**Interviewed by:** Omotayo Akinola, GRC Analyst
**Interview Duration:** 60 minutes

### Finding 1
**Question asked:** Of the controls currently in place across all four 
scope areas, which ones are you least confident are operating effectively?

**What the stakeholder said:** The CISO identified three controls with 
the lowest operating confidence. First, the offboarding access 
revocation process, which they acknowledged is dependent on a manual 
notification chain between HR and IT that has proven unreliable. Second, 
the SharePoint permission governance control, which relies on periodic 
manual reviews that are not occurring at the required frequency. Third, 
the cybersecurity awareness training program, which tracks completion 
but does not measure whether staff have actually changed their behaviour 
as a result of training.

**What existing documentation states:** All three controls are 
documented in the Security Controls Register as active and operational.

**Variance identified:** Yes. The Security Controls Register classifies 
all three controls as active and operational, but the CISO's own 
assessment indicates that none of the three are operating with the 
effectiveness the register implies.

**Risk implication:** Controls documented as active and operational that 
are acknowledged internally to be unreliable provide false assurance. 
A risk rating based on the documented control status would underestimate 
actual residual risk across IAM, customer data handling, and 
cybersecurity awareness scope areas.

**Follow-up document requested:** Current Security Controls Register 
and any available control testing or assessment evidence for the three 
identified controls.

---

### Finding 2
**Question asked:** If a CBN examiner walked in tomorrow, which area 
of your security posture would you be most concerned about?

**What the stakeholder said:** The CISO identified identity and access 
management as the area of greatest concern, specifically the combination 
of the offboarding gap, the permission review frequency gap, and the 
absence of a formal privileged access management process. They noted 
that these three issues together create a scenario where the organization 
cannot demonstrate to an examiner that it knows who has access to what, 
whether that access is appropriate, or whether former staff retain any 
residual access.

**What existing documentation states:** The IAM policy documents 
provisioning and deprovisioning requirements but does not include a 
privileged access management procedure.

**Variance identified:** Yes. The absence of a privileged access 
management procedure is a documented gap that has not been remediated. 
The CISO's assessment confirms this gap is known and unresolved.

**Risk implication:** The inability to demonstrate access control 
maturity across provisioning, deprovisioning, permission review, and 
privileged access management is a high-severity finding under the CBN 
Cybersecurity Framework, which specifically requires financial 
institutions to implement and evidence access control processes 
proportionate to their risk exposure.

**Follow-up document requested:** Current IAM policy and any privileged 
access management documentation however informal, including any records 
of privileged account inventories.

### Overall Interview Assessment
This interview surfaced two high-severity findings across the identity 
and access management scope area. The most significant finding is the 
CISO's own acknowledgment that three controls documented as active and 
operational are not functioning at the level the documentation implies. 
All findings will be carried forward into the current state assessment 
report.

---

## Interview Log 7: Senior Product Operations Manager
**Date of Interview:** 19 March 2026
**Interviewed by:** Omotayo Akinola, GRC Analyst
**Interview Duration:** 45 minutes

### Finding 1
**Question asked:** What internal communications, trackers, or shared 
files does your team use that involve customer data outside of officially 
sanctioned systems?

**What the stakeholder said:** The operations team uses a shared 
WhatsApp group to communicate quickly about transaction exceptions and 
escalations during peak processing periods. These messages sometimes 
include customer account references and transaction amounts. The team 
also maintains a manually updated Excel tracker on a shared personal 
OneDrive folder that logs unresolved transaction disputes, which includes 
customer names, account numbers, and transaction details.

**What existing documentation states:** The Acceptable Use Policy 
prohibits the use of personal messaging platforms and personal cloud 
storage for business purposes and explicitly prohibits the sharing of 
customer data outside of approved systems.

**Variance identified:** Yes. Both the WhatsApp group and the personal 
OneDrive tracker represent direct violations of the Acceptable Use 
Policy. Neither has been flagged, reported, or addressed despite the 
policy being in place.

**Risk implication:** Customer personal and financial data is being 
shared through unapproved channels that are outside IT visibility, 
outside security controls, and outside data protection governance. 
This creates a direct NDPA 2023 exposure and a significant customer 
data handling risk that would not be visible to IT, compliance, or 
the CISO without this interview.

**Follow-up document requested:** No document exists for this finding. 
This is a ground-truth finding that only the interview surfaced. The 
finding will be escalated to the CISO and CCO as a priority issue 
following this interview.

---

### Finding 2
**Question asked:** How does the operations team actually behave around 
security practices when under pressure?

**What the stakeholder said:** The operations manager was candid that 
during month-end processing periods, security practices are deprioritized 
in favour of throughput. Staff share login credentials for a shared 
operations dashboard because the individual authentication process is 
considered too slow during peak hours. The manager acknowledged this 
is not ideal but said it is a practical necessity given current system 
limitations.

**What existing documentation states:** The Acceptable Use Policy and 
the IT Access Management Policy both explicitly prohibit credential 
sharing. The IT Access Management Policy requires individual 
authentication for all system access.

**Variance identified:** Yes. Credential sharing is a direct and ongoing 
violation of two separate policies. It is not an isolated incident but 
an established practice during predictable peak periods.

**Risk implication:** Credential sharing eliminates individual 
accountability for system access during peak processing periods. In 
the event of a data breach or unauthorized transaction during those 
periods, it would be impossible to attribute actions to a specific 
individual.

**Follow-up document requested:** Operations dashboard access logs for 
the last three months, to assess whether individual authentication is 
reflected in the logs or whether shared credential use has masked 
individual activity.

---

### Finding 3
**Question asked:** What third-party tools or platforms does the 
operations team use that may not be formally approved by IT or reviewed 
for security?

**What the stakeholder said:** The team uses a free-tier project 
management tool to track internal task assignments and a free document 
conversion tool that staff use to convert customer-facing documents into 
different formats. Neither tool was formally requested through IT or 
reviewed for security. Both were adopted informally because they were 
convenient. The document conversion tool requires uploading files to 
process them, and staff have uploaded internal documents including some 
containing customer reference data.

**What existing documentation states:** The IT Acceptable Use Policy 
requires all third-party tools to be formally reviewed and approved by 
IT before use. The Third-Party Risk Management Policy, though in draft 
form, also requires vendor security assessments.

**Variance identified:** Yes. Both tools are in active use without IT 
approval or security review. The document conversion tool in particular 
processes uploaded files externally, meaning customer reference data 
may have been transmitted to a third-party server outside Verdant Pay's 
control without any security assessment or data processing agreement 
in place.

**Risk implication:** The use of an unapproved external document 
conversion tool that processes files containing customer data creates 
a significant data protection exposure under NDPA 2023, which requires 
data controllers to ensure that any third party processing personal data 
on their behalf has appropriate safeguards in place. No data processing 
agreement exists with this vendor.

**Follow-up document requested:** Names of both tools identified, to 
enable IT to conduct a retrospective security assessment and determine 
whether a data processing agreement is required.

### Overall Interview Assessment
This interview surfaced three high-severity findings across customer 
data handling, identity and access management, and governance posture 
scope areas. All three findings were invisible before this interview. 
None appear in any policy document, IT configuration, or compliance 
record. The WhatsApp data sharing, credential sharing during peak 
periods, and unapproved external tool use represent a category of risk 
that only ground-level operational interviews can surface. All findings 
will be carried forward into the current state assessment report with 
a priority escalation flag.
