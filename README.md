# Security & Compliance Engineering

## Overview
This repository documents practical security, compliance, and governance work performed across Microsoft 365 environments. Each entry represents a real implementation of policy, risk mitigation, or platform hardening. The goal is to demonstrate clear engineering decisions, technical execution, and alignment with organizational security requirements.

---

## 1. AI Governance and Data Protection

### Disabled Copilot and Copilot Agents Across Two Tenants  
**Summary:**  
After a security review with leadership and direction from the CTO, Copilot and all Copilot agents were disabled across both managed tenants. The decision was based on uncertainty around how Copilot handles internal data and the organization’s preference to avoid AI‑driven content exposure until the risks are fully understood.

**Key Actions:**  
- Reviewed Copilot agent deployment status in both tenants.  
- Validated security concerns with leadership.  
- Disabled Copilot availability at the tenant level.  
- Removed Copilot service plans from all users.  
- Confirmed that Copilot features no longer appeared in Teams, Outlook, or Microsoft 365 apps.  
- Documented the governance decision and updated internal policy.

**Impact:**  
Ensured that no organizational data could be processed by Copilot services and aligned both tenants with the organization’s AI risk posture.

---

## 2. Email Security and Threat Mitigation

### M365 Quarantine Policy Hardening  
**Summary:**  
Updated Microsoft 365 quarantine policies to prevent end users from previewing, releasing, or deleting quarantined messages. Implemented an administrator‑controlled workflow to reduce phishing exposure and ensure consistent, compliant handling of suspicious emails.

---

## 3. SharePoint Governance and Automation

### Automated Secure Deletion of SharePoint Soft Delete Bin  
**Summary:**  
Developed a PowerShell automation using a dedicated service account and PnP PowerShell to clear a SharePoint site’s soft delete bin every 24 hours. This was implemented to meet stricter document security requirements beyond the default SharePoint retention behavior.

### Operationalized Automation with Task Scheduler  
**Summary:**  
Configured Windows Task Scheduler to run the cleanup script daily using a service account, ensuring consistent enforcement of the secure‑deletion requirement.

---

## 4. Identity, Licensing, and Access Governance

### Hybrid Group‑Based Licensing Architecture  
**Summary:**  
Created on‑premises security groups for Microsoft 365 licensing, synchronized them to Entra ID, and assigned licenses to the groups. Validated the identity flow by adding and removing users on‑premises and confirming license changes in the cloud.

---

## 5. Telemetry and SIEM Integration

### Entra Application for Splunk Integration  
**Summary:**  
Built an Entra application that allows Splunk to securely access Microsoft 365 message trace and audit data. This improved centralized monitoring and strengthened incident response capabilities.

---

## 6. Customer‑Facing Governance Solutions

### Microsoft Bookings Deployment  
**Summary:**  
Collaborated with a customer to design and deploy a Microsoft Bookings solution. Created a shared mailbox, configured delegate permissions, and established a centralized workflow for handling appointment requests.

---

## 7. Deployment of DLP Policies and Sensitivity Labels
**Summary:**  
Tested, configured, and deployed Microsoft 365 Data Loss Prevention policies and Sensitivity Labels across multiple environments. Ensured policies aligned with organizational data-handling requirements and supported secure collaboration.

**Key Actions:**  
- Evaluated existing data flows and risk points.  
- Implemented DLP rules for email, SharePoint, and Teams.  
- Published Sensitivity Labels with appropriate encryption and access controls.  
- Validated policy behavior with test users and real workflows.  
- Provided guidance to staff on proper usage.

**Impact:**  
Strengthened data protection posture and reduced the risk of accidental or unauthorized data exposure.
