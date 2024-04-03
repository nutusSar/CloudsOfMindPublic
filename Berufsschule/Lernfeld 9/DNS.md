---
tags:
  - "#Lernfeld9"
  - "#AP1"
  - "#Berufsschule"
  - "#Netzwerktechnik"
---
## Dynamic Naming System

Das Domain Name System ordnet lesbare / merkbare Namen bzw. Adressen (google.com) zu IPs zu. DNS ist ein weltweites, hierarchisches System mit Delegation.
* . :Root-Zone
* de : Top-Level-Domain
* Koblenz : Second-Level-Domain
* Bildung : Subdomain
* Moodle : Hostname

## Ports
* 53 TCP/UDP
* 853 TCP nur mit TLS (RFC 7858)
* 853 UDP nur mit DTLS (RFC 8094)

## Resource Records
DNS hat mehrere Resource Records (DNS-RR), welche dazu dienen bei Abfragen an den DNS anzugeben, was man genau möchte.
* Type A ("Address"): IPv4-Adresse
* Type PTR (Pointer): Reverse DNS
* Type AAAA: IPv6-Adresse (4* so groß wie IPv4)
* Type MX (Mail Exchange): Mailserver
* Type NS (Nameserver): DNS-Server
* Type SOA (Start of Authority): Zuständigkeit
* Type TXT: Kommentare etc.
* Type TLSA ("TLS Authority"): Zertifikatsvalidierung
Diese kann man in der CMD anwenden, indem man zunächst 
```console
C:\Users\Mein Computer> nslookup
```
öffnet. Dann kann man mit
```console
> set type=<type>
```
den gewünschten Typen des Records eingeben, wonach man die gewünschte Domain eingeben kann und das Ergebnis erhält.

## Beispiel
* IPv4 von moodle.bildung.koblenz.de:
	```console
	Name: moodle.bildung.koblenz.de
	Address: 82.115.104.42
	```
* IPv6 von google.de:
	```console
	Name google.de
	Adress: 2a00:1450:4001:81c::200e
	```
* Mailserver von gibip.de:
	```console
	gibip.de        MX prefernce = 10, mail exchanger = mx.mpma.de
	```
* Kommentar von gibip.de:
	```console
	“v=spf1 mx ip4:94.130.176.143 ip6:2a01:4f8:c0c:a39a::1 -all” gibip.de text =“Hallo      BSIT22c!”
	```

## Root Zone
Die Root-Zone wird von 13 Root-Nameservern bedient, a-root-servers.net bis m.root-servers.net
```console
C:\Users\Mein Computer> nslookup
> set type=NS
> .
(root) nameserver = a.root-servers.net
	...
(root) nameserver = m.root-servers.net
```
Zur Vermeidung von Ausfällen sind diese 13 Adressen sogenannte "Anycast-Adressen". Es gibt in Wahrheit also deutlich mehr als 13 Root-Server.

## Reverse DNS
Für den Reverse lookup gibt es einen eigenen Resource Record "PTR-Record".
Beispiel 10.7.4.2 hat einen PTR-Eintrag in der Domain 2.4.7.10.in-addr.arpa.
```console
C:\Users\Mein Computer> nslookup
> set type=PTR
> 2.4.7.10.in-addr.arpa.
2.4.7.10.in-addr.arpa    name = localhost
```
Bei IPv6 ist die Reverse-Zone ip6.arpa.

## DNS vs. DNS-Ressolver
Man unterscheidet zwischen echten DNS-Servern und DNS-Resolvern
* **Server**:
	Zuständig für eine oder mehrere Zonen. Erhält die Zuständigkeit durch Delegation (SOA/NS-Record).
* **Resolver**:
	Nimmt Clients die Arbeit ab
	->Rekursiver Durchlauf aller Zonen
	z.B.: moodle.bildung.koblennz.de
	1) Frage Root-Server nach Zone de
	2) Frage de-Server nach Zone koblenz.de
	3) Frage koblenz.de-Server nach Zone bildung.koblenz.de
	4) Frage bildung.koblenz.de-Server nach A-Record für moodle.bildung.koblenz.de
	=> Rekursive Nameserver-Abfrage 
	
Bekannte öffentliche Resolver:
* Google: 8.8.8.8, 8.8.4.4
* Cloud Flare: 1.1.1.1, 1.1.2.2
* Andere: 9.9.9.9

Pi-Hole als Resolver z.B. als Adblocker

## Aufbau eines Records
Eine DNS-Zone ist in einer Zonendatei hinterlegt
Beispiel für eine Zonendatei der Domain gibip.de:
```
gibip.de. 3600 IN SOA ns.inwx.de. hostmaster....

@ 1800 IN NS ns2.inwx.eu.

www.gibip.de. 300 IN A 34.56.100.201

www 300 IN AAAA 2001:6f8:128d::1

@ 300 IN MX 5 mx.mpma.de

@ 300 IN TXT "Dies ist ein Kommentar"
```
@ ist hier ein Platzhalter und ist Gleichgültig mit:
* gibip.de.
* www.gibip.de.
* www
Dies gilt nur solange der Punkt hinter de ist!!!
Der allgemeine Aufbau ist:
Zone---TTL---Internet---ResoruceRecordTyp---Daten
```
example.com. 1800  IN  SOA  ns1.example.com. mailbox.example.com. (
                                                100   ; Seriennummer
                                                300   ; Refresh Time
                                                100   ; Retry Time
                                                6000  ; Expire Time
                                                600   ; negative Caching Zeit
                                               )
example.com. 1800  IN  NS   ns1.example.com.
```


