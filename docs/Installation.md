# Installation

## Overview

This document records the installation and configuration of the virtual machines used in the Ashag Technologies enterprise lab.

## Virtual Machines

| Hostname | Operating System | Role |
|----------|------------------|------|
| DC01 | Windows Server 2022 Standard Evaluation | Domain Controller, DNS Server, DHCP Server |
| HR-PC01 | Windows 11 Pro | HR Workstation |
| FIN-PC01 | Windows 11 Pro | Finance Workstation |
| web01 | Ubuntu Server | Linux Web Server |
| attack01 | Kali Linux | Security Testing Workstation |

## Completed Tasks

- Installed all virtual machines.
- Configured hostnames according to the enterprise naming standard.
- Configured VirtualBox networking (NAT + Internal Network).
- Assigned a static IP address to DC01.
- Installed Active Directory Domain Services (AD DS).
- Promoted DC01 to the first Domain Controller.
- Created the `ashag.local` Active Directory forest.
- Installed and configured the DNS Server role.
- Installed and configured the DHCP Server role.
- Created and activated the **AshagLab** DHCP scope.
- Verified DHCP client address assignment.
- Joined **HR-PC01** to the `ashag.local` domain.
- Joined **FIN-PC01** to the `ashag.local` domain.
- Verified domain authentication using the `whoami` command.
- Verified computer objects were created in Active Directory.
- Created Organizational Units (OUs).
- Moved domain workstations into the **Workstations** OU.
- Created **HR** and **Finance** domain user accounts.
- Created **HR_Users** and **Finance_Users** security groups.
- Added users to their respective security groups.
- Created departmental shared folders.
- Configured NTFS permissions using Active Directory security groups.
- Configured SMB share permissions.
- Verified authorized access to departmental shares.
- Verified unauthorized access was denied.
- Configured the Default Domain Policy password policy.
- Configured the Default Domain Policy account lockout policy.
- Verified Group Policy application on domain-joined workstations.
- Configured a static IP address for the Ubuntu Server (`web01`).
- Configured DNS to use the domain controller (`192.168.10.10`).
- Verified network connectivity to the domain controller.
- Installed and configured the OpenSSH Server.
- Installed and configured the Apache Web Server.
- Verified web server access from a Windows client.
- Ubuntu Server (`web01`) is configured with a static IP address and provides web services for future SOC monitoring labs.
## Network

| Host | Internal IP | Role |
|------|-------------|------|
| DC01 | 192.168.10.10 | Domain Controller / DNS / DHCP |
| HR-PC01 | DHCP (192.168.10.100+) | Domain Client |
| FIN-PC01 | DHCP (192.168.10.100+) | Domain Client |
| web01    | 192.168.10.20          | Ubuntu Web Server|

## Notes

- Adapter 1 (NAT) provides Internet access.
- Adapter 2 (AshagLab Internal Network) provides private communication between lab machines.
- DC01 provides Active Directory, DNS, and DHCP services for the `ashag.local` domain.
- Domain-joined clients receive IP addresses automatically from the DHCP server.
- Group Policy is centrally managed through the Default Domain Policy.
- Departmental file access is controlled using Active Directory security groups and NTFS permissions.