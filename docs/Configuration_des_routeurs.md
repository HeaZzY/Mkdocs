---
title: "Configuration des routeurs"
---

# Configuration des routeurs de chartres

## Addresse VIP
192.168.248.254

## Configurations des interfaces

### Pour CHA_RT1
| Interface               | Encapsulation | IP Address           | Masque de sous-réseau | NAT       |
|-------------------------|---------------|----------------------|-----------------------|-----------|
| GigabitEthernet0/0.1     | dot1Q 240     | 172.28.127.3          | 255.255.255.0         | Non       |
| GigabitEthernet0/0.248   | dot1Q 248     | 192.168.248.253       | 255.255.255.0         | Inside    |
| GigabitEthernet0/1       | N/A           | 183.44.28.1           | 255.255.255.0         | Outside   |




### Pour CHA_RT2

| Interface               | Encapsulation | IP Address           | Masque de sous-réseau | NAT       |
|-------------------------|---------------|----------------------|-----------------------|-----------|
| GigabitEthernet0/0.1     | dot1Q 240     | 172.28.127.4          | 255.255.255.0         | Non       |
| GigabitEthernet0/0.248   | dot1Q 248     | 192.168.248.252       | 255.255.255.0         | Inside       |
| GigabitEthernet0/1       | N/A           | 221.87.128.2          | 255.255.255.0         | Outside       |


## Tables de routage

| Destination     | Masque de sous-réseau | Prochain saut   | Interface            |
|-----------------|-----------------------|-----------------|----------------------|
| 0.0.0.0         | 0.0.0.0               | 183.44.28.2      | GigabitEthernet0/1    |
| 172.28.96.0     | 255.255.224.0          | 192.168.248.10   | GigabitEthernet0/0.248 |



## Configuration du NAT
| NAT ID | Source List         | Interface             | Overload |
|--------|---------------------|-----------------------|----------|
| 1      | access-list 1        | GigabitEthernet0/1    | Oui      |
| 2      | access-list 2        | GigabitEthernet0/1    | Oui      |
| 3      | access-list 3        | GigabitEthernet0/1    | Oui      |
| 4      | access-list 4        | GigabitEthernet0/1    | Oui      |
| 5      | access-list 5        | GigabitEthernet0/1    | Oui      |
| 6      | access-list 6        | GigabitEthernet0/1    | Oui      |
| 7      | access-list 7        | GigabitEthernet0/1    | Oui      |


## Configurations des ACL

| ACL  | Réseau autorisé      | Masque Inversé      |
|------|----------------------|---------------------|
| 1    | 192.168.248.0        | 0.0.0.255           |
| 2    | 172.28.96.0          | 0.0.0.255           |
| 3    | 172.28.97.0          | 0.0.0.255           |
| 4    | 172.28.98.0          | 0.0.0.255           |
| 5    | 172.28.99.0          | 0.0.0.255           |
| 6    | 172.28.100.0         | 0.0.0.255           |
| 7    | 172.28.101.0         | 0.0.0.255           |



