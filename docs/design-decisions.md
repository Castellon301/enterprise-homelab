\## Why assign permissions to groups?



Assigning permissions to security groups instead of individual users simplifies administration, reduces errors, and follows Microsoft's AGDLP model.



\# Design Decisions



\---



\## DD-001



\### Active Directory Organizational Units



The Active Directory structure mirrors the organizational departments of VPS Technologies.



Benefits:



\- Easier administration

\- Simplified Group Policy deployment

\- Department-based delegation



\---



\## DD-002



\### Group Policy Separation



Computer policies and user policies are separated into different GPOs.



Computer GPO:



\- Workstation Baseline



User GPO:



\- User Experience



Benefits:



\- Easier troubleshooting

\- Cleaner management

\- Better scalability



\---



\## DD-003



\### Group-Based Permissions



Department folders use Active Directory security groups rather than individual users.



Example:



GG\_Engineering



↓



Engineering Share



Benefits:



\- Simplified administration

\- Better scalability

\- Supports RBAC

\- Follows Microsoft best practices



\---



\## DD-004



\### Principle of Least Privilege



Users receive only the permissions necessary to perform their duties.



Department users receive Modify permissions.



Administrative functions remain restricted to Administrators.

