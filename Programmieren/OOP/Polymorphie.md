---
tags:
  - "#AP2"
  - "#Programmieren"
  - "#OOP"
---
# Polymorphie
## Definition
Polymorphie bedeutet "vielgestaltig" und in der Programmierung bezieht es sich auf die Fähigkeit einer Methode oder eines Objekts, in verschiedenen Kontexten unterschiedliche Formen oder Verhaltensweisen anzunehmen.

## Zweck
Der Hauptzweck von Polymorphie ist es, die Wiederverwendbarkeit und Flexibilität des Codes zu erhöhen. Es ermöglicht es Entwicklern, generischen Code zu schreiben, der mit Objekten verschiedener Klassen arbeiten kann, solange diese Klassen eine gemeinsame Schnittstelle oder Basisklasse implementieren.

## Arten von Polymorphie

### Methodenüberladung
Dies ist eine Form der Polymorphie, bei der mehrere Methoden im selben Scope denselben Namen haben, sich jedoch in der Anzahl oder den Typen ihrer Parameter unterscheiden. Diese Art von Polymorphie ist in statisch typisierten Sprachen wie Java und C# häufig.

### Methodenüberschreibung (Overriding)
Dies ist eine Form der Polymorphie, bei der eine Methode in einer Unterklasse eine Methode der Oberklasse mit derselben Signatur ersetzt. Diese Art von Polymorphie wird verwendet, um spezifisches Verhalten in Unterklassen zu implementieren.

### Subtyp-Polymorphie (Inklusionspolymorphie)
Dies ist die häufigste Form der Polymorphie in der OOP. Sie ermöglicht es, eine Oberklasse-Referenz zu verwenden, um ein Objekt einer Unterklasse zu referenzieren. Dadurch kann einheitlicher Code geschrieben werden, der mit Objekten verschiedener Klassen arbeitet.

## Vorteile von Polymorphie
+ **Erweiterbarkeit**: Polymorphie ermöglicht es, neue Klassen hinzuzufügen und deren spezifische Implementierungen zu definieren, ohne den bestehenden Code zu ändern. Dies fördert die Erweiterbarkeit des Systems.
+ **Wiederverwendbarkeit**: Durch die Verwendung von Polymorphie kann allgemeiner Code geschrieben werden, der mit einer Vielzahl von Objekten arbeitet, was die Wiederverwendbarkeit des Codes erhöht.
+ **Wartbarkeit**: Polymorphie fördert die Wartbarkeit des Codes, da Änderungen an der Implementierung einer Methode in einer Unterklasse vorgenommen werden können, ohne den Code zu beeinflussen, der die Oberklasse verwendet.
+ **Flexibilität**: Polymorphie bietet die Flexibilität, verschiedene Implementierungen zur Laufzeit auszuwählen, was die Anpassungsfähigkeit des Systems erhöht.
