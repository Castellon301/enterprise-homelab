\# Project Journal



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

