# Core Functions for Identity & Access Management

**1. Manage Access to Microsoft 365 and Cloud Apps**
   - Assign users access to Outlook, Teams, SharePoint, etc.
   - Control access to third-party SaaS apps (like Slack, Salesforce, Zoom) using Single Sign-On (SSO).

📌 Example: You assign Teams access to a new hire and configure SSO for Zoom so they can log in using their work email.

**2. Centralized User Management**
   - Create, modify, or disable user accounts from Azure AD portal or via automation tools (e.g., PowerShell, Logic Apps).

📌 Example: When someone leaves the company, you disable their Azure AD account to cut off access to all apps.

**3. Multi-Factor Authentication (MFA)**
   - Require users to verify their identity using phone or app in addition to a password.

📌 Example: You enable MFA for all admins to prevent account hijacking.

**4. Conditional Access Policies**
   - Block access from outside the country.
   - Allow access only from compliant devices (enrolled in Intune).

📌 Example: A user tries logging in from an unknown country—access is blocked unless they use VPN or company device.

**5. Self-Service Password Reset (SSPR)**
   - Allow users to reset their password without calling IT.
   - You can require verification via phone or email.

📌 Example: A remote employee forgets their password—they reset it from the login screen.

**6. Sign-In Logs and Security Reports**
   - Failed login attempts.
   - Sign-ins from unusual locations/devices.
   - Risky users or sign-ins flagged by Microsoft’s AI.

📌 Example: You get an alert that a user logged in from multiple countries within an hour—investigation needed.

**7. External User Access (Azure AD B2B)**
   - Invite external users (vendors, consultants) to access Teams or SharePoint with their own email address.

📌 Example: A contractor gets temporary access to your internal project team in Microsoft Teams.

**8. Role-Based Access Control (RBAC) & PIM**
   - Assign admin roles (e.g., Intune Admin, User Admin) with limited scope.
   - With Privileged Identity Management (PIM), grant time-bound access to sensitive roles.

📌 Example: You give a junior admin access to manage groups only for the HR department.

**9. App Registration and OAuth Tokens**
   - Register internal or third-party apps to integrate with Azure AD for secure authentication via OAuth/OpenID Connect.

📌 Example: You build a company dashboard that users sign into using their Microsoft 365 login.

**10. Device Registration & Compliance (with Intune)**
   - Enforce that only domain-joined or compliant (encrypted, up-to-date) devices can access company resources.

📌 Example: Block users from accessing files on OneDrive unless the device is encrypted and has antivirus.


