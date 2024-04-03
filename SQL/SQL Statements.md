---
tags:
  - "#AP1"
  - "#SQL"
topic: Syntax
page: "2"
---
## SQL Statements
Die meisten Operation werden mittels SQL Statements durchgeführt.
Diese bestehen aus Schlüsselwörtern gefolgt von Namen oder Operationen.
## Allgemeine Syntax
```SQL
SELECT [DISTINCT | ALL] <Spaltenliste> | *
FROM <Tabellenliste>
[WHERE <Bedingungsliste>]
[GROUP BY <Spaltenliste>]
	[HAVING <Bedingungsliste>]
[UNION | MINUS | INTERSECT <Select-Ausdruck>]
[ORDER BY <Ordnungsliste>];
```

## Abarbeitungsrheinfolge
1) Alle in der Relationenliste angegebenen Relationen werden über das Kreuzprodukt oder einen JOIN miteinander verknüpft.
2) Auswahl aller Tupel (Zeilen), die die angegebene WHERE-Bedingung erfüllen. Eine Relation liegt vor.
3) Mittels der Auswahlliste am Anfang der SELECT-Anweisung findet jetzt auf das bisherige Resultat eine Projektion auf die angegebenen Spalten statt.
4) Gruppierung gemäß der GROUP BY-Klausel. Eine Gruppierung fasst dabei mehrere Tupel zu einem Tupel zusammen, so dass die Ergebnisrelation weniger Tupel enthält.
5) Eine folgende HAVING-Klausel führt jetzt auf das Ergebnis der Gruppierung nochmals eine Restriktion auf bestimmte Tupel durch.
6) Alle Hauptteile der SELECT-Anweisung werden jetzt mittel UNION, INTERSECT oder MINUS miteinander verknüpft.
7) Ergebnisrelation wird nach der Ordnungsliste der ORDER BY-Klausel sortiert.

