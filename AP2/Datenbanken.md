---
tags:
  - "#AP2"
---
## Definition
Bei Datenbanken handelt es sich um Systeme zur elektronischen Datenverwaltung. Es ist somit eine strukturierte Sammlung von Daten/Informationen. Dieses System wird von einem DBMS (Datenbankmanagementsystem) verwaltet.

## Redundanz 
Redundanz (Überfluss) beschreibt das mehrmalige Speichern von gleichen Daten. Dies soll jedoch in einer Datenbak vermieden werden, denn redundante Daten müssen auch redundant gepflegt werden, damit es nicht zu Anomalien in der Datenbank kommt.

## Normalformen
### 1. Normalform
+ Die Attribute sind atomar. Die Attribute sind in ihre kleinstmöglichen Attributeinheiten Unterteilt. 
**Beispiel**: Name wird aufgeteilt in Vor- und Nachname.
Das erreichen der 1. Normalform kann durch das Hinzufügen von Spalten oder Zeilen geschehen.

### 2. Normalform
+ 1. Normalform
+ jedes Nicht-Schlüssel-Attribut vom Primärschlüssel voll funktional abhängig ist.
**Beispiel**: Schüler, Klasse, Klassenlehrer, Fach, Fach-Lehrer mit Primärschlüssel Schüler+ Fach, befindet sich nicht in der 2. Normalform, denn Klassenlehrer ist nur von dem Schüler Teil des Primärschlüssels abhängig und nicht vom Fach.
Somit würde man diese Relationsschema aufteilen in 2 Relationsschemen. 

### 3. Normalform
+ 2. Normlaform
+ jedes Nichtschlüsselattribute nicht transitiv vom Primärschlüssel abhängig ist, d.h. aus keinem Nichtschlüsselattribut folgt ein anderes Nichtschlüsselattribut.
**Beispiel**: Schüler, Klasse, Klassenlehrer mit Primärschlüssel Schüler ist nicht in der 3. Normalform, denn der Klassenlehrer folgt bereits aus der Klasse und somit folgt der Lehrer aus einem Nichtschlüsselattribut.

## Kardinalitäten
### Eins-zu-Eins (1:1)
- Jeder Datensatz in Tabelle A ist mit genau einem Datensatz in Tabelle B verbunden und umgekehrt. Diese Art von Beziehung wird verwendet, wenn die beiden Tabellen logisch zusammengehören, aber aus praktischen Gründen getrennt werden sollen. 
**Beispiel**:
- Eine Tabelle `Person` enthält persönliche Daten.
- Eine Tabelle `PersonDetail` enthält detaillierte Informationen zur Person, die aus Gründen der Übersichtlichkeit getrennt gehalten werden.

### Eins-zu-Viele (1:N)
- Jeder Datensatz in Tabelle A kann mit einem oder mehreren Datensätzen in Tabelle B verbunden sein, aber jeder Datensatz in Tabelle B ist mit genau einem Datensatz in Tabelle A verbunden. Dies ist die häufigste Art von Beziehung in Datenbanken. 
**Beispiel**:
- Eine Tabelle `Abteilung` enthält Informationen über Abteilungen.
- Eine Tabelle `Mitarbeiter` enthält Informationen über Mitarbeiter, wobei jeder Mitarbeiter nur einer Abteilung zugeordnet ist, aber eine Abteilung viele Mitarbeiter haben kann.

### Viele-zu-Viele (N:M)
- Jeder Datensatz in Tabelle A kann mit mehreren Datensätzen in Tabelle B verbunden sein, und umgekehrt. Diese Art von Beziehung wird oft durch eine Zwischentabelle (oder Verknüpfungstabelle) modelliert, die die Beziehungen zwischen den beiden Tabellen speichert. 
**Beispiel**:   
- Eine Tabelle `Studenten` enthält Informationen über Studenten.
- Eine Tabelle `Kurse` enthält Informationen über Kurse.
- Eine Zwischentabelle `StudentKurse` speichert, welche Studenten welche Kurse belegen, da ein Student mehrere Kurse belegen kann und ein Kurs von mehreren Studenten belegt werden kann.

## ACID
+ **Atomicity**: Eine Transaktion wird entweder als Ganzes durchgeführt oder gar nicht.
+ **Consistency**: Nach einer Transaktion, soll die Datenbank sich in einem konsistenten Zustand befinden, unter der Voraussetzung, dass sie dies zu Beginn der Transaktion bereits war.
+ **Isolation**: Parallel laufende Transaktionen dürfen sich nicht gegenseitig beeinflussen. Dies wird z.B. durch die Sperrung der Datensätze erreicht.
+ **Durability**: Nach dem erfolgreichen Abschluss einer Transkation, sind die Daten dauerhaft in der Datenbank gespeichert.


---
## Backlinks
[[AP2]]
[[Persistenz]]



