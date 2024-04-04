---
tags:
  - "#Testing"
---
## Definition
Pitest ist ein Mutation Test-System. Bei Mutationstests handelt es sich um Tests, welche automatisch Mutationen in den Code einfügen. Danach werden die "normalen" Tests ausgeführt. Schlägt ein Test fehl, heißt es dir Mutation des Codes wurde entdeckt und wird gekillt. Schlägt kein Test fehlt, hat die Mutation überlebt.
>[!info]
>Mutationstests überprüfen somit nicht die Richtigkeit des eigentlichen Codes, sondern die Qualität der Tests, ob diese Fehler überhaupt erkennen können. Unit-Tests hingegen, können nur Code identifizieren, der definitiv nicht getestet wird.

## Funktionsweise
PIT lässt die selbstgeschriebenen Unit-Tests des Entwicklers gegen veränderte Versionen des Codes laufen. Die Idee dabei ist, dass verschiedene Codelogiken unterschiedliche Ergebnisse liefern sollen, welche die Unit-Tests zum fehlschlagen bringen sollten. Ist dies jedoch nicht der Fall, ist dies ein Indiz, dass etwas mit der Testsuite falsch sein könnte. 
## Vor- und Nachteile
| **Vorteile**                                        | **Nachteile**                                                                                         |
| --------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| Qualität der Tests wird überprüft                   | Relativ lange Laufzeit, da bei jeder Mutation alle Tests der entsprechenden Klasse ausgeführt werden. |
| Kombinieren Zeilen Abdeckung und Mutation Abdeckung |                                                                                                       |
| Überprüft ob Tests überhaupt Fehler erkennen können |                                                                                                       |


