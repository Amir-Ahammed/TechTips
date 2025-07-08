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

