# SOC Lab 01 - Small Enterprise

## Overview

This project simulates the IT infrastructure of **Ashag Technologies**, a fictional company used to build a realistic enterprise environment for SOC and blue team training.

This lab establishes the foundation for future projects involving:

- Active Directory
- DNS
- DHCP
- Windows Server
- Windows 11 Workstations
- Ubuntu Server
- Kali Linux
- Splunk
- Sysmon
- Threat Hunting
- Incident Response

---

## Objectives

- Build a realistic enterprise Active Directory environment.
- Configure Windows and Linux systems.
- Deploy core enterprise services.
- Prepare the infrastructure for future SOC labs.
- Document the environment using professional project documentation.

---

## Environment

| Hostname | Operating System | Role |
|----------|------------------|------|
| DC01 | Windows Server 2022 Standard Evaluation | Domain Controller, DNS Server, DHCP Server |
| HR-PC01 | Windows 11 Pro | HR Workstation |
| FIN-PC01 | Windows 11 Pro | Finance Workstation |
| web01 | Ubuntu Server | Linux Web Server |
| attack01 | Kali Linux | Security Testing Workstation |

---

## Repository Structure

```text
docs/
diagrams/
screenshots/
configs/
```

---

## Current Status

### Completed

- [x] Virtual machines created
- [x] Operating systems installed
- [x] Hostnames configured
- [x] VirtualBox networking configured
- [x] Static IP configured for DC01
- [x] Active Directory Domain Services installed
- [x] DNS Server installed
- [x] DC01 promoted to Domain Controller
- [x] Active Directory forest (`ashag.local`) created
- [x] DHCP Server installed and authorized
- [x] DHCP scope created and activated
- [x] DHCP client connectivity verified
- [x] Join HR-PC01 to the domain
- [X] Create Organizational Units (OUs)

### Remaining

- [ ] Join FIN-PC01 to the domain
- [ ] Create users and security groups
- [ ] Configure Group Policy Objects (GPOs)
- [ ] Configure file shares and NTFS permissions
- [ ] Configure Ubuntu Server
- [ ] Final documentation and architecture diagrams

---

## Documentation

Detailed documentation is available in the `docs/` directory.

---

## License

This project is intended for educational and portfolio purposes.
