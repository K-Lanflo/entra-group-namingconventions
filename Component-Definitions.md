# Entra ID Naming Convention Components and Definitions

#### Exemple: `SGR-USR-Entra-PIM-CloudAdmins`
#### `(Group Type)-(Assignment Type)-(Service Name)-(Sub-Service Name)-(Descriptive Group Name)`

#

### Group Type (2-3 characters)
The first component identifies the category of group and who can manage membership.

| Code | Type | Usage | Notes |
| --- | --- | --- | --- |
| SGR | Security Group | For granting access to resources and assigning permissions | Most common; managed by IT and group owners |
| DGR | Distribution Group | For sending emails to multiple recipients | Typically managed by communications teams |
| MGR | Microsoft 365 Group | For collaboration including email, calendar, and document sharing | Self-service group creation encouraged for teams |
| DYN | Dynamic Group | Membership automatically updated based on user attributes | Managed by IT; requires careful rule configuration |


Example: The first part of `SGR-USR-Entra-PIM-CloudAdmins` is `SGR`, indicating this is a security group.
#

### Assignment Type (2-3 characters)
This component describes how access is assigned or who can access the resource.

| Code | Assignment Type | Usage | Notes |
| --- | --- | --- | --- |
| USR | User-based | Groups containing individual users | Most straightforward assignment method |
| DEV | Device-based | Groups containing devices | Most straightforward assignment method |
| GRP | Group-based | Groups that contain other groups for hierarchical management | Used for complex permission structures |
| SVC | Service-based | Groups for service accounts and automated processes | Restricted; requires elevated approval |
| ROL | Role-based | Groups assigned based on job roles or organizational titles | Often paired with dynamic membership rules |
| LOC | Location-based | Groups based on geographic location or office location | Used for regional resource access |
| DEP | Department-based | Groups specific to departments or business units | Enables cross-functional collaboration |

Example: The second part of `SGR-USR-Entra-PIM-CloudAdmins` is `USR`, indicating this group contains individual users.

#

### Service Name (2-5 characters)
The service name identifies the primary Microsoft 365, Azure, or business application that the group supports.

| Code | Service | Purpose |
| --- | --- | --- |
| Entra | Microsoft Entra ID | Identity and access management |
| M365 | Microsoft 365 | General Microsoft 365 services |
| Teams | Microsoft Teams | Teams collaboration platform |
| Share | SharePoint Online | Document management and collaboration |
| Exch | Exchange Online | Email and calendar services |
| Intune | Microsoft Intune | Device management and compliance |
| Defender | Microsoft Defender | Security threat protection |
| Sentinel | Microsoft Sentinel | Security information and event management |
| Power | Power Platform | Power Automate, Power Apps, Power BI |
| DataLake | Data Lake | Data storage and analytics |

Example: The third part of `SGR-USR-Entra-PIM-CloudAdmins` is `Entra`, identifying this group manages Entra ID access.

#

### Sub-Service Name (2-5 characters)
This component specifies a particular feature, module, or subset of the primary service.

| Code | Sub-Service | Usage |
| --- | --- | --- |
| PIM | Privileged Identity Management | Temporary elevated access; requires approval |
| MFA | Multi-Factor Authentication | Authentication management and enforcement |
| CAP | Conditional Access Policies | Policy creation and management |
| Guest | Guest Access Management | External user access controls |
| Device | Device Management | Intune device enrollment and compliance |
| Incidents | Incident Management | Sentinel incident investigation and response |
| Analytics | Analytics and Reporting | Data analysis and business intelligence |
| Collab | Collaboration | Teams, SharePoint, and group collaboration |
| Reports | Reporting | Access to reporting and audit logs |
| Onboard | Onboarding | New user and device setup processes |

Example: The fourth part of `SGR-USR-Entra-PIM-CloudAdmins` is `PIM`, indicating the group manages Privileged Identity Management features.

#

### Descriptive Group Name (Variable, 1-4 words)
The final component uses clear, business-friendly language to describe the specific function or role of group members.

Guidelines:

- Use PascalCase (capitalize first letter of each word)
- Keep it concise but meaningful
- Avoid abbreviations unless universally recognized
- Describe the access level or responsibility

Common Descriptors:

- Admin/Admins – Full administrative control
- Owner – Resource owners with management rights
- Manager/Managers – Supervisory or managerial access
- Member/Members – Standard user access
- Viewer/Viewers – Read-only access
- Operator – Operational/support access
- Approver/Approvers – Access approval authority
- Auditor/Auditors – Audit and compliance access

Example: The fifth part of 'SGR-USR-Entra-PIM-CloudAdmins' is CloudAdmins, indicating the group contains cloud administrators.
