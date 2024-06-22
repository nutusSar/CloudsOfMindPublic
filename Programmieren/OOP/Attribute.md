---
tags:
  - "#AP2"
  - "#Programmieren"
  - "#OOP"
---
## Definition
Attribute sind Eigenschaften oder Merkmale eines Objektes. In der OOP werden diese als Variablen in einer Klasse dargestellt. Sie beschreiben somit den Zustand eines Objektes. Jedes Objekt hat seine eigene Kopie dieser Attribute.

## Zweck
Attribute dienen dazu, die Daten und den Zustand von Objekten zu speichern. Sie sind die Hauptkomponenten, die die Eigenschaften eines Objekts definieren.

## Arten von Attributen
### Instanzattribute
Dabei handelt es sich um Attribute, die spezifisch für jede Instanz eines Objektes sind. Sie werden im Konstruktor des Objektes instanziiert.

### Klassenattribute
Diese Attribute sind für alle Instanzen eines Objektes gleich. Sie werden innerhalb der Klasse, aber außerhalb von Methoden instanziiert.

## Sichtbarkeit von Attributen
### Public
Diese Attribute sind von außerhalb der Klasse erreichbar und können somit von anderen Objekten manipuliert werden. Es gibt keine Möglichkeit, den Zugriff zu kontrollieren.

### Private
Der Zugriff auf Attribute, die als **private** markiert sind, ist nur von innerhalb der Klasse möglich, das heißt, dass nur das Objekt selbst seine Attribute verändern kann. Es gibt die Möglichkeit, **getter** und **setter** bereitzustellen, die den Zugriff auf diese Attribute von außerhalb klar definieren.

### Protected
Diese Attribute sind von innerhalb der Klasse und von allen Unterklassen erreichbar, aber nicht von außerhalb. Wie bei **private** gibt es die Möglichkeit, **getter** und **setter** zu definieren.
