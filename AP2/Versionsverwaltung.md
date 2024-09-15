---
tags:
  - "#AP2"
---
## Definition
Die Nutzung von Versionsverwaltungssystemen (VCS) ist ein wesentlicher Bestandteil der Softwareentwicklung.
Versionsverwaltungssysteme sind Systeme, die es ermöglichen Änderungen an Dateien, Quellcode oder Dokumenten nachzuverfolgen, zu verwalten und auf vorherige Versionen zurückzugreifen. Sie bieten Werkzeuge zum Vergleichen der Unterschiede zwischen verschiedenen Versionen, zum Zusammenführen verschiedener Versionen und zur Verwaltung von Parallel, jedoch abweichenden geführten Versionen.

## Eigenschaften
+ **Rückverfolgbarkeit**: Nachvollziehen von Änderungen, wer sie wann gemacht hat
+ **Kollaboration**: Erleichtert die Zusammenarbeit mehrerer Entwickler am selben Projekt
+ **Fehlerbehebung**: Ermöglicht das Zurücksetzen auf frühere Versionen bei Fehlern

## Verschiedene Versionsverwaltungssysteme
### Subversion (SVN)
+ Zentralisiert
+ Ein Server speichert das Haupt-Repository, auf das alle Entwickler zugreifen
+ Änderungsverfolgung und Möglichkeit, ältere Versionen wiederherzustellen

### Concurrent Version System (CVS)
+ Zentralisiert
+ Unterstützt gleichzeitige Bearbeitung von Dateien durch mehrere Benutzer
+ Einfache Architektur, aber veraltet und weniger leistungsfähig als neue Systeme

### Team Foundation Server (TFS mit Source Safe)
+ Zentralisiertes System von Microsoft
+ Integriert Versionsverwaltung, Build-Verwaltung, Tests und Projektmanagment
+ Unterstützt agile Entwicklungsprozesse und ist stark in die Microsoft-Umgebung eingebunden

### Git
+ Verteiltes Versionsverwaltungssystem (DVCS)
+ Jeder Entwickler hat eine vollständige Kopie des Repositories, was es schneller und flexibler macht
+ Unterstützt paralleles Arbeiten mit Branches und leichtes Zusammenführen von Code

## VCS vs. DVCS
+ **VCS (Zentralisierte Versionskontrollsysteme)**: Ein zentrales Repository, auf das alle Entwickler zugreifen. Änderungen werden an einem zentralen Ort gespeichert.
+ **DVCS (Verteilte Versionskontrollsysteme)**: jeder Entwickler hat eine eigene Kopie des gesamten Repositories, was die Arbeit offline und unabhängig vom zentralen Server ermöglicht.

## Wichtige Funktion eines Verwaltungssystems 
+ **Commit**: Speichern von Änderungen im Repository mit einer Beschreibung des Updates.
+ **Revert**: Zurücksetzen einer Datei oder eines ganzen Projektes auf eine frühere Version.
+ **Branch**: Erstellen eines neuen Entwicklungszweiges für parallele Arbeit an neuen Features oder Bugfixes
+ **Merge**: Zusammenführen von zwei Entwicklungszweigen, um Änderungen zu integrieren.
+ **Cherry-Pick**: Spezifische Commits von einem Branch in einen anderen kopieren, ohne den gesamten Branch zu mergen.
+ **Pull/Push**: Abrufen (Pull) und Hochladen (Push) von Änderungen zwischen lokalem und remote Repository.
+ **Rebase**: Kombiniert Änderungen eines Branches auf eine neue Basis, um die Historie sauber zu halten.

## Übliche Workflows im Team
+ **Pull-/Mergerequests**: Entwickler erstellen einen neuen Branch, arbeiten daran und stellen am Ende einen Pull- oder Mergerequest, um den Code zur Überprüfung und Integration in das Hauptrepository vorzuschlagen.
+ **Feature Branching**: Für jedes neue Feature wird ein eigener Branch erstellt, um eine saubere Trennung zwischen verschiedenen Entwicklungssträngen zu ermöglichen.
+ **Continuous Integration (CI)**: Automatisierung von Tests und Builds, um sicherzustellen, dass Änderungen keine Fehler einführen.
