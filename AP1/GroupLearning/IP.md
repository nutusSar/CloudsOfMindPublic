---
tags:
  - "#AP1"
  - "#Netzwerktechnik"
  - "#HackingTutorial"
---
## IPv4
### Aufbau
+ 32 Bit, 4 Blöcke mit je 8 Bit

#### Private Netzwerke
+ 10.0.0.0 bis 10.255.255.255
+ 172.16.0.0 bis 172.31.255.255
+ 192.168.0.0 bis 192.168.255.255
#### Loopback
+ 127.0.0.0 bis 127.255.255.255 (localhost)
### Klassen VERALTET
![[Pasted image 20240211164820.png]]
### Subnetting
+ Netzwerkmaske gibt den Netzwerk- und Hostanteil einer IPv4 Adresse an
+ Die erste Adresse ist die Netzwerkadresse
+ Die höchste Adresse die Broadcastadresse
+ Hinzufügen von Einsen zur Subnetzmaske ->weniger Hosts pro Netzwerksubnetz, aber mehr Netzwerksubnetze 
+ Einsen aus der Subnetzmaske entfernen -> mehr Hosts pro Netzwerk, aber weniger Netzwerke
![[Pasted image 20240212105008.png]]
**Beispiel:**
+ Netzwerkadresse: 192.168.100.0
+ Broadcastadresse: 192.168.100.255
#### Formeln
+ $$2^n-2 = AnzahlDerHosts$$ (n = Anzahl der Bits des Hostanteils)
+ $$2^n=AnzahlDerSubnetze$$
+ (n = Anzahl der Subnetzbits)
#### Vorgehen anhand eines Beispiels:
![[Pasted image 20240212115406.png]]
Ziel: 64 Subnetze mit je mindestens 1000 Hosts
Welche Subnetzmaske kann 1000 Hosts beinhalten
![[Pasted image 20240212110350.png]]
1. **Mögliche Hosts in Unserem Netzwerk:** 
	![[Pasted image 20240212113921.png]] 
	-> Genügend Hostadressen
2. **Welche Netzmaske bietet ausreichend Hosts:**
	![[Pasted image 20240212114351.png]]
	Anzahl der Hosts >= 1000, $$2^9-2 = 510 < 1000$$ Deswegen n = 10.
3. **Wie viele Subnetze sind mit 1022 Hosts möglich:**
	11111111 . 11111111 . 000000**00 . 00000000** ->Die hinteren 10Bits sind reserviert für Hosts 
	Das heißt 6Bits stehen für Subnetze zur Verfügung:$$2^6=64Subnetze$$
	CIDR = Anzahl der Einsen -> 8 + 8 + 6 = 22
4. **Einteilen der Subnetze:**

| **IP-Adresse mit CIDR** | **Netzwerkadresse** | **Broadcastadresse** | **Erste und letzte Hoastadresse** |
| --- | --- | ---- | --- |
| 158.45.0.0/22           | 158.45.0.0 |  158.45.3.255 | 158.45.0.1 bis 158.45.3.254 |
| 158.45.4.0/22           | 158.45.4.0 |  158.45.7.255 | 158.45.4.1 bis 158.45.7.254  |
| 158.45.8.0/22           | 158.45.8.0 |  158.45.11.255 | 158.45.8.1 bis 158.45.11.254  |
| ...                     | ... | ... | ... |
| 158.45.252.0/22 | 158.45.252.0 |  158.45.255.255 | 158.45.252.1 bis 158.45.255.254  |
## IPv6
### Aufbau
+ 4Mal so lang wie IPv4 -> 128 Bits
+ Darstellung in 4er Hexadezimal Blöcken: 2001:0db8:85a3:08d3:1319:8a2e:0370:7344 -> 1 Block entsprechen 16 Bit
### Kürzen
+ Führende Nullen in einem Block werden weggelassen
+ Die längste Kette von 0er Blöcken darf einmalig mit :: gekürzt werden
**Beispiel:**
+ Ungekürzt: 2001:0DB8:0000:0001:0000:0000:0010:01FF
+ Gekürzt: 2001:DB8:0:1::10:1FF

### Scopes IPv6
![[Pasted image 20240212125349.png]]
Die beiden wichtigsten Scopes sind der Link-Local-Scope und Global-Scope. Nur IPv6-Pakete mit einer globalen Absender-Adresse werden außerhalb des lokalen Netzwerks geroutet. IPv6-Pakete mit link-lokaler Absender-Adresse sind nur innerhalb des lokalen Netzwerks gültig und werden auch nur dann verwendet, wenn das Ziel link-lokal ist.
### Subnetting
+ Ersten 64 Bits Netzwerkanteil, Hinteren 64 Bits Hostanteil
+ Standardmäßig /64 für ein komplettes Netz
![[Pasted image 20240212131511.png]]