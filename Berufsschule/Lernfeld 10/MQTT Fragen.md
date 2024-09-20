---
tags:
  - "#Berufsschule"
  - "#Lernfeld10_11_12"
---
## 1. Wofür wird MQTT genutzt?
Wird im Umfeld des IoT genutzt, um eine einfache Kommunikation zwischen Geräten zu ermöglichen. 
+ Smart Homes
+ Automatisierung von Industrieanlagen
+ Gesundheitswesen (Überwachung)

## 2. Nenne und beschreibe mindestens drei Vorteile von MQTT.
+ **Geringe Bandbreite**: Minimiert die Größe von Nachrichten, was sich für Netzwerke mit geringer Bandbreite.
+ **Geringer Rechenaufwand**: Eignet sich auch für rechenschwächere Computer wie Micro-Controller, was die kosten senkt.
+ **Zuverlässige Verbindung**: Funktioniert auch in instabilen Netzwerken zuverlässig, was besonders in Industrieanlagen von Vorteil ist, um die Informationen von Sensoren zuverlässig zu erhalten.

## 3. Erkläre das Publish/Subscribe Pattern.
+ Daten werden z.B. von Sensoren an einen Broker gesendet. Diese sind dort public mit einem Topic versehen.
+ Andere Geräte Subscribern auf die Topics für die Daten, die für sie von Interesse sind. Der Broker informiert die Subscriber über Änderung der Daten und teilt ihnen die neue Daten mit.
+ Die komplette Kommunikation läuft also über den Broker ab.

## 4. 
### 4.1 Wann und wofür wurde MQTT entwickelt?
+ Zur Überwachung von ÖL-Pipelines
+ 1999 von IBM und Eurotech

### 4.2 Welche Herausforderungen gab es damals im ersten Projekt?
+ Instabile Netzwerke
+ Geringe Bandbreite
+ Trotzdem eine zuverlässige Kommunikation der Systeme gefordert

## 5. Seit wann ist MQTT ein internationaler Standard?
+ 2014

## 6. Wofür steht MQTT?
+ **M**essage **Q**ueuing **T**elemetry **T**ransport

## 7. Wie viele QoS Level gibt es bei MQTT?
Es sind 3 **Q**uality **o**f **S**ervice Level vorhanden.

## 8. Erkläre kurz die einzelnen Leveln bei MQTT
+ **At most once**: (QoS 0) Sender erwartet keine Empfangsbestätigung -> Nachricht wird einmal gesendet
+ **At least once**: (QoS 1) Kopie der Nachricht wird solange aufbewahrt, bis eine Empfangsbestätigung eingeht. Bei einer Zeitüberschreitung wird die Nachricht erneut gesendet. 
+ **Exactly once**: (QoS 2) 4-Way-Handshake, soll versichern, dass Nachrichten genau einmal verarbeitet werden.