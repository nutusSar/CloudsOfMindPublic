---
tags:
  - "#AP2"
---
## Data Warehouse

### Definition
Ein Data Warehouse ist ein zentrales Repository für strukturierte Daten, das für die Durchführung von Datenanalysen und Business Intelligence (BI) optimiert ist. Es speichert Daten aus verschiedenen Quellen in einem strukturierten Format, typischerweise in relationalen Datenbanken, und unterstützt komplexe Abfragen und Berichterstattung.

### Merkmale
+ **Datenstrukturierung**: Daten werden vor der Speicherung strukturiert und aufbereitet, oft in Form von Tabellen und Dimensionen.
+ **ETL-Prozess**: Daten werden durch Extract, Transform, Load (ETL)-Prozesse in das Data Warehouse geladen, wobei sie bereinigt, transformiert und aggregiert werden.
+ **Optimierung für Abfragen**: Data Warehouses sind optimiert für schnelle Abfragen, Analysen und komplexe Berichte.
+ **Schema-on-Write**: Die Struktur der Daten wird vor der Speicherung definiert.

### Vor- und Nachteile
| **Vorteile**                                                                                                 | **Nachteile**                                                                                                             |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| **Schnelle Abfragen**: Optimiert für schnelle und komplexe Abfragen,                                         | **Kosten**: Höhere Kosten für Speicherung und Wartung, insbesondere bei großen Datenmengen                                |
| **Konsistenz**: Daten sind konsistent und strukturiert, was die Analyse erleichtert,                         | **Flexibilität**: Weniger flexibel bei der Aufnahme neuer Datenquellen oder Änderungen im Schema                          |
| **Geschäftsorientierung**: Ideal für analytische Anwendungen, Business Intelligence und Entscheidungsfindung | **Vorverarbeitung**: Daten müssen vor der Speicherung verarbeitet werden, was Zeit und Ressourcen in Anspruch nehmen kann |

## Data Lake

### Definition
Ein Data Lake ist ein zentrales Repository, das große Mengen an rohen und unstrukturierten oder semi-strukturierten Daten speichert. Es ermöglicht die Speicherung von Daten in ihrem ursprünglichen Format und unterstützt eine flexible Datenverarbeitung und Analyse.

### Merkmale
+ **Datenvielfalt**: Speichert strukturierte, semi-strukturierte und unstrukturierte Daten in ihrem ursprünglichen Format.
+ **Schema-on-Read**: Die Struktur der Daten wird erst beim Abruf definiert, nicht vor der Speicherung.
+ **Echtzeit- und Batch-Verarbeitung**: Unterstützt sowohl Echtzeit- als auch Batch-Datenverarbeitung.
+ **Skalierbarkeit**: Häufig auf kostengünstiger, skalierbarer Speicherinfrastruktur basierend, wie z.B. Cloud-Speicher.

### Vor- und Nachteile
| **Vorteile**                                                                                                                      | **Nachteile**                                                                                                                  |
| --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **Flexibilität**: Ermöglicht das Speichern und Verarbeiten von Daten in unterschiedlichen Formaten und von verschiedenen Quellen. | **Datenmanagement**: Herausforderungen bei der Verwaltung und Governance von Daten aufgrund der Vielfalt und Unstrukturierung. |
| **Skalierbarkeit**: Kostengünstige Skalierung durch Nutzung von Cloud-Speicherlösungen.                                           | **Langsamere Abfragen**: Kann langsamer bei komplexen Abfragen sein, da Daten erst beim Zugriff strukturiert werden müssen.    |
| **Datenvielfalt**: Unterstützung für eine Vielzahl von Datenarten und -quellen.                                                   | **Qualitätssicherung**: Höhere Anforderungen an Datenqualität und -konsistenz, da Daten in ihrem Rohformat gespeichert werden. |

## Gegenüberstellung
| **Merkmal**           | **Data Warehouse**                                     | **Data Lake**                                                         |
| --------------------- | ------------------------------------------------------ | ----------------------------------------------------------------------- |
| **Datenstruktur**     | Strukturierte Daten in relationalen Datenbanken        | Rohdaten in ihrem ursprünglichen Format, inkl. unstrukturierter Daten    |
| **Datenaufbereitung** | Vor der Speicherung durch ETL-Prozesse                 | Nach der Speicherung beim Abruf durch Schema-on-Read                    |
| **Optimierung**       | Für schnelle Abfragen und Analysen optimiert           | Für flexible Speicherung und Verarbeitung optimiert                     |
| **Schema**            | Schema-on-Write (Struktur vor Speicherung)             | Schema-on-Read (Struktur bei Zugriff)                                   |
| **Speicherort**       | Typischerweise teure, hochperformante Speicherlösungen | Oft kostengünstige, skalierbare Speicherlösungen                        |
| **Verarbeitung**      | Batch-Verarbeitung für analytische Anwendungen         | Echtzeit- und Batch-Verarbeitung möglich                              |
| **Datenvielfalt**     | Fokus auf strukturierte Daten                          | Unterstützung für eine Vielzahl von Datenarten und -quellen            |
