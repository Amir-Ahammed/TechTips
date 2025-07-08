# How Microsoft Intune and Entra ID Work Together: A-Z User Lifecycle Example
This guide breaks down how Microsoft **Entra ID** (identity and access control) and **Microsoft Intune** (device and app management) work together to support an employee throughout their entire lifecycle—from onboarding to offboarding.

---

## Meet Amir – New Hire at XYZ Ltd.

Let’s walk through his journey from Day 1 to Exit, powered by Entra ID + Intune automation.

---

## 1. Joiner Phase – New User Onboarding

| Step | Entra ID | Intune |
|------|----------|--------|
| **User Creation** | Account auto-created via HR system or manually in Entra ID | N/A |
| **Group Assignment** | Added to security groups (e.g., "Sales Team") | Triggers Intune app/policy assignments |
| **License Assignment** | M365 & Intune licenses via group-based licensing | Enables enrollment in Intune |
| **MFA & Conditional Access** | Enforces secure login policies (e.g., MFA, location-based access) | Ensures only compliant devices connect |
| **Welcome Workflow** | Sends login credentials & temporary access pass | N/A |

---

## 2. Device Enrollment & Configuration

| Step | Entra ID | Intune |
|------|----------|--------|
| **Device Join** | Device Azure AD Joined (Autopilot or manual) | Auto-enrolled into Intune (MDM) |
| **Policy Enforcement** | N/A | Deploys security policies, device restrictions, compliance rules |
| **App Deployment** | N/A | Pushes required apps (Teams, Outlook, LOB apps) |
| **Compliance Monitoring** | N/A | Tracks device health, patch status, and encryption |

---
## 3. App Access Request – Office 365 or Adobe Licensing

### Scenario: User Requests Access to Microsoft 365 or Adobe

| Step | Entra ID | Intune |
|------|----------|--------|
| **App Request Workflow** | User submits request via internal portal or Self-Service | N/A |
| **Group Membership** | Approved users are added to relevant group (e.g., `O365-License`, `Adobe-Entitlement`) | Group triggers app assignment |
| **License Assignment** | Entra ID applies license via group-based licensing rules | Activates product entitlement (e.g., M365 E3 or Adobe Creative Cloud) |
| **App Installation** | N/A | Intune pushes app package to user device (Office Apps or Adobe Installer via Win32 deployment) |
| **Activation** | User logs in with Entra ID credentials | App activates using assigned license |

> **Example:**  
> Amir requests Adobe Illustrator access → Approved → Added to `Adobe-Creative-Team` group → License is auto-assigned → Intune installs the app silently → Ready to use upon next login.

---

## 3. Mover Phase – Role or Department Change

| Scenario | Entra ID | Intune |
|----------|----------|--------|
| **Role Change** | Updated group membership changes access to apps/files | Deploys new app set & updates policies |
| **Privileged Access** | Uses PIM for elevated access | N/A |
| **Access Reviews** | Periodic group membership & access audits | N/A |
| **Device Monitoring** | N/A | Ensures the device remains compliant |

---

## 4. Leaver Phase – Offboarding

| Step | Entra ID | Intune |
|------|----------|--------|
| **Account Disablement** | Auto-disabled via HRMS sync or manual removal | N/A |
| **Access Revocation** | Group/role removal → loss of access | Compliance policy blocks device |
| **Remote Actions** | N/A | Remote wipe or selective wipe for BYOD |
| **Audit Logging** | Logs identity/access changes | Records device actions and status |

---

## Summary: Why Entra ID + Intune Are Better Together

- ✅ **Zero-touch provisioning** with Autopilot + Entra join
- 🔐 **Secured identity** with conditional access & MFA
- 📦 **Centralized policy & app deployment**
- ⚙️ **Automated role transitions & offboarding**
- 🧾 **Audit-ready for compliance**

> **Tagline:** One identity. One device. Total control.

---
## Access Management with Entra ID + Intune

Managing who gets access to **what**, **when**, and **how** is critical to maintaining a secure IT environment. Here's how access management is handled seamlessly using Entra ID and Intune.

---

### Key Access Control Components

| Component | Entra ID Role | Intune Role |
|-----------|---------------|-------------|
| **Group-Based Access** | Manages access to M365, SaaS apps, files, and systems via security group membership | Deploys apps and config policies based on group membership |
| **Role-Based Access Control (RBAC)** | Grants admin roles (e.g., User Admin, Security Admin) based on least privilege | Assigns scoped admin access to manage specific devices or workloads |
| **Conditional Access (CA)** | Enforces access based on conditions like device state, location, risk level, compliance | Blocks/Allows access only from compliant, managed devices |
| **Privileged Identity Management (PIM)** | Provides just-in-time access to high-privilege roles with audit trails | N/A |
| **Self-Service Access (SSPR & Group Join)** | Users can request or join groups via access packages | Triggers app/license assignment and policy enforcement via group logic |

---

### 🔁 Example: Secure App + Device Access for Fatima

> 🔄 Amir joins the **Design Team**  
> - Added to `DesignTeam-O365` and `AdobeCloud-Users` groups  
> - Gains access to SharePoint, Teams, Photoshop, Illustrator, etc...
> - Conditional Access ensures her laptop is Intune-compliant before allowing access  
> - Office and Adobe apps are installed silently via Intune  
> - Amir requests temporary access to a Power BI report — approved through **PIM**  
> - Access expires automatically after 7 days

---



