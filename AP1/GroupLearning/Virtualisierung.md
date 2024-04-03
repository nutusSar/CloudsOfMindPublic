---
tags:
  - "#AP1"
  - "#Netzwerktechnik"
---
## Definition
Virtualisierung bezeichnet die Erstellung virtueller Versionen von Hardware, Betriebssystemen, Speichergeräten oder anderen Ressourcen, um mehrere Anwendungen oder Betriebssysteme auf einem einzelnen physischen Server auszuführen, wodurch die Effizienz und Flexibilität der IT-Infrastruktur erhöht werden.
Unabhängigkeit von den physischen Hardwareressourcen, d.h. man kann sich z.B. eine x86 Architektur auf einem ARM Prozessor virtualisieren, da die Hardware emuliert wird.

![[Pasted image 20240210170432.png]]

## Hypervisor
![[Pasted image 20240210170236.png]]
### Typ 1
Bare-Metal, hat direkten Zugriff auf die Hardwareresourcen, läuft direkt auf der Hardware
+ Schneller als Typ 2
### Typ 2
!(Bare-Metal, hat direkten Zugriff auf die Hardwareresourcen, läuft direkt)
Ist eine Anwendung, die auf den Host-Betriebssystem installiert ist.
+ Langsamer als Typ 1, da dieser sich mit den Host-Betriebssystem absprechen muss
+ Beibehalten der Funktionen des Host-Betriebssystems 
## Servervirtualisierung 
Servervirtualisierung ist die Technologie, bei der eine physische Server-Hardware in mehrere virtuelle Instanzen aufgeteilt wird, die unabhängig voneinander laufen können, wodurch Ressourcen besser genutzt und die Effizienz gesteigert wird.
## Desktopvirtualisierung
Desktopvirtualisierung ist eine Technologie, bei der ein zentraler Server Desktop-Betriebssysteme und -Anwendungen hostet, die dann auf entfernten Geräten, wie Laptops oder Thin Clients, über das Netzwerk bereitgestellt und ausgeführt werden, was die Verwaltung, Sicherheit und Flexibilität verbessert.
## Anwendungvirtualisierung
Die Anwendungsvirtualisierung ist eine Technologie, bei der Anwendungen von der physischen Hardware isoliert und in einer virtualisierten Umgebung ausgeführt werden, was eine einfachere Bereitstellung, Portabilität und Verwaltung der Anwendungen ermöglicht, unabhängig von der zugrunde liegenden Betriebssystem- oder Hardwareplattform.

## Snapshot
**Abbild einer virtuellen Maschine**
Bei der Erstellung werden Status, die Konfiguration und die Datenträgerinhalte einer virtuellen Maschine gespeichert. Dies kann im laufendem Betrieb erstellt werden. Es ist problemlos möglich auf einen Snapshot zurückzukehren. Vor Veränderung der Konfig ist ein Snapshot zu empfhelen

## Container vs Virtualisierung 
Container und Virtualisierung sind beide Technologien zur Bereitstellung und Verwaltung von Anwendungen, unterscheiden sich jedoch in ihrer Herangehensweise und den damit verbundenen Vor- und Nachteilen.

### Virtualisierung:
- Virtualisierung erstellt virtuelle Maschinen (VMs), die vollständige Betriebssysteminstanzen einschließlich des Kernels umfassen.
- Jede VM benötigt ein eigenes Betriebssystem und startet einen eigenen Kernel, was zu einem höheren Ressourcenverbrauch führen kann.
- Isolierte Umgebungen ermöglichen die Ausführung unterschiedlicher Betriebssysteme auf demselben Host.

### Container:
- Container teilen sich den Kernel des Host-Betriebssystems und isolieren nur die Anwendungsprozesse.
- Container sind leichtgewichtiger, da sie ohne eigenes Betriebssystem auskommen und Ressourcen effizienter nutzen.
- Da sie den Kernel teilen, sind Container in der Regel schneller und verbrauchen weniger Speicher als virtuelle Maschinen.
- Portabilität (Image -> Zweite Instanz, horizontale Skalierung)

![[Pasted image 20240224114730.png]]

Die Wahl zwischen Container und Virtualisierung hängt von den spezifischen Anforderungen ab. Container eignen sich gut für Anwendungen mit vielen Microservices, bei denen Effizienz und Skalierbarkeit wichtig sind. Virtualisierung wird oft für Workloads bevorzugt, die unterschiedliche Betriebssysteme erfordern oder mehr Isolation benötigen. Oft werden beide Technologien auch kombiniert, um die Vorteile beider Ansätze zu nutzen.


