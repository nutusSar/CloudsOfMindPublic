---
tags:
  - "#AP2"
  - "#Programmieren"
  - "#OOP"
---
## Definition
Eine Schnittstelle ist eine Sammlung von Methoden und/oder Eigenschaften, die eine Klasse implementieren muss. Sie beschreibt das "Was" (die Signaturen der Methoden), aber nicht das "Wie" (die Implementierung dieser Methoden).

## Zweck
Der Hauptzweck von Schnittstellen ist es, eine klare und standardisierte Kommunikationsweise zwischen verschiedenen Softwarekomponenten zu definieren. Schnittstellen ermöglichen es, dass verschiedene Klassen eine gemeinsame Basis haben, unabhängig von ihrer spezifischen Implementierung.

## Vorteile von Schnittstellen
+ **Modularität**: Schnittstellen fördern die Modularität des Codes, indem sie eine klare Trennung zwischen der Definition und der Implementierung von Funktionalitäten ermöglichen.
+ **Austauschbarkeit**: Klassen, die dieselbe Schnittstelle implementieren, können ausgetauscht werden, ohne dass der Code, der diese Klassen verwendet, geändert werden muss. Dies fördert die Flexibilität und Erweiterbarkeit des Systems.
+ **Wiederverwendbarkeit**: Durch die Definition von Schnittstellen können allgemeine Funktionalitäten standardisiert und in verschiedenen Teilen eines Systems oder in verschiedenen Projekten wiederverwendet werden.

## Schnittstellen in der Praxis
+ **API-Design**: Schnittstellen spielen eine zentrale Rolle im Design von APIs (Application Programming Interfaces), da sie die Verträge zwischen verschiedenen Softwarekomponenten definieren.
+ **Plugins und Erweiterung**: Viele Softwareanwendungen verwenden Schnittstellen, um Plugins und Erweiterungen zu ermöglichen. Entwickler können neue Funktionalitäten hinzufügen, indem sie vorgegebene Schnittstellen implementieren.
+ **Testbarkeit**: Durch die Verwendung von Schnittstellen können Abhängigkeiten in einer Anwendung leicht durch Mock-Objekte ersetzt werden, was das Testen einzelner Komponenten vereinfacht.
+ **Entkopplung**: Schnittstellen fördern die Entkopplung der Komponenten in einem Softwaresystem, was die Flexibilität und Wartbarkeit erhöht.
