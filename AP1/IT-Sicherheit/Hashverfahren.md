---
tags:
  - "#AP1"
  - "#IT-Sicherheit"
---

## Definition

Ein Hashverfahren ist eine kryptografische Funktion, die dazu dient, Daten in einer festen Länge abzubilden, wobei selbst kleine Änderungen in den Eingabedaten zu erheblichen Veränderungen im erzeugten Hashwert führen.
## Funktionsweise von Hashfunktionen

### Lawineneffekt
Der Lawineneffekt ist ein entscheidendes Merkmal von sicheren Hashfunktionen. Selbst eine minimale Änderung in den Eingabedaten sollte zu einer völlig unterschiedlichen Ausgabe führen. Dies bedeutet, dass, wenn sich auch nur ein Bit in den Eingabedaten ändert, der resultierende Hashwert statistisch gesehen vollständig unterschiedlich sein sollte. Der Lawineneffekt sorgt dafür, dass kleine Veränderungen in den Eingabedaten zu großen Veränderungen im Hashwert führen, was die Kollisionssicherheit erhöht.

### Einwegfunktion
Hashfunktionen werden als Einwegfunktionen betrachtet, was bedeutet, dass es praktisch unmöglich ist, von einem gegebenen Hashwert auf die ursprünglichen Eingabedaten zurückzuschließen. Die Einwegfunktionseigenschaft stellt sicher, dass, selbst wenn der Hashwert bekannt ist, es extrem schwierig ist, die ursprünglichen Daten zu rekonstruieren.

### Kollisionssicherheit
Kollisionen treten auf, wenn zwei unterschiedliche Eingabewerte denselben Hashwert erzeugen. Eine gute Hashfunktion strebt danach, Kollisionen zu verhindern oder zumindest so selten wie möglich zu machen. Der Lawineneffekt und die Streuung der Hashwerte spielen eine entscheidende Rolle bei der Erreichung von Kollisionssicherheit.

## Verwendung/Nutzen

- **Integritätsprüfung:** Hashwerte dienen zur Überprüfung, ob Daten während der Übertragung oder Speicherung unverändert geblieben sind.
  
- **Passwortspeicherung:** Hashfunktionen werden verwendet, um Passwörter sicher zu speichern. Der Hashwert wird gespeichert, nicht das Passwort selbst.

- **Digitale Signaturen:** Hashwerte werden in Kombination mit privaten Schlüsseln verwendet, um digitale Signaturen zu erzeugen und die Authentizität von Daten zu gewährleisten.

## Weitere wichtige Aspekte

- **Kollisionen:** Eine Kollision tritt auf, wenn zwei verschiedene Eingaben denselben Hashwert erzeugen. Gute Hashverfahren minimieren das Risiko von Kollisionen.

- **Salzen:**  Das Salzen verbessert die Sicherheit von Hashfunktionen, indem zufällige Daten den Eingabedaten vor dem Hashen hinzugefügt werden. Dies gewährleistet, dass selbst identische Passwörter unterschiedliche Hashwerte generieren, da individuelle Salze verwendet werden und erhöht somit die Sicherheit von Passwortspeicherung.

- **Stärke der Hashfunktion:** Die Sicherheit eines Hashverfahrens hängt von der Unumkehrbarkeit des Prozesses und der Widerstandsfähigkeit gegenüber Angriffen ab.

## Beispiele für sichere Hashalgorithmen

- **SHA-256 (Secure Hash Algorithm 256-bit):** Ein häufig verwendetes Hashverfahren mit einer Ausgabe von 256 Bits.

- **SHA-3 (Secure Hash Algorithm 3):** Der neueste Standard der Secure Hash Algorithm-Familie, der für verschiedene Ausgabe- und Eingabegrößen geeignet ist.

- **bcrypt:** Ein langsamer, salzbasierter Hashalgorithmus, der speziell für Passwortspeicherung entwickelt wurde.

- **Argon2:** Ein adaptiver Hashalgorithmus, der für den Schutz vor bestimmten Angriffen wie Brute-Force-Angriffen optimiert ist.
