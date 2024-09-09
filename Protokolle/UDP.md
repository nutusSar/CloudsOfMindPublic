---
tags:
  - "#AP1"
  - "#Netzwerktechnik"
  - "#HackingTutorial"
section: "1"
---
## User Datagram Protocol 
Ist ein verbindungsloses Kommunikationsprotokoll, wodurch es sich besonders für zeitkritischen Übertragungen eignet (Streaming, DNS-Abfragen).

## Merkmale
+ Verbindungslos
+ Braucht keinen Handshake
+ Keine konkrete Reihenfolge der Pakete
+ Übertragungsrate höher als bei TCP
## Ablauf
![[Pasted image 20240224110222.png]]
Der Client muss nicht erst eine Verbindung aufbauen, sondern sendet direkt Pakete


## Vor- und Nachteile
| **Vorteile**             | **Nachteile**                                            |
| ------------------------ | -------------------------------------------------------- |
| Geringer Overhead        | Keine Garantie für die Zustellung von Daten              |
| Schnelle Übertragung     | Keine Paketsequenzierung oder Fehlerkorrektur            |
| Einfache Implementierung | Möglicher Datenverlust bei schlechter Netzwerkverbindung |
|                          | UPD-Flood-Attack                                                         |


## Vergleich UDP und TCP
|**Merkmale**|**UDP**|**TCP**|
|---|---|---|
|Verbindungslosigkeit|Ja|Nein|
|Zuverlässige Zustellung|Nein|Ja|
|Paketsequenzierung|Nein|Ja|
|Fehlerkorrektur|Nein|Ja|
|Overhead|Gering|Höher als UDP|
|Geschwindigkeit|Schnell|Abhängig von der Netzwerkbedingungen und -last|
|Einfachheit|Ja|Nein|