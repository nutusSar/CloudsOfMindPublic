---
tags:
  - "#AP1"
  - "#Netzwerktechnik"
---
## Transmission Control Protocol
Definiert, wie Netzwerkkonversationen aufgebaut und aufrecht gehalten werden. Dabei wird eine Verbindung solange aufrecht gehalten, bis beide Seiten die Verbindung beenden.
Durch TCP werden Daten in der richtigen Reihenfolge, verlustsicher, zeitüberwacht und verbindungsorientiert übertragen.

## Merkmale
+ Verbindungsorientiert
+ Benötigt Handshake
+ Übertragungsrate geringer als UDP
+ Korrekte Reihenfolge der Pakete
## Ablauf
1. **Initialisierung**
	Es wird eine Eins-zu-Eins Verbindung aufgebaut. Diese wird während dem gesamten Datenaustausch beibehalten (3-Way-Handshake)
2. **Datenübertragung**
	Es werden Datenblöcke verschickt. Der Empfänger sendet Empfangsbestätigungen, die die Sequenznummer des Datenblockes beinhalten.
	Timer beim Sender überwachen die Sequenznummern der Datenblöcke. 
	Wird die Sequenznummer vor Ablauf des Timers nicht als erhalten bestätigt, so wird der Datenblock erneut gesendet.
	Die Flussteuerung sorgt für einen reibungslosen Ablauf.
3. **Verbindungsabbau**
	Alle Daten wurden übertragen oder ein höheres Protokoll sorgt für die Trennung.

### 3-Way-Handshake
![[Pasted image 20240224102454.png]]
**Erklärung anhand Alice und Bob Beispiels**:
1. Alice schickt Bob einen Terminvorschlag
2. Bob schickt Alice eine Bestätigung des Terminvorschlags inkl. seines Terminvorschlags
3. Alice schickt Bob eine Bestätigung, dass sie Bobs Bestätigung und Terminvorschlag erhalten hat
## Vor- und Nachteile
| **Vorteile**                                                              | **Nachtei**                                                  |
| ------------------------------------------------------------------------- | ------------------------------------------------------------ |
| Datenverlust wird verhindert                                              | Mitsenden der Information wie das Paket zusammengesetzt wird	<br>=> Ineffizient und sehr zeitaufwendig, riesiger Overhead  |
| Garantiert das Daten fehlerfrei und in der richtigen Reihenfolge ankommen |  Es werden Daten erneut gesendet und gewartet bis eine Empfangsbestätigung eintritt                                                              |
| Versenden und Empfangen von Daten gleichzeitig möglich                    | Geringere Datenübertragung als UDP                                                             |
| Datenpakete können einer Anwendung zugeordnet werden                      |                                                              |

## Vergleich TCP und UDP
| **Merkmale** | **TCP** | **UDP** |
| ---- | ---- | ---- |
| Verbindungslosigkeit | Nein | Ja |
| Zuverlässige Zustellung | Ja | Nein |
| Paketsequenzierung | Ja | Nein |
| Fehlerkorrektur | Ja | Nein |
| Overhead | Höher als UDP | Gering |
| Geschwindigkeit | Abhängig von der Netzwerkbedingungen und -last | Schnell |
| Einfachheit | Nein | Ja |
