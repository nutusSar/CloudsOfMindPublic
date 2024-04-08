---
tags:
  - "#AP1"
  - "#Netzwerktechnik"
  - "#Berufsschule"
  - "#Lernfeld9"
---
## Definition
+ **V**irtual **L**ocal **A**rea **N**etwork
+ Aufteilen eines Netzwerkes in sepperrate Einheiten
+ Logische Verbindung
+ Kann auf Switchen realisiert werden.
VLANs (Virtuelle LANs) teilen einen Switch per Konfiguration in mehrere virtuelle Switches
VLANs sind in IEEE 802.1Q spezifiziert.

## Funktionsweise
### Portbasiertes VLAN
+ Zuweisen der einzelnen Port zu unterschiedlichen VLANs
+ VLANs werden mit einer VLAN-ID durchnummeriert (Standard-ID: 1)
+ Verfügbare IDs 1 - 4094 (0 und 4095 sind reserviert)
Vor das EtherType-Feld wird ein Tag eingesetzt
![[Pasted image 20240304125434.png]]

## VLAN-Trunking
+ Ein Trunkport an jeder Switch, ermöglicht das Kommunizieren der gleichen VLANSs zweier Switches über den gleichen Port
+ Frame wird mit einem VLAN-Tag versehen , welcher zwischen Source Mac und Frame länge kommt.
+ Hat ein Frame kein VLAN-Tag so geht die Switch davon aus, dass es sich um das Standard VLAN handelt.

## Vorteile
+ Günstiger als ein eigenes Netzwerk mit einem Router
+ Broadcastdomainen werden verkleinert -> Mehr Leistung
+ Unabhängigkeit von der physikalischen Topologie
+ Mehr Sicherheit, da die Frames nur noch an die erwünschten Personen gesendet werden


## Über die CLI einrichten
### VLAN zwischen zwei Switches
#### VLAN erstellen
```
Switch(config)# vlan 10 
Switch(config-vlan)# name Verwaltung
```

#### VLAN löschen
```
Switch(config)# no vlan 10
```

#### Alle VLANs löschen
```
Switch# delete flash:vln.dat
Switch# reload
```

#### Port zu VLAN zuweisen (access)
```
Switch(config)# interface Fa0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10
```

#### Port zurück zu VLAN1
```
Switch(config-if) no switchport access vlan
```

#### Trunk-Port
```
Switch(config)# interface Fa0/1
Switch(config-if)# switchport mode trunk
Switch(config-if)# switchport trunk native vlan 99
Switch(config-if)# switchport trunk allowed vlan 20,30,40
```

#### Diagnose
```
Switch# show vlan
```
+ VLANs, Status, Portzuweisung

```
Switch# show interfaces vlan 20
```
+ up

```
Switch# show interfaces Fa0/1 switch
```
+ VLAN Zuordnung, Trunk, ...

### Trunk-Port auf Cisco-Router (Router-on-a-stick)
```
Router(config)# interface G0/1
Router(config-if)# no shutdown

Router(config-if)# interface G0/1.10
Router(config-subif)# encapsulation dot1q 10
Router(config-subif)# ip address 192.168.10.1 255.255.255.0
```

### Nice2Know
#### Mehrere Interfaces auf einmal konfigurieren
```
Switch(config)# interface range fa0/1 - 10
```
