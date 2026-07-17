\# NTFS Permissions



\## Purpose



NTFS permissions provide file system authorization for users and groups.



\## Enterprise Design



Engineering

\- GG\_Engineering → Modify



Finance

\- GG\_Finance → Modify



\## Design Decisions



\- Permissions are assigned to Active Directory groups.

\- Individual users are not assigned directly.

\- Least privilege is followed.

\- Department folders use explicit permissions after breaking inheritance.



\## Lessons Learned



\- Inheritance simplifies administration.

\- Explicit permissions provide department isolation.

\- Authentication and authorization are separate concepts.

