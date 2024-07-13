---
tags:
  - "#AP2"
---
## Definition
Bei Datenbanken handelt es sich um Systeme zur elektronischen Datenverwaltung. Es ist somit eine strukturierte Sammlung von Daten/Informationen. Dieses System wird von einem DBMS (Datenbankmanagementsystem) verwaltet.

## Redundanz 
Redundanz (Überfluss) beschreibt das mehrmalige Speichern von gleichen Daten. Dies soll jedoch in einer Datenbak vermieden werden, denn redundante Daten müssen auch redundant gepflegt werden, damit es nicht zu Anomalien in der Datenbank kommt.

## Schlüssel
+ **Primärschlüssel**: Eindeutiges Attribut eines jeden Elementes einer Tabelle
+ **Fremdschlüssel**: Attribut, welches der Primärschlüssel eines Elementes einer Anderen Tabelle ist
+ **Anonym**: Künstlich erstellte Schlüssel ohne inhaltliche Bedeutung, die rein zur Identifikation dienen und keine externe Referenz haben.
+ **Künstlich**: Es wird dem Element ein weiteres Attribut hinzugefügt, welches zur Identifizierung dient (fortlaufende Nummer).
+ **Natürlich**: Es wird ein vorhandenes Attribut des Elementes als Primärschlüssel ausgewählt.
+ **Zusammengesetzt**: Es werden mehrere vorhandene Attribute des Elementes zusammen als Primärschlüssel ausgewählt.
## Referentielle Integrität

### Definition
Die referentielle Integrität in Datenbanken bezieht sich auf die Konsistenz und die Ordnung der Daten, insbesondere in Bezug auf Beziehungen zwischen Tabellen. Sie umfasst zwei wichtige Konzepte:
+ **Aktualisierungsweitergabe**: Dies bedeutet, dass Änderungen an einem Primärschlüsselwert (in der referenzierten Tabelle) automatisch in allen Fremdschlüsseln (in abhängigen Tabellen) aktualisiert werden. Dadurch bleiben alle Verweise auf die aktualisierte Datensatzidentität konsistent und korrekt.
+ **Löschweitergabe**: Hierbei geht es darum, dass das Löschen eines Datensatzes in der Primärtabelle dazu führt, dass alle abhängigen Datensätze in den Fremdschlüsseltabellen ebenfalls gelöscht werden. Dies verhindert "verwaiste" Datensätze oder Referenzen auf nicht mehr existierende Datensätze und trägt zur Datenkonsistenz bei.

### Löschmaßnahmen
#### CASCADE
Wenn CASCADE verwendet wird, wird eine Löschoperation auf den Primärschlüssel einer Tabelle auch alle abhängigen Datensätze in Fremdschlüssel-Tabellen löschen. Dies bedeutet, dass, wenn ein Datensatz in der Primärtabelle gelöscht wird, alle zugehörigen Datensätze in den Fremdschlüssel-Tabellen ebenfalls automatisch gelöscht werden.

#### DENY oder RESTRICT
Diese Option verhindert die Löschoperation, wenn in abhängigen Tabellen noch Datensätze vorhanden sind, die auf den zu löschenden Primärschlüssel verweisen. Dadurch wird sichergestellt, dass keine Daten gelöscht werden, die von anderen Datensätzen abhängig sind.

#### SET NULL
Bei Verwendung dieser Option werden die Fremdschlüssel in den abhängigen Tabellen auf NULL gesetzt, wenn der entsprechende Datensatz in der Primärtabelle gelöscht wird. Dies bedeutet, dass die Referenz auf den gelöschten Datensatz aufgehoben wird.

#### NO ACTION 
(Standardverhalten): Wenn keine der oben genannten Optionen explizit festgelegt ist, wird oft das NO ACTION-Verhalten verwendet. Dabei wird die Löschoperation abgebrochen, wenn es noch abhängige Datensätze gibt, um unbeabsichtigte Löschungen und Dateninkonsistenzen zu vermeiden.

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
+ Jeder Datensatz in Tabelle A ist mit genau einem Datensatz in Tabelle B verbunden und umgekehrt. Diese Art von Beziehung wird verwendet, wenn die beiden Tabellen logisch zusammengehören, aber aus praktischen Gründen getrennt werden sollen. 
**Beispiel**:
+ Eine Tabelle `Person` enthält persönliche Daten.
+ Eine Tabelle `PersonDetail` enthält detaillierte Informationen zur Person, die aus Gründen der Übersichtlichkeit getrennt gehalten werden.

### Eins-zu-Viele (1:N)
+ Jeder Datensatz in Tabelle A kann mit einem oder mehreren Datensätzen in Tabelle B verbunden sein, aber jeder Datensatz in Tabelle B ist mit genau einem Datensatz in Tabelle A verbunden. Dies ist die häufigste Art von Beziehung in Datenbanken. 
**Beispiel**:
+ Eine Tabelle `Abteilung` enthält Informationen über Abteilungen.
+ Eine Tabelle `Mitarbeiter` enthält Informationen über Mitarbeiter, wobei jeder Mitarbeiter nur einer Abteilung zugeordnet ist, aber eine Abteilung viele Mitarbeiter haben kann.

### Viele-zu-Viele (N:M)
+ Jeder Datensatz in Tabelle A kann mit mehreren Datensätzen in Tabelle B verbunden sein, und umgekehrt. Diese Art von Beziehung wird oft durch eine Zwischentabelle (oder Verknüpfungstabelle) modelliert, die die Beziehungen zwischen den beiden Tabellen speichert. 
**Beispiel**:   
+ Eine Tabelle `Studenten` enthält Informationen über Studenten.
+ Eine Tabelle `Kurse` enthält Informationen über Kurse.
+ Eine Zwischentabelle `StudentKurse` speichert, welche Studenten welche Kurse belegen, da ein Student mehrere Kurse belegen kann und ein Kurs von mehreren Studenten belegt werden kann.

## ACID
+ **Atomicity**: Eine Transaktion wird entweder als Ganzes durchgeführt oder gar nicht.
+ **Consistency**: Nach einer Transaktion, soll die Datenbank sich in einem konsistenten Zustand befinden, unter der Voraussetzung, dass sie dies zu Beginn der Transaktion bereits war.
+ **Isolation**: Parallel laufende Transaktionen dürfen sich nicht gegenseitig beeinflussen. Dies wird z.B. durch die Sperrung der Datensätze erreicht.
+ **Durability**: Nach dem erfolgreichen Abschluss einer Transkation, sind die Daten dauerhaft in der Datenbank gespeichert.

## Anomalien
+  **Einfügeanomalie**: Eine Einfügeanomalie tritt auf, wenn bestimmte Daten in eine Datenbank nicht eingefügt werden können, ohne dass gleichzeitig unnötige oder unvollständige Informationen eingefügt werden müssen.
+  **Änderungsanomalie**: Eine Änderungsanomalie entsteht, wenn eine Aktualisierung in einer Datenbank an mehreren Stellen vorgenommen werden muss, um Konsistenz zu gewährleisten, was zu Inkonsistenzen führen kann, wenn nicht alle Änderungen korrekt ausgeführt werden.
+ **Löschanomalie**: Eine Löschanomalie tritt auf, wenn das Löschen bestimmter Daten aus einer Datenbank dazu führt, dass wichtige, noch benötigte Informationen ebenfalls unbeabsichtigt gelöscht werden.
## Datentypen
+ **Boolesche Werte**: Datentyp mit den Werten `true` und `false`.
+ **Ganzzahl**: Datentyp für ganze Zahlen ohne Dezimalstellen.
+ **Gleitkommawerte**: Datentyp für Zahlen mit Dezimalstellen.
+ **Währung**: Datentyp für Geldbeträge, oft mit festgelegten Dezimalstellen für Genauigkeit.
+ **Datumswerte**: Datentyp für Datum und Uhrzeit.
+ **Texte fester Länge**: Datentyp für Zeichenketten mit fester, vorgegebener Länge.
+ **Texte variabler Länge**: Datentyp für Zeichenketten, deren Länge variabel ist.
+ **BLOB (Binary Large Object)**: Datentyp für große binäre Daten, wie Bilder oder Videos.
+ **Geokoordinaten**: Datentyp zur Speicherung von Längen- und Breitengraden für geografische Positionen.

## Umgang bei Integragtion/Erweiterung
Bei der Integration und Erweiterung von Bestandssystemen ist es entscheidend, vorhandene Datenbank- und Speicherkonzepte sorgfältig zu berücksichtigen. Dies beinhaltet die Analyse der bestehenden Datenstruktur, Datenformate, Zugriffsmethoden und Integrationspunkte. Durch die Einhaltung etablierter Konzepte wie Datenbanknormalisierung, gute Indexierung, effiziente Speicherverwaltung und die Sicherstellung der Datenkonsistenz können Kompatibilitätsprobleme minimiert und die Leistung optimiert werden. Darüber hinaus sollten Erweiterungen so gestaltet werden, dass sie die Skalierbarkeit des Systems unterstützen und zukünftige Anforderungen problemlos integrieren können, ohne die Integrität oder Sicherheit der vorhandenen Daten zu beeinträchtigen.

## Betrachten von Schnittstellen
Das Beachten von Schnittstellen zu weiteren Systemen ist ein wichtiger Aspekt bei der Integration von Speicherlösungen und Datenbanksystemen. Es erfordert eine genaue Analyse und Planung, um sicherzustellen, dass die neuen Systeme nahtlos mit bestehenden oder zukünftigen Systemen kommunizieren können. Dies beinhaltet die Berücksichtigung von APIs (Application Programming Interfaces) und anderen Kommunikationsstandards, um Daten effizient auszutauschen und Interoperabilität sicherzustellen. Durch die Einhaltung solcher Schnittstellenstandards können Integrationsprobleme minimiert und die Integration neuer Funktionen oder Systeme erleichtert werden, ohne die Stabilität oder Sicherheit des Gesamtsystems zu gefährden.

## Datenquellen
| **Merkmal**            | **Relationale Datenbanken**                                                                   | **Schemafreie Datenbanken**                                                                 | **Sensoren**                                                                     | **CSV-Dateien**                                                                             |
| ---------------------- | --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| **Struktur**           | Strukturierte Daten in Tabellen mit vordefinierten Schemata.                                  | Flexible Datenmodelle ohne feste Strukturanforderungen.                                     | Echtzeitdaten aus physischen oder digitalen Messungen.                           | Tabellarische Daten im CSV-Format für einfache Datenspeicherung und -austausch.             |
| **Abfragesprache**     | SQL (Structured Query Language) für komplexe Abfragen und Transaktionen.                      | Meistens NoSQL-Abfragesprachen wie MongoDB Query Language.                                  | -                                                                                | -                                                                                           |
| **Datenintegrität**    | Hohe Datenintegrität durch Konsistenzregeln und Transaktionskontrolle.                        | Flexibilität in der Datenmodellierung kann zu Kompromissen bei der Datenintegrität führen.  | Abhängig von der Genauigkeit der Sensoren und der Umgebung.                      | -                                                                                           |
| **Skalierbarkeit**     | Skalierbarkeit kann durch vertikale oder horizontale Partitionierung erreicht werden.         | Skalierbarkeit durch horizontale Skalierung und Verteilung der Daten auf mehrere Knoten.    | -                                                                                | -                                                                                           |
| **Datenformat**        | Fest definierte Strukturen in Tabellenformaten.                                               | Variabler Datensatzformat; unterstützt unstrukturierte und halbstrukturierte Daten.         | Echtzeitdaten in verschiedenen Formaten wie numerische Werte, Texte, Bilder usw. | Textbasiertes Format mit Trennzeichen wie Komma, semikolon, oder Tabulator.                 |
| **Anwendungsbereiche** | Geeignet für Anwendungen, die komplexe Abfragen, Transaktionen und Datenintegrität erfordern. | Gut geeignet für Big Data, IoT-Anwendungen und Projekte mit unvorhersehbarem Datenwachstum. | IoT, Überwachung, Umweltüberwachung, Gesundheitswesen, Verkehrsmanagement usw.   | Datenaustausch zwischen verschiedenen Systemen und einfache Archivierung von Tabellendaten. |


---
## Backlinks
[[AP2]]
[[Persistenz]]



