---
tags:
  - "#AP1"
  - "#SQL"
topic: Schlüsselbegriff
page: "4"
---
## Was sind Spaltenausdrücke?
Spaltenausdrücke dienen zur Änderung der Art der Datenanzeige, sowie um Berechnungen durchzuführen.
Spaltennamen sowie alle zulässigen Funktionen sind als Variablen zulässig.

## Regeln bei arithmetischen Ausdrücken
+ Auswertung von links nach rechts
+ Punkt vor Strich
+ Klammern können Standardprioritätsregeln außer Kraft setzen oder Lesbarkeit verbessern

## Beispiele
### Beispiel 1
Artikelpreis wird um 3000€ erhöht
```SQL
SELECT Artikel, Artikelpreis + 3000
FROM Sortiment
```
In der Ausgabe erscheint eine Spalte mit der Bezeichnung "Artikelpreis + 3000". Als Wert enthält diese den um 3000€ erhöhten Artikelpreis. In der Relation "Sortiment" wird weder eine neue Spalte mit dieser Bezeichnung angelegt noch wird der Inhalt des Feldes geändert. Sie dient lediglich der Anzeige.

### Beispiel 2
Artikelpreis wird zuerst mit 12 multipliziert und dann um 100€ erhöht.
```SQL
SELECT Artikel, 12 * Artikelpreis + 100
FROM Sortiment
```

Artikelpreis wird zuerst um 100€ erhöht und dann mit 12 multipliziert.
```SQL
SELECT Artikel, 12 * (Artikelpreis + 100)
FROM Sortiment
```
