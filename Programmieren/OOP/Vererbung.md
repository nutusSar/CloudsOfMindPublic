---
tags:
  - "#AP1"
  - "#Programmieren"
  - "#OOP"
---
## Definition
Vererbung ist ein Mechanismus, durch den eine Klasse (Unterklasse) Eigenschaften und Verhaltensweisen (Attribute und Methoden) von einer anderen Klasse (Oberklasse) übernimmt. Die Unterklasse kann zusätzlich eigene Eigenschaften und Verhaltensweisen definieren oder geerbte Methoden überschreiben.

## Zweck
Der Hauptzweck der Vererbung besteht darin, Codewiederverwendung und eine hierarchische Struktur von Klassen zu ermöglichen. Dadurch wird der Code modularer, leichter verständlich und einfacher zu warten.

## Arten der Vererbung
### Einfache Vererbung
Eine Unterklasse erbt von einer einzigen Oberklasse.

### Mehrfachvererbung
Eine Unterklasse erbt von mehr als einer Oberklasse. Dies ist in einigen Programmiersprachen wie Python möglich, aber in anderen wie Java nicht erlaubt. In Java wird Mehrfachvererbung durch Interfaces erreicht.

### Multilevel-Vererbung
Eine Klasse erbt von einer Unterklasse, die wiederum von einer anderen Klasse erbt, wodurch eine mehrstufige Hierarchie entsteht.

### Hierarchische Vererbung
Eine Oberklasse wird von mehreren Unterklassen geerbt.

### Hybride Vererbung
Eine Kombination aus zwei oder mehr Vererbungstypen.

## Vorteile der Vererbung
+ **Codewiederverwendung**: Durch die Vererbung können bestehende Klassen wiederverwendet werden, ohne den ursprünglichen Code zu duplizieren. Dies fördert die Effizienz und reduziert Redundanz.
+ **Erweiterbarkeit**: Neue Klassen können leicht erstellt werden, indem sie von bestehenden Klassen erben und zusätzliche Eigenschaften oder Methoden hinzufügen oder vorhandene überschreiben. Dies fördert die Erweiterbarkeit des Systems.
+ **Wartbarkeit**: Änderungen an der Oberklasse wirken sich automatisch auf alle Unterklassen aus, was die Wartbarkeit des Codes verbessert. Dies bedeutet, dass allgemeine Änderungen zentral vorgenommen werden können.
+ **Hierarchische Klassifizierung**: Vererbung ermöglicht die Schaffung einer hierarchischen Struktur von Klassen, was die Organisation und Strukturierung des Codes erleichtert.
