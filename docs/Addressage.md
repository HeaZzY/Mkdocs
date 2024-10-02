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

# VLAN et addressages

Management 240
DMZ Publique 244
DMZ Privée 241
Serveur 242
WAN 248
Interco 243
Service 245 

# Adressage VLAN 240
Adresse du switch coeur de réseau : 10.10.240.1 <br>
Adresse du switch distribution : 10.10.240.2 <br>
Adresse du CHA_RT1 : 10.10.240.3 <br>
Adresse du CHA_RT2 : 10.10.240.4 <br>

Adresse du DC01 : 10.10.240.10 <br>
Adresse du DC02 : 10.10.240.20 <br>
Adresse du serveur http DMZPublique : 10.10.240.30 <br>
Adresse du serveur mariadb DMZPRIV : 10.10.240.40

# Adressage vlan 

Management : 10.10.240.0/24
DMZ Publique 192.168.28.0/24
DMZ Privé 192.168.128.0/24
Serveur : 172.28.97.0/24
Interco : 192.168.43.0/24
WAN : 192.168.248.0/24







