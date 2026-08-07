# Network Configuration

## DC01

### Network Adapters

| Adapter | Purpose | Configuration |
|---------|---------|---------------|
| Ethernet | NAT | DHCP (Internet Access) |
| Ethernet 2 | AshagLab Internal Network | Static |

### Internal Network Configuration

| Setting | Value |
|---------|-------|
| IP Address | 192.168.10.10 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | None |
| Preferred DNS | 192.168.10.10 |

### DHCP Configuration

| Setting | Value |
|---------|-------|
| Scope Name | AshagLab Scope |
| Address Range | 192.168.10.100 - 192.168.10.200 |
| Subnet Mask | 255.255.255.0 |
| Lease Duration | 8 Days |
| DNS Server | 192.168.10.10 |
| Domain Name | ashag.local |

### Linux Server

| Host | IP Address | DNS | Purpose |
|------|------------|-----|---------|
| web01 | 192.168.10.20 | 192.168.10.10 | Ubuntu Web Server |

### Notes

- DC01 uses a static IP because it serves as the Domain Controller, DNS Server, and DHCP Server.
- Adapter 1 (Ethernet) uses NAT for Internet access.
- Adapter 2 (Ethernet 2) is connected to the VirtualBox internal network (`AshagLab`).
- DHCP automatically assigns IP addresses to client computers in the `192.168.10.100-192.168.10.200` range.
- Clients use DC01 (`192.168.10.10`) as their DNS server to locate Active Directory services.
