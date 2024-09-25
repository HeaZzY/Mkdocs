---
title: "Configurations des firewalls"
---

# Configuration des Firewalls

## Firewall SN210

### Interfaces

| Interface    | Mode       | VLAN  | IP Address           | Subnet Mask      |
|--------------|------------|-------|----------------------|------------------|
| **in.1**     | Sub-Interface | 240   | 172.28.172.6         | /24 (255.255.255.0) |
| **in.2**     | Sub-Interface | 244   | 192.168.44.254       | /24 (255.255.255.0) |
| **out**      | Access     | 248   | 192.168.248.10        | /24 (255.255.255.0) |

### Routage

| Destination         | Passerelle          |
|---------------------|---------------------|
| **Par défaut**       | 192.168.248.254     |
| **INTRACHA**         | 192.168.44.10 (FWpnsense) pour 172.28.96.0/24 |
| **INTERCO1-Core-OPNsense** | 192.168.44.10 (FWpnsense) pour 192.168.43.0/24 |

---

## Firewall pfSense

### Interfaces

| Interface    | IP Address         | Subnet Mask          |
|--------------|--------------------|----------------------|
| **LAN 1**    | 192.168.44.10       | /24 (255.255.255.0)  |
| **MANAGEMENT** | 172.28.127.5       | /24 (255.255.255.0)  |
| **WAN**      | 192.168.43.254      | /24 (255.255.255.0)  |

### Routage

| Destination         | Passerelle          |
|---------------------|---------------------|
| **Internet**         | 192.168.44.254 vers 0.0.0.0/0 |
| **Intranet**         | 192.168.43.1 vers 172.28.96.0/19 |
