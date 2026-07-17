\# Changelog



\## 2026-07-13



\### Milestone 1 - Foundation



\- Created GitHub repository

\- Installed GitHub Desktop

\- Initialized project documentation

\- Standardized VM naming



\### Milestone 2 - Identity



\- Installed Windows Server 2022

\- Installed VirtIO drivers

\- Configured static networking

\- Installed Active Directory Domain Services

\- Installed DNS

\- Created forest `corp.vpstechnologies.internal`

\- Set NetBIOS name to `VPSTECH`

\- Created Proxmox snapshot `Baseline-ADDS`


## 2026-07-14

### Milestone 3 - Enterprise Identity

Added:

- Organizational Unit hierarchy
- Enterprise user accounts
- Security groups
- Windows 11 workstation joined to the domain
- CLIENT01 moved into the Workstations OU



## 2026-07-17

### Added

- FS01 enterprise file server
- Departmental SMB shares
- NTFS permissions for Engineering and Finance
- RBAC implementation using Active Directory security groups

### Changed

- Replaced inherited local Users permissions with explicit domain security groups.

