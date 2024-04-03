---
tags:
  - "#AP1"
  - "#Lernfeld9"
  - "#Berufsschule"
  - "#Netzwerktechnik"
---

## Dynamic Host Configuration Protocol
DHCP Verteilt IPv4 Adressen an Hosts im Lan. Dabei werden auch Zusatz Informationen weitergegeben z.B.:
* Gateway
* [[DNS]]
* NTP
* ...
Die zu verteilende IPv4 Adresse kommt aus einem Adresspool. Sie wird temporär mit einer einstellbaren Lease-Dauer vergeben.

## Ports
 * 67 UDP IPv4 Server oder Relay-Agent
 * 68 UDP IPv4 Client
 * 547 UDP IPv6 Server oder Relay-Agent
 * 546 UDP IPv6 Client

## Grundablauf
DORA: 
1. **DHCP DISCOVER**
	* Client (Broadcast auf Layer 2): "Hat es einen DHCP-Server?"
2. **DHCP OFFER**
	* Server: "Ich bin einer und hätte die 10.x.y.z für dich."
3. **DHCP REQUEST**
	* Client: "Danke, die hätte ich gerne"
4. **DHCP ACK**
	* Server: "OK, ist eingetragen"

## Rogue DHCP Server
Ist ein von Admin nicht eingerichteter Server der falsche Info rausgibt. 
* falsche Adresse
* falscher Gateway
* Man in the Middle
Abhilfe: 
* DHCP Snooping aktivieren
* DHCP Guard

## DHCP Starvation
Massiv viele "DORA mit Fake-MAC leeren den verfügbaren Adresspool
-> Denial of Service für neue Clients im LAN
Abhilfe:
* Port Security (Anzahl MAC-Adressen pro Port begrenzen)

## IPv6-Adressvergabe
* SLAAC (Stateless Address Auto Configuration)
	-> Präfix aus Router Advertisment, Hostanteil aus EUI64
	-> Hostanteil wird von der eigenen MAC-Adresse abgeleitet
* Es gibt auch DHCPv6