---
tags:
  - "#AP2"
  - "#Programmieren"
---
## Definition
Unter dem Begriff Rekursion verbirgt sich der Prozess einer Funktion, die sich selbst erneut aufruft. Dies geschieht solange, bis ein bestimmter Fall eintritt.
## Vor- und Nachteile
| **Vorteile**                                                            | **Nachteile**                                                                      |     |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | --- |
| Zustandslos -> Beweisbarkeit des Codes auf Korrektheit bleibt vorhanden | Maximale Verschachtelungstiefe kann erreicht werden, wodurch das Programm abstürzt |     |
| Aufteilen eines Problems in mehrere Teilprobleme                        | Hoher Speicherverbrauch                                                            |     |
| Effizienter bei bestimmten Datenstrukturen als Iterative Lösungen       | Schwerer zu Debuggen -> Verschachtelungstiefe kann sehr schnell sehr tief werden   |     |
| Rekursiver Code kann verallgemeinert werden                             | I                                                                                  |     |
## Bekannte rekursive Algorithmen 
+ **Fakultät**
+ **Fibonacci-Folge**
+ **Baumüberquerung**
+ **Schnelles Sortieren**

## Arten der Rekursion
+ **Direkte Rekursion**: Die Funktion ruft sich selbst auf.
+ **Indirekte Rekursion**: Die Funktion ruft eine zweite Funktion auf, welche die erste wieder aufruft. Es entsteht ein Loop zwischen den beiden Funktionen.
+ **Endrekursion**: Die Funktion ruft sich am Ende eines rekursiven Aufrufs erneut auf. Berechnungen werden vor dem rekursiven Aufruf durchgeführt. Somit wird die Rekursion Effizienter und das Risiko des Aufbrauchens des Stapelspeichers reduziert.
+ **Nicht-Schlussrekursion**: Berechnungen werden auch noch nach dem rekursiven Aufruf durchgeführt.
+ **Gegenseitige Rekursion**: Mehrere Funktionen rufen sich gegenseitig Rekursiv auf, bis eine Bedingung erfüllt ist. Oftmals bei der Lösung von mehreren sich ähnelnden Probleme verwendet.



---
## Quellen
+ https://databasecamp.de/python/rekursion
