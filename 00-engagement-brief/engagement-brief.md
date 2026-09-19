# Paraclete
## Engagement Brief
**Confidential | Internal Use Only**

## Client Overview

Paraclete Limited is a Lagos-based fintech company operating a cloud-native digital payments platform that enables peer-to-peer transfers, bill payments, and merchant collections across Nigeria. Founded in 2019, the company has grown to approximately 120 staff across product, engineering, operations, compliance, and customer support functions. Its customer base stands at roughly 340,000 active users, with transaction volumes averaging NGN 2.1 billion monthly.

Paraclete operates entirely on cloud infrastructure, primarily Microsoft Azure for core workloads and Microsoft 365 for internal collaboration, communication, and document management. It holds a Payment Service Solution Provider (PSSP) licence issued by the Central Bank of Nigeria (CBN) and is therefore subject to the CBN Cybersecurity Framework for Payment Service Providers, the Nigeria Data Protection Act 2023 (NDPA), and PCI-DSS requirements relevant to card transaction handling.

## Engagement Context

In Q1 2026, Paraclete's compliance team flagged three concerns during a routine internal review: several former staff accounts remained active in the M365 environment weeks after offboarding, cloud storage permissions on SharePoint had expanded beyond originally intended boundaries, and no formal data classification policy existed to govern how sensitive customer financial data was being handled internally.

These findings were escalated to the board, which authorized an internal cyber risk assessment to establish a clear picture of the organization's current risk posture ahead of a planned Series B fundraising round and a CBN regulatory examination expected in Q4 2026. The assessment is being conducted by the internal GRC team.

## Scope of Assessment

The assessment covers four defined areas:

Identity and access management across the M365 environment, including user provisioning, offboarding controls, privileged access, and conditional access policies.

Customer data handling, covering how personally identifiable financial data is stored, classified, accessed, and shared internally across cloud systems.

Cybersecurity awareness and human risk, examining staff training coverage, phishing susceptibility indicators, and behavioral practices around data handling.

Governance and policy posture, reviewing the existence, currency, and operational effectiveness of key policies including acceptable use, data classification, incident response, and third-party risk management.

Physical infrastructure, on-premises hardware, and consumer-facing application security fall outside the current scope of this engagement.

## Key Stakeholders

The following roles have been identified as primary contacts for the assessment through a structured stakeholder identification process that followed the four scope areas, the three flagged incidents, decision authority, and data flow across the organization.

The Head of IT Infrastructure is responsible for M365 administration, Azure environment configuration, privileged access management, and day-to-day technical operations. They hold direct visibility into how access is provisioned, reviewed, and configured across the M365 environment.

The Cloud Administrator is responsible for managing cloud platform configurations, SharePoint permissions, and Azure storage environments. They hold ground-truth technical visibility into how customer data is stored, who can access it, and whether current configurations match intended design.

The Head of People Operations is responsible for staff onboarding, offboarding, HR data management, training administration, and policy acknowledgment records. They own the employee lifecycle process that directly connects to identity and access management, cybersecurity awareness, and governance posture.

The Data Protection Officer is responsible for ensuring Paraclete's handling of customer personal data complies with the Nigeria Data Protection Act 2023 and related obligations. They hold regulatory correspondence, breach notification history, consent mechanisms, and data classification policy.

The Chief Compliance Officer owns the regulatory relationship with CBN, oversees internal policy currency and review cycles, and holds examination history including prior findings and open remediation commitments. They are the primary stakeholder for governance and policy posture and examination readiness.

The Chief Information Security Officer owns Paraclete's overall security strategy, control design decisions, risk tolerance, and incident response capability. They hold visibility into known security gaps, control effectiveness across all four scope areas, and the organization's defined risk appetite.

The Senior Product Operations Manager represents how business teams interact with internal systems day to day. They hold ground-truth visibility into operational reality including workarounds, informal practices, and shadow IT that no policy document, configuration review, or technical scan would surface.

## Assessment Objective

The objective of this engagement is to produce a structured, evidence-based cyber risk register that reflects Paraclete's actual risk exposure across the four scope areas, supports prioritized remediation planning, and provides a credible governance artifact ahead of both the Series B process and the CBN examination.
