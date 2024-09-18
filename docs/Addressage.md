---
title: "Addressage du réseau Chartres"
---
# Contexte
Chartres nous avons:<br><br>
La Direction Général<br>
DSI<br>
Système d'information (management)<br>
Juridique<br>
Marketing<br>
Ressource Humaines<br>
SAV

# Addressage
Pour le site de chartres nous avons l'addressage suivante: 172.28.96.0 -> 172.28.127.255<br>

Donc:<br>

Direction Général: 172.28.96.0/24 VLAN 241 <br>
DSI: 172.28.97.0/24 VLAN 242 <br>
Juridique: 172.28.98.0/24 VLAN 243 <br>
Marketing: 172.28.99.0/24V VLAN 244<br>
Ressource Humaines: 172.28.100.0/24 VLAN 245 <br>
SAV: 172.28.101.0/24 VLAN 246 <br>
Management: 172.28.127.0/24 VLAN 240 <br>
WAN: 192.168.248.0/24 VLAN 248 

# Adressage VLAN 240
Adresse du switch coeur de réseau : 172.28.127.1 <br>
Adresse du switch distribution : 172.28.127.2 <br>
Adresse du CHA_RT1 : 172.28.127.3 <br>
Adresse du CHA_RT2 : 172.28.127.4 <br>

Adresse du DC01 : 172.28.127.10 <br>
Adresse du DC02 : 172.28.127.20 <br>
Adresse du serveur linux : 172.28.127.30

# Adressage VLAN WAN

CHA_RT1: 192.168.248.254 IP Publique: 
CHA_RT2: 192.168.248.253 IP publique: 
Switch core: 192.168.248.1





