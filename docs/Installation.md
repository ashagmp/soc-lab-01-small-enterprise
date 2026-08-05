# Installation

## Overview

This document records the installation and initial configuration of the virtual machines used in the Ashag Technologies enterprise lab.

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
- Created and activated the **AshagLab Scope**.
- Verified DHCP client address assignment on **HR-PC01**.

## Network

| Host | Internal IP | Role |
|------|-------------|------|
| DC01 | 192.168.10.10 | Domain Controller / DNS / DHCP |
| HR-PC01 | DHCP (192.168.10.100+) | Domain Client |

## Notes

- Adapter 1 (NAT) provides Internet access.
- Adapter 2 (AshagLab Internal Network) provides private communication between lab machines.
- DC01 provides Active Directory, DNS, and DHCP services for the `ashag.local` domain.
- DHCP is configured and operational.
- HR-PC01 successfully received an IP address from the DHCP server.
- Joined HR-PC01 to the `ashag.local` domain.
- Verified domain authentication using the `whoami` command.
- Verified the computer object was created in Active Directory.
- Created Organizational Units (OUs) for enterprise organization.
- Moved HR-PC01 into the Workstations OU.
- Joined FIN-PC01 to the `ashag.local` domain.
- Verified domain authentication on FIN-PC01 using the `whoami` command.
- Verified the computer object was created in Active Directory.
- Moved FIN-PC01 into the Workstations Organizational Unit.
- Created Organizational Units for enterprise organization.
- Created HR and Finance domain user accounts.
- Created HR_Users and Finance_Users security groups.
- Added users to their respective security groups.