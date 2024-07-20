---
tags:
  - AP2
---
## Definition
>[!Quote] [BSI](https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/Kompendium_Einzel_PDFs_2021/07_SYS_IT_Systeme/SYS_1_8_Speicherloesungen_Edition_2021.pdf?__blob=publicationFile&v=2)
>In der Vergangenheit wurden Speicherlösungen oft umgesetzt, indem Speichermedien direkt an einen Server angeschlossen wurden. Diese sogenannten Direct-Attached-Storage-(DAS)-Systeme können die aktuellen und zukünftigen Anforderungen jedoch oft nicht mehr erfüllen. Daher sind die heute weitverbreiteten zentralen Speicherlösungen und deren Bestandteile notwendig, die sich wie folgt unterscheiden lassen: 
> + **Speicherlösungen**: Eine Speicherlösung besteht aus einem oder mehreren Speichernetzen sowie mindestens einem Speichersystem.
> + **Speichernetze**: Speichernetze ermöglichen einerseits den Zugriff auf die Speichersysteme, andererseits die Replikation von Daten zwischen Speichersystemen.
> + **Speichersysteme**: Als Speichersystem wird die zentrale Instanz bezeichnet, die für andere ITSysteme Speicherplatz zur Verfügung stellt. Ein Speichersystem erlaubt außerdem den zeitgleichen Zugriff mehrerer IT-Systeme auf den vorhandenen Speicherplatz.

## Sicherheitsmechanismen

Die Festlegung und Implementierung von Sicherheitsmechanismen sowie Zugriffsmöglichkeiten und -rechten ist entscheidend, um die Integrität, Vertraulichkeit und Verfügbarkeit von Daten zu gewährleisten. Hier sind die wesentlichen Schritte und Überlegungen:

### 1. Anforderungsanalyse
+ Identifikation der zu schützenden Ressourcen und Daten.
+  Bestimmung der Sicherheitsanforderungen basierend auf Unternehmensrichtlinien, gesetzlichen Vorgaben und Best Practices.

### 2. Zugriffsrichtlinien erstellen
+  Definition von Benutzerrollen und -gruppen mit spezifischen Zugriffsrechten.
+  Festlegung von Richtlinien für den Zugriff auf Systeme, Anwendungen und Daten.

### 3. Authentifizierungsmechanismen implementieren    
+ Einsatz starker Authentifizierungsmethoden wie Passwort-Richtlinien, Zwei-Faktor-Authentifizierung (2FA) und biometrische Verfahren.
+ Implementierung zentraler Authentifizierungsdienste wie LDAP, Kerberos oder Active Directory.

### 4. Autorisierung und Zugriffskontrollen
+ Nutzung des Prinzips der geringsten Privilegien (Least Privilege Principle), um sicherzustellen, dass Benutzer nur die notwendigen Zugriffsrechte erhalten.
+ Einsatz von Zugriffskontrolllisten (ACLs) und rollenbasierter Zugriffskontrolle (RBAC) zur Feinsteuerung der Zugriffsrechte.
### 5. Verschlüsselung
+ Implementierung von Verschlüsselungstechniken für Daten im Ruhezustand und während der Übertragung (z. B. SSL/TLS, VPNs, Datenbankverschlüsselung).
+ Sicherstellung, dass sensible Daten immer verschlüsselt gespeichert und übertragen werden.

### 6. Überwachung und Protokollierung
+ Implementierung von Überwachungs- und Protokollierungssystemen, um verdächtige Aktivitäten und Zugriffsversuche zu erkennen.
+ Regelmäßige Überprüfung und Analyse der Protokolle zur Identifikation und Behebung von Sicherheitsvorfällen.

### 7. Schulung und Sensibilisierung:
+ Schulung der Mitarbeiter in Bezug auf Sicherheitsrichtlinien, Best Practices und den sicheren Umgang mit Daten.
+ Durchführung regelmäßiger Sicherheitstrainings und Sensibilisierungskampagnen.

### 8. Regelmäßige Sicherheitsüberprüfungen und Audits
+ Durchführung von Sicherheitsüberprüfungen und Audits, um die Wirksamkeit der implementierten Sicherheitsmechanismen zu gewährleisten.
+ Identifikation von Schwachstellen und Umsetzung von Korrekturmaßnahmen.

### 9. Notfall- und Wiederherstellungspläne
+ Erstellung und Implementierung von Notfallplänen zur schnellen Reaktion auf Sicherheitsvorfälle.
+ Sicherstellung regelmäßiger Backups und Tests der Wiederherstellungsprozesse.

### Beispielhafte Implementierung:

+ **Zugriffsmöglichkeiten**: Implementierung von VPNs für den sicheren Remote-Zugriff auf Unternehmensnetzwerke. Nutzung von Netzwerksicherheitszonen zur Segmentierung des Netzwerks und zur Begrenzung des Zugriffs auf kritische Systeme.
+ **Zugriffsrechte**: Einrichtung von RBAC (Role Based Access Control) in Datenbanksystemen wie MySQL oder PostgreSQL, um zu steuern, welche Benutzer welche Aktionen auf welchen Daten ausführen dürfen. Verwendung von ACLs auf Dateisystemebene, um den Zugriff auf spezifische Dateien und Verzeichnisse zu steuern.

## Zugangskontrollen
Zugangskontrollen sind Sicherheitsmaßnahmen, die den Zugang zu physischen oder digitalen Ressourcen beschränken, um unbefugten Zugriff zu verhindern.

+ **Gebäude**: Sicherheitsmechanismen wie Ausweiskarten, biometrische Scanner (Fingerabdruck, Gesichtserkennung), PIN-Codes oder Wachpersonal kontrollieren den Zutritt zu Gebäuden.
+ **Serverraum**: Zutrittskontrollen umfassen elektronische Zugangssysteme, biometrische Scanner und mechanische Schlösser, die sicherstellen, dass nur autorisiertes Personal Zugang zum Serverraum hat.
+ **Schrank**: Sicherheitsschränke oder Racks können mit Schlössern, Zahlencodes oder elektronischen Zugangskontrollen ausgestattet sein, um den Zugriff auf sensible Hardware oder Dokumente zu beschränken.


## Implementierung und Inbetriebnahme des Zugriffs auf lokale und vernetzte Speicherlösungen sowie vernetzte Systeme (z.B. SAN, NAS, DAS)
Die Implementierung und Inbetriebnahme von Speicherlösungen erfordert eine sorgfältige Planung und Durchführung, um sicherzustellen, dass die Systeme effizient und sicher arbeiten. Hier sind die Schritte und Überlegungen für den Zugang zu lokalen und vernetzten Speicherlösungen:

### 1. Bedarfsanalyse und Planung
+ **Bedarfsanalyse**: Bestimmen Sie den Speicherbedarf, die Performance-Anforderungen und die spezifischen Anforderungen Ihrer Anwendungen.
+ **Auswahl der Speicherlösung**: Wählen Sie die passende Speicherlösung basierend auf den Anforderungen:
	+ **[SAN (Storage Area Network)](SAN%20und%20NAS)**: Ideal für Hochleistungsanwendungen mit hohem Datenaufkommen und Bedarf an Block-Level-Zugriff.
	+ **[NAS (Network Attached Storage)](SAN%20und%20NAS)**: Geeignet für Datei-Level-Zugriff und einfache Dateifreigabe über ein Netzwerk.
	+ **DAS (Direct Attached Storage)**: Bietet direkte Verbindung zu einem Server, ideal für Anwendungen, die hohe Leistung und geringen Latenz benötigen.

### 2. Hardware- und Software-Vorbereitung
+ **Hardware-Beschaffung**: Beschaffen Sie die notwendigen Hardware-Komponenten wie Speichergeräte, Server, Netzwerk-Switches und Verkabelung.
- **Software-Vorbereitung**: Installieren und konfigurieren Sie die erforderlichen Betriebssysteme, Treiber und Verwaltungssoftware für Ihre Speicherlösung.

### 3. Netzwerk- und Infrastrukturkonfiguration
+ **Netzwerkintegration**:
	+ **SAN**: Konfigurieren Sie Fibre Channel oder iSCSI-Verbindungen und richten Sie Zoning und Masking ein, um den Datenfluss und die Sicherheit zu optimieren.
	+ **NAS**: Konfigurieren Sie Netzwerkprotokolle wie NFS oder SMB für den Dateizugriff.
	+ **DAS**: Verbinden Sie das Speichergerät direkt mit dem Server über SCSI, SAS oder SATA.
	+ **IP-Adressierung**: Planen und konfigurieren Sie IP-Adressen für Netzwerkgeräte und Speicherlösungen.

### 4. Einrichtung der Speicherlösung
+ **Physische Installation**: Installieren Sie die Hardware-Komponenten und verbinden Sie sie gemäß den Netzwerkkonfigurationsanforderungen.
+ **Speicherkonfiguration**:
+  **SAN**: Erstellen und konfigurieren Sie Speicherpools, LUNs (Logical Unit Numbers) und weisen Sie diese den entsprechenden Servern zu.
	+ **NAS**: Erstellen Sie Freigaben, definieren Sie Zugriffsrechte und konfigurieren Sie Benutzer- und Gruppenkonten.
	+ **DAS**: Konfigurieren Sie das Speichersystem auf dem Server, richten Sie RAID (falls erforderlich) ein und formatieren Sie die Laufwerke.

### 5. Implementierung von Sicherheitsmaßnahmen
+ **Zugriffskontrollen**: Implementieren Sie Zugriffskontrolllisten (ACLs), rollenbasierte Zugriffskontrolle (RBAC) und andere Sicherheitsrichtlinien, um den Zugriff auf die Speicherressourcen zu steuern.
+ **Verschlüsselung**: Implementieren Sie Verschlüsselungstechnologien für die Daten im Ruhezustand und während der Übertragung.

### 6. Testen und Validierung
+ **Funktionstests**: Führen Sie Tests durch, um sicherzustellen, dass die Speicherlösung ordnungsgemäß funktioniert und den Anforderungen entspricht.
+ **Leistungstests**: Testen Sie die Leistung der Speicherlösung unter realen Lastbedingungen, um sicherzustellen, dass sie die erforderliche Geschwindigkeit und Zuverlässigkeit bietet.
+ **Sicherheitstests**: Überprüfen Sie die Implementierung der Sicherheitsmaßnahmen, um sicherzustellen, dass der Zugriff nur für autorisierte Benutzer möglich ist.

### 7. Inbetriebnahme und Überwachung
+ **Inbetriebnahme**: Setzen Sie die Speicherlösung offiziell in Betrieb und integrieren Sie sie in Ihre IT-Infrastruktur.
+ **Überwachung**: Implementieren Sie Überwachungs- und Verwaltungstools, um die Leistung und Sicherheit der Speicherlösung kontinuierlich zu überwachen und Probleme proaktiv zu identifizieren und zu beheben.

## Berücksichtigung der Organisationsstrukturen im Unternehmen unter Beachtung von örtlichen Vorgaben
Bei der Implementierung und Verwaltung von IT-Systemen, einschließlich Speicherlösungen und Netzwerkinfrastrukturen, ist es essenziell, die Organisationsstrukturen des Unternehmens sowie örtliche Vorgaben zu berücksichtigen. 

### 1. Analyse der Organisationsstrukturen
+ **Hierarchie und Verantwortlichkeiten**  
  Verstehen Sie die Hierarchie und die Verantwortlichkeiten innerhalb des Unternehmens. Bestimmen Sie, welche Abteilungen oder Teams Zugriff auf welche Daten oder Systeme benötigen und in welchem Umfang.

+ **Arbeitsabläufe**  
  Berücksichtigen Sie die bestehenden Arbeitsabläufe und Prozesse, um sicherzustellen, dass die Implementierung der IT-Systeme diese nicht stört oder verändert.

+ **Berechtigungsanforderungen**  
  Definieren Sie die Zugriffsrechte und Sicherheitsanforderungen entsprechend den spezifischen Anforderungen der verschiedenen Abteilungen und Benutzergruppen.

### 2. Berücksichtigung örtlicher Vorgaben
+ **Regulatorische Anforderungen**  
  Stellen Sie sicher, dass alle örtlichen gesetzlichen und regulatorischen Anforderungen, wie Datenschutzbestimmungen (z.B. DSGVO) oder branchenspezifische Vorschriften, erfüllt werden.

+ **Sicherheitsrichtlinien**  
  Berücksichtigen Sie örtliche Sicherheitsrichtlinien und Standards, die möglicherweise zusätzliche Anforderungen an die physische und digitale Sicherheit stellen.

+ **Infrastrukturvorgaben**  
  Beachten Sie die baulichen und infrastrukturellen Gegebenheiten des Unternehmensstandorts, wie z.B. Kabelwege, Belüftungssysteme und Raumgestaltung, um eine reibungslose Installation und Integration der IT-Systeme zu gewährleisten.

### 3. Integration in die bestehende IT-Infrastruktur
+ **Kompatibilität**: Überprüfen Sie, ob neue Systeme und Lösungen mit der bestehenden IT-Infrastruktur und den verwendeten Technologien kompatibel sind.

+ **Schnittstellen**: Planen Sie die Integration neuer Systeme mit bestehenden Anwendungen und Datenquellen, um einen nahtlosen Betrieb zu gewährleisten.

### 4. Ressourcenplanung und -verwaltung
+ **Kapazitätsplanung**: Stellen Sie sicher, dass die IT-Systeme den aktuellen und zukünftigen Anforderungen der Organisation hinsichtlich Kapazität und Leistung gerecht werden.

+ **Budgetierung**: Berücksichtigen Sie das Budget des Unternehmens und planen Sie die Kosten für die Implementierung und Wartung der Systeme entsprechend.

### 5. Schulung und Unterstützung
+ **Schulung**: Planen und bieten Sie Schulungen für die Benutzer und Administratoren der neuen Systeme an, um sicherzustellen, dass sie die Systeme effektiv nutzen können.

+ **Support**: Richten Sie einen Support-Plan ein, der den Anforderungen der Organisation entspricht, um schnelle Problemlösungen und Unterstützung zu gewährleisten.

### 6. Dokumentation und Kommunikation
+ **Dokumentation**: Erstellen Sie umfassende Dokumentationen für die Konfiguration, Verwaltung und Nutzung der IT-Systeme.

+ **Kommunikation**: Halten Sie alle relevanten Stakeholder über Änderungen, Implementierungspläne und Zeitpläne informiert, um Missverständnisse und Widerstände zu vermeiden.

### Beispielhafte Umsetzung
+ **Organisationsstruktur**: In einem großen Unternehmen könnte die IT-Abteilung für die zentrale Verwaltung von Datenbanken verantwortlich sein, während die einzelnen Abteilungen für ihre spezifischen Datenzugriffe und Datensicherheitsmaßnahmen zuständig sind.

+ **Örtliche Vorgaben**: Ein Unternehmen in der EU muss sicherstellen, dass alle Datenverarbeitungsprozesse den Anforderungen der DSGVO entsprechen, insbesondere hinsichtlich der Speicherung und Verarbeitung personenbezogener Daten.

## Planung 
>[!Quote] [BSI](https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/Kompendium_Einzel_PDFs_2021/07_SYS_IT_Systeme/SYS_1_8_Speicherloesungen_Edition_2021.pdf?__blob=publicationFile&v=2)
>Bevor Speicherlösungen in einer Institution eingesetzt werden, SOLLTE eine Anforderungsanalyse durchgeführt werden. In der Anforderungsanalyse SOLLTEN unter anderem die Themen Performance und Kapazität betrachtet werden. Auf Basis der ermittelten Anforderungen SOLLTE dann eine detaillierte Planung für Speicherlösungen erstellt werden. Darin SOLLTEN folgende Punkte berücksichtigt werden: 
>+ Auswahl von Herstellern und Lieferanten, 
>+ Entscheidung für oder gegen zentrale Verwaltungssysteme (Management-Systeme),
>+ Planung des Netzanschlusses,
>+ Planung der Infrastruktur sowie
>+ Integration in bestehende Prozesse

## Usermanagement
Usermanagement bezeichnet die Verwaltung und Organisation von Benutzerkonten und deren Zugriffsrechten in IT-Systemen. Es umfasst die Erstellung, Aktualisierung, Deaktivierung und Löschung von Benutzerkonten sowie die Zuweisung und Überwachung von Zugriffsrechten und Sicherheitsrichtlinien. Ziel ist es, den sicheren und effizienten Zugriff auf Systemressourcen zu gewährleisten und den Anforderungen der Organisation gerecht zu werden.

## Trusted Platform Module (TPM)
[[TPM]] kann zur Verbesserung der Sicherheit von Speicherlösungen beitragen, indem es eine hardwarebasierte Verschlüsselung und sicheren Schlüsselmanagement bereitstellt. Es schützt gespeicherte Daten durch sichere Speicherung und Verwaltung von Verschlüsselungsschlüsseln, gewährleistet die Integrität der Daten und des Systems und unterstützt den Schutz von Daten bei der Speicherung auf lokalen und vernetzten Speichern.

## Fog und [Cloud](Cloudcomputing)
### Definition
**Cloud Computing:** Cloud Computing bezeichnet die Bereitstellung von IT-Ressourcen wie Rechenleistung, Speicher und Anwendungen über das Internet von zentralisierten Rechenzentren aus. Diese Ressourcen können flexibel skaliert und von überall mit Internetverbindung genutzt werden.

**Fog Computing:** Fog Computing ist ein verteiltes Computing-Modell, das Rechenleistung und Speicher näher an den Endgeräten oder Datenquellen bereitstellt. Es ergänzt das Cloud Computing, indem es Daten lokal verarbeitet, um Latenz zu reduzieren und Echtzeit-Analysen zu
### Gegenüberstellung

| **Merkmal**            | **Fog Computing**                                                                                                                 | **Cloud Computing**                                                                        |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| **Speicherort**        | Dezentrale lokale Geräte und Gateways                                                                                             | Zentralisierte Rechenzentren oder Cloud-Datenzentren                                       |
| **Zugriffszeit**       | Niedrigere Latenz durch lokale oder nahe Datenverarbeitung                                                                        | Höhere Latenz aufgrund der Entfernung zu den Rechenzentren                                 |
| **Datenverarbeitung**  | Datenverarbeitung erfolgt lokal, nahe an der Quelle                                                                               | Daten werden zentral in der Cloud verarbeitet                                              |
| **Skalierbarkeit**     | Skalierbarkeit durch Hinzufügen oder Aktualisieren von lokalen Fog Nodes                                                          | Hohe Skalierbarkeit durch Erweiterung der Cloud-Ressourcen                                 |
| **Kosten**             | Anfangskosten für lokale Hardware, potenziell niedrigere Betriebskosten bei hoher Datenverarbeitung vor Ort                       | Oft nach Nutzung (Pay-as-you-go-Modell), jedoch kann sich mit großen Datenmengen summieren |
| **Bandbreitennutzung** | Reduzierte Bandbreitennutzung durch lokale Verarbeitung und Speicherung                                                           | Hohe Bandbreitennutzung für die Übertragung von und zur Cloud                              |
| **Datenkonsistenz**    | Konsistenz muss zwischen lokalen und zentralen Systemen verwaltet werden                                                          | Konsistenz wird zentral verwaltet und synchronisiert                                       |
| **Sicherheitsrisiken** | Lokale Speicherung kann Sicherheitsrisiken durch verteilte Punkte erhöhen, jedoch mehr Kontrolle über lokale Sicherheitsmaßnahmen | Daten sind in externen Rechenzentren gespeichert, Risiko von Datenlecks und Cyberangriffen |
| **Verfügbarkeit**      | Abhängig von der Verfügbarkeit und Wartung lokaler Geräte und Netzwerke                                                           | Hohe Verfügbarkeit und Redundanz durch Cloud-Infrastruktur                                 |
| **Flexibilität**       | Flexibilität durch die Verteilung der Speicherressourcen auf verschiedene Knoten                                                  | Hohe Flexibilität bei der Skalierung von Speicher und Zugriff                              |
| **Datenverarbeitung**  | Echtzeitverarbeitung durch lokale Knoten kann schnelle Reaktionen ermöglichen                                                     | Zentrale Datenverarbeitung kann große Datenmengen effizient verarbeiten                    |

## SaaS und XaaS
| **Merkmal**           | **SaaS (Software as a Service)**                                                               | **XaaS (Anything as a Service)**                                                            |
|-----------------------|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **Definition**        | Bereitstellung von Software-Anwendungen über das Internet                                     | Bereitstellung von IT-Ressourcen und -Dienstleistungen über das Internet                   |
| **Speicherort**       | Speicher in Rechenzentren des SaaS-Anbieters                                                    | Verschiedene Speicherorte abhängig vom spezifischen XaaS-Modell (z.B. IaaS, PaaS, SaaS)  |
| **Verwaltung**        | Anbieter verwaltet Speicher und Daten                                                            | Verwaltung variiert je nach XaaS-Modell: Anbieter oder Nutzer sind verantwortlich          |
| **Skalierbarkeit**    | Anbieter skaliert Speicher nach Bedarf                                                           | Flexibilität in der Skalierung je nach Modell und Bedarf des Nutzers                       |
| **Zugriff**           | Zugang zu Daten über die SaaS-Anwendung                                                          | Zugriff auf Speicher je nach Dienstmodell und Infrastruktur                                |
Siehe auch: [[Cloudcomputing]]

## Data Warehouse
**Siehe auch**: [[Data Warehouse und Data Lake]]
+ **Datenstrukturierung:** Daten werden in strukturierten Formaten wie relationalen Tabellen gespeichert.
+ **Verwaltung:** Speicher wird typischerweise in zentralen, leistungsfähigen Rechenzentren bereitgestellt und optimiert für schnelle Datenabfragen und -analysen.
+ **Zugriffsmodell:** Daten werden vor der Speicherung aufbereitet, was einen schnellen und effizienten Zugriff auf strukturierte Daten ermöglicht.

## Data Lake
**Siehe auch**: [[Data Warehouse und Data Lake]]
+ **Datenvielfalt:** Unterstützt die Speicherung von unstrukturierten, semi-strukturierten und strukturierten Daten in ihrem Rohformat.
+ **Verwaltung:** Oft kostengünstige und skalierbare Speicherlösungen, wie Cloud-Speicher, die große Datenmengen flexibler speichern.
+ **Zugriffsmodell:** Daten werden in ihrem ursprünglichen Format gespeichert und erst beim Zugriff analysiert, was eine hohe Flexibilität für unterschiedliche Datenarten bietet.