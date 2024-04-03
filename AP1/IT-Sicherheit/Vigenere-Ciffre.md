---
tags:
  - "#AP1"
  - "#IT-Sicherheit"
---
## Erklärung
Die Vigenere-Chiffre ist eine symmetrische Verschlüsselung aus dem 16. Jahrhundert.  Sie ist polyalphabetisch, d.h., dass Buchstaben sich im Schlüssel wiederholen dürfen.
## Ablauf
Zuerst wird das sogenannte "Vigenere-Quadrat" gebildet. Dies sieht wie folgt aus:
![[Pasted image 20231117130233.png]]

In der obersten Zeile befindet sich die Klartextzeile, während die Spalte ganz links die Schlüsselspalte ist.
Nun kann man sich einen beliebigen Schlüssel aussuchen. In diesem Fall der Schlüssel "PASSWORT".
Im nächsten Schritt wird der Schlüssel so oft wie möglich Buchstabe für Buchstape über den Klartext geschrieben.
Achtung es ist wichtig, dass jeder Buchstabe am Ende genau einem anderen Buchstaben zugeordnet ist.

Ein Beispiel:
<div style="font-family: Monospace;">
Passw ortPassw ortP <br>
Super geheimer Text
</div>

### Verschlüsselung
Als nächstes erfolgt die Verschlüsselung. Dabei wird in der Schlüsselspalte die Zeile mit dem aktuellen Buchstaben des Schlüssels gesucht und in der Klartextzeile die Spalte des Klartextes. Wo sich dann die Beiden Zeilen und Spalten dann treffen, befindet sich der entsprechende Buchstabe des Geheimtextes.

Ein Beispiel:
P ist der erste Buchstabe des Schlüssels, also ist unsere Zeile die P Zeile.
S ist der erste Buchstabe des Klartextes, also ist unsere Spalte die S Spalte.
Es wird geschaut, wo die P Zeile und die S Spalte sich kreuzen. Dies passiert an der Stelle H. Somit ist H der erste Buchstabe unseres Geheimtextes.
Aus "Super geheimer Text" wird "Huhwn uvatiewn Hvqi"

### Entschlüsselung
Bei der Entschlüsselung wird der Schlüssel, genau wie bei der Verschlüsselung, über den Geheimtext geschrieben.
Der Schlüssel gibt die Zeile an, in welcher wir den aktuellen Buchstaben des Geheimtextes suchen, um somit die passende Spalte des Klartextes zu erhalten.

Ein Beispiel:
P ist wieder der erste Buchstabe des Schlüssels, also ist unsere Zeile die P Zeile.
H ist der erste Buchstabe des Geheimtextes. Das H in der P Zeile befindet sich in der Spalte S.
Somit ist der erste Buchstabe des Klartextes ein S.
Aus "Huhwn uvatiewn Hvqi" wird wieder "Super geheimer Text"
