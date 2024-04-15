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
### Definition
+ Ein Trunkport an jeder Switch, ermöglicht das Kommunizieren der gleichen VLANSs zweier Switches über den gleichen Port
+ Frame wird mit einem VLAN-Tag versehen , welcher zwischen Source Mac und Frame länge kommt.
+ Hat ein Frame kein VLAN-Tag so geht die Switch davon aus, dass es sich um das Standard VLAN handelt.
### 802.1Q
![[Pasted image 20240409114308.png]]
- **TPID**: Tag Protocol Identifier (0x8100)
- **TCI**: Tag Control Information
    - **PCP**: Priority Code Point: Benutzer-Prioritätsinformationen.
    - **DEI**: Drop Eligible Indicator
    - **VID**: VLAN-Identifier, Identifizierung des VLANs, zu dem der Frame gehört.
## Vorteile
+ Günstiger als ein eigenes Netzwerk mit einem Router
+ Broadcastdomainen werden verkleinert -> Mehr Leistung
+ Unabhängigkeit von der physikalischen Topologie
+ Mehr Sicherheit, da die Frames nur noch an die erwünschten Personen gesendet werden

## Switchport modes

- _**Access**_: Permanent Nontrunking, auch wenn der Nachberport dies nicht zustimmt. Es wird trotzdem versucht zu verhandeln, dass der Link zu einem Nontrunk-Link wird.
- _**Trunk**_: Permanent Trunking, auch wenn der Nachberport dies nicht zustimmt. Es wird trotzdem versucht zu verhandeln, dass der Link zu einem Trunk-Link wird.
- **Dynamic Auto**: Ein Port wird zu einem Trunk-Port, wenn der benachbarte Port auf Trunk- oder "dynamic desirable" Modus eingestellt ist. Einige Switchports haben diesen Modus standardmäßig aktiviert.
- **Dynamic Desirable**: VDer Port versucht aktiv den Link zu einem Trunk-Link umzuwandeln. Der Port wird zu einem Trunk-Port, wenn der benachbarte Ethernet-Port auf Trunk-, "dynamic desirable" oder "dynamic auto" Modus eingestellt ist.
- _**No**-**negotiate**_ — Disables DTP. The port will not send out DTP frames or be affected by any incoming DTP frames. If you want to set a trunk between two switches when DTP is disabled, you must manually configure trunking using the (switchport mode trunk) command on both sides.
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
