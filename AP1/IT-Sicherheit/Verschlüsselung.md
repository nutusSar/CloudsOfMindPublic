---
tags:
  - "#AP1"
  - "#IT-Sicherheit"
---
## Bedeutung
Unter Verschlüsselung versteht man das Umwandeln eines Textes, dem sogenannten Klartext in einen Geheimtext. Für dies Umwandlung verwändet man einen Schlüssel. Dabei ist es wichtig, dass man den Geheimtext auch wieder in den Klartext zurück wandeln kann.
Verschlüsselung hat als Ziel die [Vertraulichkeit](Schutzziele) einer Nachricht zu bewahren.
## Mono- vs. Polyalphabetische Verschlüsselung
Bei der monoalphabetischen Verschlüsselung darf das Alphabet genau einmal im Schlüssel vorhanden sein. Dies hat den großen Nachteil, dass es eine sehr geringe Anzahl an Schlüsseln gibt wodurch man durch brute-forcen den Geheimtext entschlüsseln kann. Ein monoalphabetisches Verfahren ist z.B. die [[Caesar-Verschlüsselung]].
Bei polyalphabetischen Verschlüsselungen spielt es keine Rolle, wie oft ein Buchstabe des Alphabets im Schlüssel vorkommt. Ein Beispiel für die polyalphabetische Verschlüsselung ist das [[Vigenere-Ciffre]].
## Substitution vs. Transposition
Bei der Substitution werden Buchstaben des Klartextes durch andere Zeichen ersetzt. Die Reihenfolge der ursprünglichen Buchstaben bleibt bestehen. Bei der Transposition werden die Positionen der Buchstaben innerhalb des Klartextes vertauscht. Der eigentliche Buchstabe bleibt jedoch bestehen.
## Symmetrische Verschlüsselung
### Definition
Die Symmetrische Verschlüsselung benutzt den gleichen Schlüssel für die Verschlüsselung als auch für die Entschlüsselung. Daraus resultiert das Schlüsselaustauschproblem, denn für die Ver- und Entschlüsselung benötigen beide Parteien den gleichen Schlüssel. Doch wenn der Schlüssel nun Ausgetauscht wird und eine unbefugte dritte Partei dies Mitbekommt, kann diese alle Nachrichten entschlüsseln als auch verschlüsseln. 

### Bekannte Verfahren:
+ [[Caesar-Verschlüsselung]]
+ [[Vigenere-Ciffre]]
+ [[AES]]
+ ...

## Asymmetrische Verschlüsselung
### Definition
Bei der asymmetrischen Verschlüsselung werden zwei Schlüssel generiert. Der erste Schlüssel ist der öffentliche Schlüssel, welcher ohne bedenken preisgegeben werden darf. Er dient zur Verschlüsselung einer Nachricht Der zweite Schlüssel ist der private Schlüssel, welcher nur der Person bekannt ist, für die die Nachricht bestimmt ist. Dieser wird zum Entschlüsseln der Nachricht verwendet.

Die Asymmetrische Verschlüsselung beruht meist auf mathematischen Rechenproblemen (auch Einweg Funktionen), die in eine Richtung sehr einfach, aber in die Rückrichtung aufwändig zu rechnen sind. Ein Beispiel ist das Zerlegen einer Zahl in ihre Primfaktoren.
>[!multi-column]
>>Die Hinrichtung:
>>3 * 7 = 21
>
>>Die Rückrichtung:
>>Welche beiden Primzahlen ergeben multipliziert 21?


### Bekannte verfahren
+ [[RSA]]
+ ...

## Symmetrisch vs. Asymmetrisch

| **Symmetrisch** | **Asymmetrisch** |
| :--: | :--: |
| Geringer Rechenaufwand | Mehr Rechenaufwand |
| Schneller | Langsamer |
| Sicherer | Theoretisch immer brechbar |
| Ein Schlüssel zum Ver- Entschlüsseln | Ein Schlüssel zum Verschlüsseln und ein Schlüssel zum Entschlüsseln |
| Eigener Schlüssel für jeden Kommunikationspartner | Jede Person besitzt einen öffentlichen und einen privaten Schlüssel |

## Fachbegriffe
+ Brechen => Knacken einer Verschlüsselung
+ Chiffrat => Geheimtext
+ Chiffre => Verschlüsselungsverfahren
+ Chiffrieren => Etwas verschlüsseln
+ Chiffrierung => Verschlüsselung 
+ Dechiffrat => Klartext nach der Entschlüsselung  
+ Entschlüsseln => Umwandeln des Geheimtextes in Klartext
+ Entziffern => Entschlüsseln eines Geheimtextes ohne den Schlüssel vorher gekannt zu haben 