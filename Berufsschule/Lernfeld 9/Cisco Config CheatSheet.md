## Wechsel Modi
Startpunkt des Command-Line-Interface ist der User-EXEC-Mode:
```console 
Gerätename>
```
In diesem Modus stehen nur folgende Funktionen zur Verfügung:
+ Nur lesender Zugriff, Überwachungs- und Diagnosebefehle
+ Wechsel in den Privileged-EXEC-Mode

Die nächste Ebene ist der Privileged-EXEC-Mode 
```console
Gerätename#
```
Der Privileged-EXEC-Mode ermöglicht das Ändern von Einstellungen.
Mit dem Befehl
```console
Gerätename#config t
```
wechselt man in den Konfigurationsmodus 

## Übersicht Modi
![[modi_uebersicht_router.png]]
## Nice2Know
Eingabehilfe:
+ Fragezeichen hinter Commands
+ Tab für Autovervollständigung
Bei ---more---:
+ Eingabetaste für eine Zeile vor
+ Leertaste für eine Seite vor
+ Beliebige Taste für Abbruch
**strg+shift+6**  Allzweck-Abbruchsequenz 
Eindeutige befehle kann man auch gekürzt stehen lassen
	config t anstatt configure terminal
Diagnose-Befehle (show-Befehle) im Konfig-Modus beginnen mit einem do


