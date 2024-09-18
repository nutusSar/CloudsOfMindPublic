---
tags:
  - "#Berufsschule"
  - "#Lernfeld10_11_12"
---
## 1. Fasse mit eigenen Worten die Qualitätsmerkmale gemäß ISO 9126 zusammen:
### Wartbarkeit
Beschreibt die Einfachheit, mit der Änderungen an einem bestehendem System vorgenommen werden. Dies umfasst:
+ **Analysierbarkeit**: Aufwand der notwendig ist einen Fehler zu diagnostizieren.
+ **Modifizierbarkeit**: Aufwand zur Fehlerbeseitigung/Verbesserungen
+ **Stabilität**: Wie wahrscheinlich ist das Auftreten eines Fehlers
+ **Testbarkeit**: Wie groß ist der Aufwand fürs Testen des Systems
### Benutzbarkeit
Die Benutzbarkeit beschreibt den Aufwand und die Zufriedenheit der Benutzer beim Interagieren mit der Anwendung. Dies umfasst:
+ **Attraktivität**: Anziehungskraft der Anwendung beim Benutzer
+ **Bedienbarkeit**: Wie leicht ist die Anwendung zu bediene?
+ **Erlernbarkeit**: Wie einfach ist es das Bedienen der Anwendung zu erlernen
+ **Verständlichkeit**: Wie einfach ist es die Anwendung zu verstehen
### Effizienz
Misst das Verhältnis zwischen der Leistung der Software und den dafür eingesetzten Ressourcen. Dies umfasst:
+ **Zeitverhalten**: Durchsatz bei Funktionsausführung, Antwort- und Verarbeitungszeiten
+ **Verbrauchsverhalten**: Anzahl und Dauer der Ressourcenzugriffe
### Funktionalität
Die Funktionalität beschreibt, inwiefern die Software die geforderten Funktionen bereitstellt. Dies umfasst:
+ **Angemessenheit**: Sind Funktionen aufgabenorientiert
+ **Sicherheit**: Ist das System vor unbefugten Zugriffen geschützt
+ **Interoperabilität**: Zusammenarbeit mit anderen Systemen
+ **Richtigkeit**: Liefert die Anwendung die vereinbarten Ergebnisse/Wirkungen
### Übertragbarkeit
Beschreibt, wie leicht die Software in eine andere Umgebung z.B. ein anderes Betriebssystem bzw. andere Hardware, übertragen lässt.
+ **Anpassbarkeit**: Wie leicht kann die Software an andere Umgebungen angepasst werden
+ **Austauschbarkeit**: Wie einfach kann die Software in einer anderen Umgebung laufen
+ **Installierbarkeit**: Aufwand der Installierung der Anwendung
+ **Koexistenz**: Kann die Anwendung parallel zu einer ähnlichen Anwendung arbeiten
### Zuverlässigkeit
Bewertet die Fähigkeit der Software, unter festgelegten Bedingungen über einen bestimmten Zeitraum stabil zu funktionieren. 
+ **Fehlertoleranz**: Kann die Software angemessen auf Fehler zu Schnittstellen reagieren
+ **Reife**: Wenige Abstürze durch Fehlerzustände
+ **Wiederherstellbarkeit**: Zurückgewinnen der Daten die bei einem Fehlerzustand der Anwendung betroffen waren unter Berücksichtigung von Zeitaufwand und eigener Aufwand
## 2. Erkläre den Unterschied zwischen der Norm ISO/IEC 9126 und der ISO/IEC 25000
ISO/IEC 9126 beschreibt die Software-Qualität anhand von 6 Merkmalen,
+ Wartbarkeit
+ Benutzbarkeit
+ Effizienz
+ Funktionalität
+ Übertragbarkeit
+ Zuverlässigkeit
mit dem Ziel die Qualität auf funktionaler Ebene messbar zu machen.
ISO/IEC 25000 ersetzte ISO/IEC 9126, denn sie umfasst nicht nur die Software-Qualität auf funktionaler Ebene, sondern den gesamten Lebenszyklus. Somit werden die Qualitätsmerkmale von ISO/IEC 9126, als auch die Bewertungs- und Messmethoden von Software-Qualität mit der ISO/IEC 25000 abgebildet.
## 3. Was wurde an der Norm ISO/IEC 9126 kritisiert?
+ Unklare Definitionen/Interpretationen, da die Qualitätsmerkmale zum teil vage definiert waren
+ Fehlen von konkreten Messmethoden für eine standardisierte Metrik
+ Eingeschränkter Fokus auf funktionaler Ebene 
+ Sicherheit von Software wird nicht als eigenes Qualitätsmerkmal definiert
## 4. Wo liegt das Problem bei der Definition von "Gebrauchstauglichkeit"?
Der Begriff "Gebrauchstauglichkeit" hängt stark von den individuellen Erfahrungen und Erwartungen des Benutzers ab. 
Denn für den einen Benutzer kann die intuitiv Anwendung verwendet werden, während sie für den nächste Komplex erscheint. Somit kann keine objektive Bewertung/Messung stattfinden.
## 5. Über welchen Schnittstellen werden Software-Anforderungen (Software Requirements Specification) beschrieben?
+ **Benutzerschnittstellen**: Definieren die Interaktion zwischen der Software und dem Benutzer durch grafische oder textbasierte Oberflächen.
+ **Systemschnittstellen**: Beschreiben, wie die Software mit anderen Systemen oder Plattformen über APIs oder Webservices kommuniziert.
+ **Hardwareschnittstellen**: Bestimmen, wie die Software mit der physischen Hardware wie Druckern, Sensoren oder anderen Geräten interagiert.
+ **Kommunikationsschnittstellen**: Legen fest, welche Protokolle und Kommunikationsmethoden für den Datenaustausch zwischen Systemen genutzt werden.
+ **Softwareschnittstellen**: Definieren die interne Kommunikation zwischen verschiedenen Softwaremodulen oder externen Anwendungen.
[Quelle](https://en.wikipedia.org/wiki/Software_requirements_specification#Structure)

## 6. Welches Problem ergibt sich bei der Prüfung der "Wartbarkeit"?
+ Schwer Messbar, da die Wartbarkeit von vielen verschiedenen Faktoren wie Modularität, Codequalität, Dokumentation etc. abhängt.
+ Die Wartbarkeit von Software wird meist erst beim tatsächlichen Erweitern oder Verbessern der Software erkenntlich
## 7. Nenne die drei Aspekt-Kategorien bei der Checkliste für Software-Anforderungen
+ Funktionale Anforderungen
+ Nicht funktionale Anforderungen
+ Rahmenbedingungen 
## 8. Beschreibe zu jeder Kategorie mindestens zwei Aspekte mit eigenen Worten
### Funktionale Anforderungen 
+ **Anwendungsfälle**: Beschreiben von konkreten Anwendungsszenarien
+ **Datenverarbeitung**: Definieren, wie Daten empfangen, verarbeitet und gespeichert werden

### Nicht funktionale Anforderungen
+ **Ressourcenverbrauch**: Wie stark wird die CPU ausgelastet
+ **IT-Sicherheit**: Anmeldung wird nach drei Fehlversuchen gesperrt

### Rahmenbedingungen
+ **Technologische Vorgaben**: Welche Technologien und Plattformen sollen verwendet werden
+ **Zeitrahmen**: In welchem Zeitraum ist die Umsetzung und die Abgabe der Software erforderlich

[Quelle](https://www.johner-institut.de/blog/iec-62304-medizinische-software/funktionale-und-nicht-funktionale-anforderungen/)