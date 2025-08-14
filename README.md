# CST8919 – DevOps Security & Compliance  

- Student Name: Xihai Ren
- Course: 25S_CST8919_300 DevOps - Security and Compliance
- Professor: Ramy Mohamed
- Due Date: Aug 15, 2025


## Azure, AWS, and GCP Service Comparison

This document lists the Microsoft Azure services covered in CST8919, along with their closest AWS and GCP equivalents.

| **Azure Service** | **AWS Equivalent** | **GCP Equivalent** |
|---|---|---|
| **Microsoft Entra ID** (Azure Active Directory) | **AWS IAM** (Identity and Access Management), AWS SSO (IAM Identity Center) | **Cloud Identity**, **Identity and Access Management (IAM)** |
| **Azure AD B2C** | **Amazon Cognito** | **Firebase Authentication** |
| **Azure Monitor** | **Amazon CloudWatch** | **Cloud Monitoring** (formerly Stackdriver Monitoring) |
| **Log Analytics** (part of Azure Monitor) | **CloudWatch Logs Insights** | **Cloud Logging** + **Cloud Logging Query Builder** |
| **Azure Policy** | **AWS Config** | **Cloud Asset Inventory** + **Organization Policy Service** |
| **Microsoft Defender for Cloud** | **AWS Security Hub** + **Amazon GuardDuty** + **Amazon Inspector** | **Security Command Center** |
| **Microsoft Sentinel** | **Amazon Security Lake** + **Amazon Detective** + **Amazon OpenSearch SIEM solutions** | **Chronicle Security Operations** (formerly Siemplify) + **Cloud Logging & Security Command Center** |
| **Azure Key Vault** | **AWS Secrets Manager** + **AWS KMS (Key Management Service)** | **Secret Manager** + **Cloud KMS** |
| **Azure Logic Apps** | **AWS Step Functions** + **Amazon EventBridge** | **Cloud Workflows** + **Eventarc** |
| **Azure Firewall** | **AWS Network Firewall** | **Google Cloud Firewall** |
| **Network Security Groups (NSG)** | **Security Groups** + **Network ACLs** | **VPC Firewall Rules** |
| **Azure App Service** | **AWS Elastic Beanstalk** | **App Engine** |
| **Azure Resource Manager (ARM)** | **AWS CloudFormation** | **Cloud Deployment Manager** |
| **Azure Blueprints** | **AWS Control Tower** + **Service Catalog** | **Deployment Manager** + **Organization Policy** |


---

## 1. Microsoft Entra ID (Azure Active Directory) / AWS IAM / GCP Cloud Identity
**Overview:**  
Microsoft Entra ID (formerly Azure AD) provides identity and access management with SSO and federated identity. AWS IAM manages users, roles, and policies across AWS accounts. GCP Cloud Identity and IAM handle centralized authentication and role-based access control for GCP resources.

**Core Features:**
- Azure: SSO, MFA, conditional access, B2B/B2C, federation with external IdPs.
- AWS: Fine-grained permissions, SSO, role assumption, MFA.
- GCP: SSO, directory sync, role-based IAM, service accounts.

**Security & Compliance:**  
ISO 27001, SOC 1/2/3, GDPR, FedRAMP.

**Pricing Model:**  
Free tiers with limited features; premium features billed per user/month. AWS IAM included at no cost; AWS SSO costs depend on directory type. GCP Cloud Identity has free and premium tiers.

**Integration for DevSecOps:**  
Integrates with CI/CD pipelines, supports identity-based automation, and secure API access.

---

## 2. Azure AD B2C / Amazon Cognito / Firebase Authentication
**Overview:**  
Customer identity and access management services.

**Core Features:**
- Azure AD B2C: Customizable user flows, MFA, social identity integration.
- Cognito: User pools, identity federation, adaptive authentication.
- Firebase Auth: Simple API integration, social login, anonymous auth.

**Security & Compliance:**  
SOC 2, ISO 27001, GDPR, HIPAA (varies by region).

**Pricing Model:**  
Pay-as-you-go based on MAUs.

**Integration for DevSecOps:**  
Easily integrated into applications with CI/CD and secure login flows.

---

## 3. Azure Monitor & Log Analytics / Amazon CloudWatch / GCP Cloud Monitoring & Logging
**Overview:**  
Cloud-native monitoring and observability services.

**Core Features:**
- Metrics and logs collection
- Alerts and dashboards
- Log query languages (KQL, Insights, Logging Query)

**Security & Compliance:**  
ISO 27001, SOC, GDPR.

**Pricing Model:**  
Charges based on data ingestion, storage, and query execution.

**Integration for DevSecOps:**  
Automated alerting, integration with pipelines, SIEM data feeds.

---

## 4. Azure Policy / AWS Config / GCP Organization Policy
**Overview:**  
Policy-as-code solutions for compliance enforcement.

**Core Features:**
- Define governance rules
- Compliance reporting
- Auto-remediation

**Security & Compliance:**  
CIS, ISO, NIST compliance support.

**Pricing Model:**  
Free or minimal cost; possible charges for evaluation.

**Integration for DevSecOps:**  
Works with IaC templates for pre-deployment compliance checks.

---

## 5. Microsoft Defender for Cloud / AWS Security Hub + GuardDuty + Inspector / GCP Security Command Center
**Overview:**  
Security posture management and workload protection.

**Core Features:**
- Vulnerability scanning
- Threat detection
- Compliance checks

**Security & Compliance:**  
ISO, SOC, FedRAMP, GDPR.

**Pricing Model:**  
Pricing based on protected resources and analysis volume.

**Integration for DevSecOps:**  
Shift-left security, pipeline integration, automated remediation.

---

## 6. Microsoft Sentinel / AWS Security Lake + Detective / GCP Chronicle
**Overview:**  
SIEM/SOAR for multi-source threat detection and response.

**Core Features:**
- Log ingestion
- AI-based analytics
- Automated playbooks

**Security & Compliance:**  
ISO, SOC, FedRAMP, GDPR.

**Pricing Model:**  
Billed per GB ingested/analyzed.

**Integration for DevSecOps:**  
Automated incident response integration.

---

## 7. Azure Key Vault / AWS Secrets Manager / GCP Secret Manager
**Overview:**  
Secrets and key management.

**Core Features:**
- Secure storage for secrets and keys
- Access policies
- Audit logging

**Security & Compliance:**  
FIPS 140-2, ISO, SOC, GDPR.

**Pricing Model:**  
Charged per operation and storage.

**Integration for DevSecOps:**  
Pipeline secret injection, automated key rotation.

---

## 8. Azure Logic Apps / AWS Step Functions / GCP Workflows
**Overview:**  
Workflow automation platforms.

**Core Features:**
- Visual workflow builder
- Event triggers
- API integration

**Security & Compliance:**  
ISO, SOC, GDPR.

**Pricing Model:**  
Pay-per-execution.

**Integration for DevSecOps:**  
Automated remediation, deployment orchestration.

---

## 9. Azure Firewall / AWS Network Firewall / GCP Cloud Firewall
**Overview:**  
Managed firewall services.

**Core Features:**
- Stateful packet inspection
- Rule-based access control
- Threat intelligence feeds

**Security & Compliance:**  
PCI DSS, ISO.

**Pricing Model:**  
Based on throughput and rule count.

**Integration for DevSecOps:**  
Firewall rules as code.

---

## 10. Network Security Groups / AWS Security Groups / GCP VPC Firewall Rules
**Overview:**  
Instance/subnet-level traffic control.

**Core Features:**
- Inbound/outbound rules
- Scoped to subnets or instances

**Security & Compliance:**  
ISO, SOC.

**Pricing Model:**  
No direct charge.

**Integration for DevSecOps:**  
Managed via IaC for consistency.

---

## 11. Azure App Service / AWS Elastic Beanstalk / GCP App Engine
**Overview:**  
PaaS application hosting.

**Core Features:**
- Auto-scaling
- Managed runtime
- Multi-language support

**Security & Compliance:**  
ISO, SOC, PCI DSS.

**Pricing Model:**  
Billed by instance and usage.

**Integration for DevSecOps:**  
Supports CI/CD pipelines.

---

## 12. Azure Resource Manager / AWS CloudFormation / GCP Deployment Manager
**Overview:**  
Infrastructure-as-code management.

**Core Features:**
- Template-based deployments
- Dependency handling

**Security & Compliance:**  
ISO, SOC.

**Pricing Model:**  
Free.

**Integration for DevSecOps:**  
Full automation in pipelines.

---

## 13. Azure Blueprints / AWS Control Tower / GCP Organization Policy + Deployment Manager
**Overview:**  
Governed environment deployment.

**Core Features:**
- Bundled RBAC, policies, templates
- Repeatable environments

**Security & Compliance:**  
Supports CIS, NIST compliance.

**Pricing Model:**  
Free.

**Integration for DevSecOps:**  
Ensures secure, compliant deployments.
