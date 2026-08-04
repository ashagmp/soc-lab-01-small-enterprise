# Network Configuration

## DC01

### Internal Network

| Setting | Value |
|---------|-------|
| Adapter | Ethernet 2 |
| IP Address | 192.168.10.10 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | None |
| Preferred DNS | 192.168.10.10 |

### Notes

- DC01 uses a static IP because it serves as the Domain Controller and DNS server for the `ashag.local` domain.
- Adapter 1 (Ethernet) uses NAT for Internet access.
- Adapter 2 (Ethernet 2) is connected to the internal VirtualBox network (`AshagLab`).