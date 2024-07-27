---
tags:
  - "#AP2"
  - "#Programmieren"
---
## Definition
Bei Programmiersprachen handelt es sich im künstliche/formale Sprachen, die zur Definierung von Datenstrukturen und Algorithmen dienen.
Sie folgen bestimmten Mustern und Regeln und besitzen einen vordefinierten Zeichensatz sowie Wortschatz.

## Compiler vs. Interpreter
### Compiler
 + Der gesamte Quellcode wird vor der Ausführung in Maschinensprache bzw. Bytecode übersetzt
 + Der Zwischencode kann auf verschiedenen Plattformen ausgeführt werden,
 + Via. Linker wird die ausführbare Datei erstellt
 + Kompilieren erfordert Zeit und Ressourcen, zur Laufzeit jedoch schneller
 + Schwerer zu Debuggen, Fehler werden erst nach dem Kompilieren erkannt
 + Beispiele: C, C++

### Interpreter
+ Der Quellcode wird direkt Zeile für Zeile ausgeführt, d.h. der Interpreter verarbeitet den Code zur Laufzeit des Programmes
+ fungiert als Vermittler zwischen Maschine und Programmierer
+ Ist zur Laufzeit langsamer als der Compiler
+ Einfacher zu Debuggen, Fehler werden direkt zur Laufzeit erkannt
+ Beispiele: Python, JS

### Just-In-Time-Compiler
+ Vereinigung von Interpreter und Compiler
+ Kompilieren des Programmes erst zur Laufzeit
+ Durch den Interpreter, können zur Laufzeit Fehler erkannt werden
+ Programm ist Plattformunabhängig
+ Beispiele: C++.NET, C#



---
## Quellen
+ https://www.dev-insider.de/der-unterschied-von-compiler-und-interpreter-a-742282/ (27.07.2024)