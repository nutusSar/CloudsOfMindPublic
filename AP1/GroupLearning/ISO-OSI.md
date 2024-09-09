---
tags:
  - "#AP1"
  - "#Netzwerktechnik"
  - "#HackingTutorial"
topic: Übersicht
section: "1"
---

## Übersicht
| **Nummer** | **OSI-Schicht**               | **TCP/IP-Modell** | **Verschickte Einheiten**     | **Protokollbeispiele**                       | **Kopplungselemente**                  |
| ---------- | ----------------------------- | ----------------- | ----------------------------- | -------------------------------------------- | -------------------------------------- |
| 7          | Anwendung<br>Application      | Anwendung         | Daten                         | HTTP,<br>FTP,<br>SMTP,<br>[[DNS]],<br>[[DHCP]],<br>Telnet | Gateway,<br>Proxy,<br>Layer-4-7-Switch |
| 6          | Darstellung<br>Presentation   | wie oben          | wie oben                      | wie oben                                     | wie oben                               |
| 5          | Sitzung<br>Session            | wie oben          | wie oben                      | wie oben                                     | wie oben                               |
| 4          | Transport<br>Transport        | Transport         | TCP: Segmente UDP: Datagramme | [[TCP]],<br>[[UDP]]                          | wie oben                               |
| 3          | Vermittlung-/Paket<br>Network | Internet          | Pakete                        | IP,<br>ICMP,<br>IPsec                        | Router                                 |
| 2          | Sicherung<br>Data Link        | Netzzugriff       | Frames                        | Ethernet,<br>WLAN,<br>MAC                    | Switch,<br>Bridge,<br>Access Point     |
| 1          | Bitübertragung<br>Physical    | wie oben          | Bits                          | Token Ring                                   | Kabel,<br>Hub,<br>Repeater             |
## Merksätze
**P**lease **D**o **N**ot **T**hrow **S**alami **P**izza **A**way (Von unten nach oben, englisch)
**A**lle **D**eutschen **S**tudenten **T**rinken **V**erschiedene **S**orten **B**ier (Von oben nach unten, deutsch)
## Netzwerkkomponenten
|**Komponenten**|**Funktion**|**Schicht im OSI-Modell**|**Protokollbeispiele**|
|---|---|---|---|
|Hub|– Ähnlich wie ein Switch  <br>– Verteilt Netzwerkverkehr an alle Ports  <br>– Bietet eine Kollisionserkennung  <br>– Sterntopologie|Schicht 1: Bitübertragungsschicht|–|
|Switch|– Sterntopologie  <br>– Netzwerkverkehr wird nur an seinen Zielteilnehmer geleitet|Schicht 2: Sicherungsschicht|Ethernet|
|Bridge|– Verbindet Netzwerke miteinander  <br>– Auch Netze mit unterschiedlicher Topologie|Schicht 2: Sicherungsschicht|Ethernet|
|Access Point|– Ermöglicht den Zugang zu einem Netzwerk für drahtlose Geräte|Schicht 2: Sicherungsschicht|WiFi (IEEE 802.11)|
|Router|– Routet Datenpakete zwischen verschiedenen Netzwerken  <br>– Erstellt Wegetabellen  <br>– Vermittelt zwischen Netzwerktypen (z.B. DSL & Ethernet)|Schicht 3: Vermittlungsschicht|RIP,<br>BGP<br> |
