## 2026-07-17

### Sprint 5 – Enterprise File Services

#### Completed

- Built FS01.
- Joined FS01 to the domain.
- Installed the File Server role.
- Created departmental SMB shares:
  - Engineering
  - Finance
  - HR
  - IT
  - Public
- Verified access to file shares from CLIENT01.

#### Sprint 6 – Enterprise Authorization

#### Completed

- Learned the difference between Share Permissions and NTFS Permissions.
- Learned how NTFS inheritance works.
- Broke inheritance for department folders.
- Replaced local `Users` permissions with Active Directory security groups.
- Assigned:
  - `GG_Engineering` → Engineering (Modify)
  - `GG_Finance` → Finance (Modify)

#### Lessons Learned

- Authentication answers **who you are**.
- Authorization answers **what you can access**.
- Permissions should be assigned to security groups instead of individual users.
- NTFS permissions and Share permissions work together.
- Inheritance simplifies administration but should be broken when department-specific security is required.
- Group-based access control scales much better than user-based permissions.

#### Next Sprint

- Secure remaining department folders.
- Configure Public share using Authenticated Users.
- Introduce AGDLP.
- Test access with multiple department users.
- Troubleshoot permission conflicts.



# Project Journal

## 2026-07-14

### Sprint 3 - Enterprise Identity

#### Completed

- Created the VPS Technologies Organizational Unit (OU) structure.
- Created department OUs:
  - Executive
  - Information Technology
  - Engineering
  - Finance
  - Human Resources
  - Help Desk
  - Contractors
- Created enterprise security groups:
  - GG_IT_Admins
  - GG_HelpDesk
  - GG_Engineering
  - GG_Finance
  - GG_HR
  - GG_Executives
- Created executive user accounts.
- Created Information Technology user accounts.
- Configured CLIENT01 to use DC01 as its DNS server.
- Successfully joined CLIENT01 to the `corp.vpstechnologies.internal` domain.
- Renamed the workstation to `CLIENT01`.
- Moved the computer object from the default **Computers** container to the **Workstations** Organizational Unit.

#### Lessons Learned

- Active Directory relies heavily on DNS.
- Organizational Units are used to organize objects and apply Group Policy.
- Security groups should be used to assign permissions instead of assigning permissions directly to users.
- Computer objects are automatically created when a workstation joins the domain.
- The default **Computers** container is not intended for long-term management of enterprise workstations.

#### Next Sprint

- Configure administrative accounts.
- Create the first Group Policy Object (GPO).
- Verify Group Policy processing on CLIENT01.
- Begin building enterprise workstation management.



\## 2026-07-13



\### Completed

\- Created the GitHub repository for the VPS Technologies enterprise home lab.

\- Installed GitHub Desktop and cloned the repository locally.

\- Created the initial documentation structure.

\- Deployed Proxmox VE on the Dell OptiPlex 7070.

\- Configured TrueNAS with direct disk passthrough.

\- Built DC01 as a Windows Server 2022 VM.

\- Installed VirtIO drivers and QEMU Guest Agent.

\- Resolved a duplicate IP conflict during static network configuration.

\- Assigned DC01 the static IP address 192.168.4.221.

\- Installed Active Directory Domain Services and DNS.

\- Promoted DC01 to the first domain controller in the new forest.

\- Created the Active Directory forest `corp.vpstechnologies.internal`.

\- Set the NetBIOS domain name to `VPSTECH`.

\- Created the Proxmox snapshot `Baseline-ADDS`.



\### Notes

\- DC01 is now the foundation for the VPS Technologies identity infrastructure.

\- Static IPs are required for domain controllers.

\- DNS is hosted on DC01.



\### Next Steps

\- Create Organizational Units in Active Directory.

\- Create security groups and user accounts.

\- Join CLIENT01 to the domain.

\- Document the environment architecture in GitHub.









