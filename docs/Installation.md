# Installation

## Overview

This document records the installation and initial configuration of the virtual machines used in the Ashag Technologies enterprise lab.

## Virtual Machines

| Hostname | Operating System | Role |
|----------|------------------|------|
| DC01 | Windows Server 2022 Standard Evaluation | Domain Controller, DNS Server |
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

## Network

| Host | Internal IP | Role |
|------|-------------|------|
| DC01 | 192.168.10.10 | Domain Controller / DNS Server |

## Notes

- Adapter 1 (NAT) provides Internet access.
- Adapter 2 (AshagLab Internal Network) provides private communication between lab machines.
- DHCP has not yet been configured.
- Client computers have not yet joined the domain.