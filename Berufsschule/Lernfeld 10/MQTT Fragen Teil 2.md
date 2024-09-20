---
tags:
  - "#Berufsschule"
  - "#Lernfeld10_11_12"
---
## 1. Erkläre die Topic Struktur
Die Topic Struktur organisiert Daten in einer hierarchischen Form. Diese ähnelt einem Pfad/URL. Die verschiedenen Ebenen eines Topics werden durch "/" getrennt. Eine Ebene repräsentiert eine spezifische Komponente eines Systems.

## 2. Erzeuge eine Topic-Struktur für folgendes Beispiel
```
CBS/GebäudeC/CE16/Termperatur
CBS/GebäudeC/CE16//Luftqualität
CBS/GebäudeC/CE16//Helligkeit
CBS/GebäudeC/CE16//Stromverbrauch

Schule/Gebäude/Raum/Sensor
```

## 3. Welche Rolle spielt Groß- und Kleinschreibung bei Topics?
+ Case-Sensitive, d.h. das gleiche Topic, einmal groß geschrieben und einmal klein geschrieben, ist nicht das selbe Topic
## 4. Erkläre mögliche MQTT Wildcards
+ **Single-Level (+)**: Eine Ebene kann einen beliebigen Wert enthalten
+ **Multi-Level (#)**: Alle folgenden Ebenen können beliebige Werte enthalten

## 5. Welche Aufgaben haben MQTT-Themen, die mit einem $-Symbol beginnen?
Diese Topics gelten als Reserviert, der Broker nutzt diese für interne Zwecke

## 6. Nenne und beschreibe fünf "Best Practices"
+ **Verwenden Sie niemals einen führenden Schrägstrich**: Führende Schrägstriche führen zu einer Null-Ebene
+ **Verwenden Sie niemals Leerzeichen in einem Thema**: Leerzeichen erschweren das Lesen und Debuggen
+ **Halten Sie das MQTT-Thema kurz und prägnant**: Themen sind in den Nachrichten enthalten, längeres Thema -> mehr übertragene Daten
+ **Verwenden sie nur ASCII-Zeichen**: Tippfehler durch nicht ASCII-Zeichen sind nur schwer nachzuvollziehen
+ **Nicht abonnieren "#"**: Clients sind oftmals nicht in der Lage die Nachrichtenlast zu verarbeiten
+ 
## 7. Was sind "Retained Messages"?
Die zuletzt gesendete Nachricht wird im Broker hinterlegt. Dies ermöglicht neuen Subscribern mit dem letzten hinterlegten Wert direkt zu arbeiten.
## 8. Was ist der "Last Will and Testament"?
Letzter Wille wird vom Client beim Broker hinterlegt. Ist der Client nicht mehr ordnungsgemäß mit dem Broker verbunden, sendet der Broker den letzten Willen an alle Subscriber.

## 9. Was sind "Persistent Sessions"?
Das sind spezielle Sessions für instabile Netzwerke. Der Broker Registriert einen Verbindungsabbruch und schick dem Client bei erneuter Verbindung alle verpassten Nachrichten. Dies sorgt dafür, dass Entwickler nach einem Verbindungsabbruch und einer Neuverbindung davon ausgehen können, dass der Zustand der gleiche ist als wie ohne Verbindungsabbruch. 