---
tags:
  - "#Programmieren"
  - "#Softwareentwicklung"
  - "#AP2"
---
## Erzeugungsmuster
+ **Fabrikmethode (factory methode)**: Erschafft ein Objekt ohne genau zu spezifizieren, um welche Klasse es sich handelt
+ **Abstrakte Fabrik (abstract factory kit)**: Erlaubt es Objekte zu erzeugen, ohne den Datentyp genau zu spezifizieren.
+ **Einzelstück (singelton)**: Versichert, dass nur eine Instanz des Objektes existieren kann.
+ **Erbauer (builder)**: Wird benutzt um komplexe Objekte zu erschaffen.
+ **Prototyp (prototype)**: Erschafft ein neues Objekt von einem bereits bestehendem Objekt

## Strukturmuster
+ **Adapter (adapter, wrapper)**: Ermöglicht das Zusammenarbeiten von zwei inkompatiblen Klassen durch das Einwickeln der einen Klasse mit einem Interface.
+ **Brücke (bridge, handle/body)**: Trennung von Abstraktionen -> Dies soll verhindern, dass zwei Klassen voneinander abhängen und somit unterschiedlich voneinander variieren können.
+ **Dekorierer (decorator)**: Ermöglicht das Erweitern des Verhaltens eines Objektes zur Laufzeit.
+ **Fassade (facade)**: Stellt ein simples Interface für ein grundlegendes komplexes Objekt.
+ **Fliegengewicht (flyweight)**: Reduziert die Kosten für komplexe Objektmodelle.
+ **Kompositum (composite)**: Vereint eine Gruppe von Objekten in einem einzelnem Objekt.
+ **Stellvertreter (proxy, surrogate)**: Stellt ein Platzhalter-Interface für ein grundlegendes Objekt zur Verfügung, welches den Zugriff kontrolliert und die Kosten oder die Komplexität reduziert.

## Verhaltensmuster
### Klassenmuster
+ **Interpreter (interpreter)**: Implementiert eine spezialisierte Sprache.
+ **Schablonenmethode (template methode)**: Definiert das Skelett eines Algorithmus als eine Abstrakte Klasse, wodurch den Unterklassen ermöglicht wird, das konkrete Verhalten zu implementieren.

### Objektmuster
+ **Beobachter (observer, dependents, publish- subscribe), listener**: Ermöglicht das Sehen eines Events.
+ **Besucher (visitor)**: Separiert einen Algorithmus von einer Objektstruktur, indem die Hierarchie von Methoden in ein neues Objekt ausgelagert werden.
+ **Iterator (iterator, cursor)**: Sequentieller Zugriff auf die Elemente eines Objektes, ohne die grundliegende Repräsentation des Objektes zu offenbaren.
+ **Kommando (Befehl, command, action, transaction)**: Erschafft Objekte, welche Parameter und Aktionen einkapseln.
+ **Memento (memento, token)**: Ermöglicht das Wiederherstellen eines bestimmten vorherigen Zustandes eine Objektes.
+ **Strategie (startegy, policy)**: Erlaubt es einen Algorithmus aus einer Familie von Algorithmen zur Laufzeit zu selektieren.
+ **Vermittler (mediator)**: Ermöglicht das lose Verknüpfen zweier Klassen, indem es die einzige Klasse ist, welche detailliertes Wissen über die Methoden der beiden Klassen besitzt. 
+ **Zustand (state, objects for state)**: Erlaubt einem Objekt, sein Verhalten zu ändern, wenn sein innerer Zustand sich verändert.
+ **Zuständigkeitskette (chain of responsibility)**: Delegiert Kommandos zu einer Kette von verarbeitenden Objekten.


---
## Sources
https://springframework.guru/gang-of-four-design-patterns/ (2024.04.11)
https://de.wikipedia.org/wiki/Entwurfsmuster_(Buch) (2024.04.11)