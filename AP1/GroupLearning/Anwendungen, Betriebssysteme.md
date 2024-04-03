---
tags:
  - "#AP1"
  - "#Netzwerktechnik"
topic: Funktionsweise PC
---
## Definition
![[Pasted image 20240208094830.png]]
## Aufgaben
+ Logik der Dateiverwaltung 
+ Speicherverwaltung (z.B. laden von Daten in den RAM)
+ Prozessverwaltung (Alle verfügbaren Ressourcen des PCs müssen verteilt werden)
+ Ein- / Ausgabe (Unterstützung und Steuerung von Peripheriegeräten)
+ Sicherheit
+ Bereitstellung der Benutzeroberfläche
+ Steuerung und Abstraktion der Hardware

## Schalenmodell
![[Pasted image 20240208094228.png]]

## Kernel
**Schnittstelle zu den Anwenderprogrammen**
+ Kontrolliert den Zugriff auf Hardware (Prozessor, Speicher, ...)
+ Stellt die notwendigen Betriebsmittel zur Verfügung
### Arten von Kernel
#### Monolithischer Kernel
![[Pasted image 20240208101621.png]]
![[Pasted image 20240208101817.png]]
+ Alle Treiber sind teil des Kernels
**Vorteile**:
+ Geringe Umschaltzeiten zischen den einzelnen Modulen
**Nachteile:**
+ Bei einer neuen Version muss der komplette Kernel neu kompiliert werden
+ Wenn ein Modul abstürzt, stürzt der komplette Kernel ab, da ein Neustart eines einzelnen Modules schwierig bzw. unmöglich ist
#### Mikrokernel
![[Pasted image 20240208102319.png]]
![[Pasted image 20240208102643.png]]
**Vorteile:**
+ Module im Benutzermodus können wahlweise neu gestartet werden
+ System wird stabiler
+ Kritische Bereiche werden übersichtlicher
**Nachteile:**
+ System wird langsamer
#### Hybridkernel
![[Pasted image 20240208102923.png]]
**Vorteile:**
+ Schneller als Mikrokernel (nicht so viel Kommunikation )
+ Robuster als monolithischer Kernel (ermöglicht den Neustart einzelner Module)
Wird in weitverbreiteten Betriebssystemen wie Windows 10 und MacOS verwendet.

### Multimode
Der User Mode schützt das System vor versehentlichen oder bösartigen Aktionen durch normale Benutzeranwendungen. Der Kernel Mode ermöglicht es dem Betriebssystem, auf Systemressourcen zuzugreifen und kritische Aufgaben zu erledigen, während gleichzeitig die Sicherheit und Integrität des Systems gewährleistet werden.
Der Wechsel zwischen User Mode und Kernel Mode ist ein wesentlicher Bestandteil der Betriebssystemarchitektur. Wenn eine Anwendung eine Systemressource anfordert oder eine privilegierte Aktion ausführen muss, löst sie eine Ausnahme (Exception) aus, die einen Kontextwechsel vom User Mode zum Kernel Mode erfordert. Das Betriebssystem übernimmt dann die Kontrolle im Kernel Mode, führt die erforderlichen Aufgaben aus und kehrt dann zum User Mode zurück.
#### Kernelmode
Arbeitet die CPU im Kernel-Mode, so ist jeder beliebige Befehl zur Ausführung zugelassen. Es kann auf sämtliche Speicherbereiche für Daten- und Programmtext, sowie auf alle Betriebsmittel zugegriffen werden. Hier ist alles erlaubt, es bestehen die höchsten Privilegien. (Mandl 2013 nennt diesen Modus deshalb auch den privilegierten Modus.)

Durch ein Steuer- oder Kontrollregister auf der CPU wird der Kernel-Mode angezeigt.

Das Betriebssystem arbeitet üblicherweise im Kernel-Mode und hat somit alle Möglichkeiten, seine definierten Aufgaben zu erfüllen.

#### Usermode
Arbeitet die CPU im User-Mode, so ist nur ein eingeschränkter Befehlssatz zur Ausführung zugelassen. Es sind also nicht alle Befehle erlaubt, ebenso kann nicht auf alle Speicherbereiche und auch nicht auf alle Betriebsmittel zugegriffen werden.

Durch ein Steuer- oder Kontrollregister auf der CPU wird der User-Mode angezeigt.

Anwendungsprogramme arbeiten üblicherweise im User-Mode. Diese haben damit nur sehr eingeschränkte Möglichkeiten, das soll auch so sein.

### Prozess/Task
Eine laufende Instanz eines Programmes mit zugeordneten Speicher-Adressbereich 

### Thread
Ein Ausführungsstrang eines Prozesses, benutzt den Speicher-Adressbereich eines Prozesses
Prozess <----1 : n----> Thread
![[Pasted image 20240209124039.png]]

## Vergleich Betriebssysteme
**Linux**:
- Verwendet ext4
- Keine Lizenzgebühren
- Vielfältige Auswahl an Desktop-Umgebungen und grafischen Benutzeroberflächen
- Vielzahl an Open-Source-Software verfügbar

**Windows**:

- Verwendet NTFS
- Höhere Benutzerakzeptanz als bei Linux
- Eher für den Standarduser geeignet
## Dateisysteme 
- **FAT32** (File Allocation Table): Ein älteres Dateisystem, das hauptsächlich auf USB-Sticks und älteren Festplatten verwendet wird. Es hat eine begrenzte Unterstützung für Dateinamen und ist weniger sicher als andere Dateisysteme, da Daten beispielsweise bei einem Absturz häufig verloren gehen können. Zudem kann das Dateisystem maximal 2 TiB groß sein und eine einzelne Datei darf maximal 4 GiB groß sein.
- **NTFS** (New Technology File System): Ein modernes Dateisystem von Microsoft, das auf Windows-Betriebssystemen verwendet wird. Es unterstützt Features wie beispielsweise Berechtigungsverwaltung, Dateiversionierung und verschiedene Flags, die sich an den Dateien und Ordnern setzen lassen. Zudem kann das Dateisystem maximal 256 TiB groß sein und eine einzelne Datei darf maximal 16 TiB groß sein.
- **ext4** (Extended File System): Ein Dateisystem, das hauptsächlich auf Linux-Betriebssystemen verwendet wird. Es untersützt Features wie die Berechtigungsverwaltung. Zudem kann das Dateisystem maximal 1 EiB groß sein und eine einzelne Datei darf so groß sein, wie das Dateisystem selbst.
## Arten von Betriebssystemen
+ Singletasking vs Multitasking 
+ Singleuser vs Multiuser
+ Einprozessor vs Multiprozessor 
+ Stapelverarbeitung, Echtzeit, Netzwerk, ...