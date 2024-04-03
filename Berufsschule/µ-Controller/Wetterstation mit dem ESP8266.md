---
autor: Jonas Klas
tags:
  - "#µ-Controller"
  - "#Berufsschule"
topic: 1. Projektarbeit, Doku
---
## Einleitung
Im Unterrichtsfach "Microcontroller" haben wir den Auftrag erhalten, ein Projekt namens "Wetterstation" zu realisieren. Vor diesem Projekt haben wir uns intensiv mit verschiedenen Funktionen des ESP8266 befasst und haben uns mit der Arduino IDE vertraut gemacht. Zur Erweiterung des ESP8266 haben wir einen DHT11-Sensor sowie ein OLED-Display integriert.

## Grundanforderung
- Der DHT11-Sensor wird zur Messung der Temperatur und Luftfeuchtigkeit eingesetzt.
- Der bereits vorhandene LDR dient der Erfassung der Helligkeit.
- Die gemessenen Werte werden auf dem OLED-Display angezeigt.
- Wenn die Temperatur unter 4°C liegt, wird eine Schneeflocke eingeblendet.
- Bei einer Luftfeuchtigkeit über 80% werden Regentropfen angezeigt.
- Abhängig von der Helligkeit erscheint entweder eine Sonne oder ein Mond.

## Hardware
Folgende Komponenten wurden für die Umsetzung der Wetterstation benötigt:
+ ESP8266
+ DHT11
+ OLED-Display
+ Platinen, welche von Herr. Wintgen angefertigt wurden (Bluetooth- und OLED-Shield).


## Aufbau der Projektstruktur
+ **WetterStation.ino:** Eigentlicher Programmcode für den ESP8266
+ **IndexPage.h:** HTML und JS für die Webseite
+ **Moon.h, Sun.h, WaterDroplets.h, SnowFlake.h und Flame.h:** Grafiken, die auf dem Display dargestellt werden.

## Programm
Die Umsetzung der Grundanforderung gestaltete sich als relativ einfach mit wenigen Problemen, da das Unterrichtsmaterial gute Dokumentationen und Tipps zur Umsetzung dieser bereitstellte.

Es müssen vorab verschiedene Bibliotheken installiert und hinzugefügt werden:
+ Adafruit NeoPixel
+ Adafruit SSD1306
+ Adafruit Unified Sensor
+ DHT sensor library

### Messen von Werten
#### Schritt 1
Im ersten Schritt analysieren wir die drei verschiedenen Sensoren (eigentlich nur zwei, jedoch drei Messwerte) und definieren die benötigten Parameter.
```C++
#define DHT_PIN D5
#define DHT_POWER D0
#define DHT_TYPE DHT11
DHT dht(DHT_PIN, DHT_TYPE);

const int LDR_PIN = A0;
```
Dabei werden die Pins sowohl für die Stromversorgung als auch für die Daten festgelegt, und es wird ein DHT-Objekt instanziiert.

#### Schritt 2
Im Setup werden die Stromversorgung des DHT11-Sensors freigegeben und dieser eingeschaltet. Dies geschieht über folgende Zeilen:
```C++
  pinMode(DHT_POWER, OUTPUT);
  digitalWrite(DHT_POWER, HIGH);
  dht.begin();
```

#### Schritt 3
Im Loop-Teil des Programms erfolgt nun der Aufruf der Funktionen zur Messung der Temperatur, Feuchtigkeit und Helligkeit.
```C++
temp = dht.readTemperature();
humi = dht.readHumidity();
light = analogRead(LDR_PIN);
```
Die gemessenen Werte werden in zuvor definierten Variablen gespeichert.

### Darstellung von Werten 
Die Werte werden nun gemessen, aber ihre Darstellung fehlt, was ihren Nutzen einschränkt. Dies wurde durch die Einbeziehung der Display-Funktionalität behoben, die es ermöglicht, die Werte mit passenden Grafiken darzustellen und hervorzuheben.
#### Schritt 1
Wie zuvor wurden verschiedene Werte definiert, darunter die Bildschirmdimensionen in Pixeln sowie der Resetpin. Ein Display-Objekt wurde erstellt, das diese Informationen enthält.
```C++
#define SCREEN_WIDTH 128
#define SCREEN_HEIGHT 64
#define OLED_RESET 0
Adafruit_SSD1306 display(SCREEN_WIDTH, SCREEN_HEIGHT, &Wire, OLED_RESET);
```

#### Schritt 2
Im Setup wird das Display erstmalig eingeschaltet und das Logo des Displays erscheint. Anschließend wird der Buffer des Displays für die weitere Nutzung gelöscht.
```C++
display.begin(SSD1306_SWITCHCAPVCC, 0x3C);
display.display();
display.clearDisplay();
```

#### Schritt 3
Im dritten Schritt werden die zuvor gemessenen Daten als Text auf das Display übertragen und dargestellt. Abhängig von den gemessenen Werten werden entsprechende Grafiken über einen if/else-Block eingeblendet.
```C++
// DISPLAYING THE DATA
display.clearDisplay();
display.setTextSize(1);
display.setTextColor(WHITE);
display.setCursor(0, 0);
display.println("Temperature: " + String(temp) + (char)247 + "C\nHumidity: " + String(humi) + "%\nLight: " + String(light)); 

if(humi > 80){
	display.drawXBitmap(21, 43, WaterDroplets_bits, WaterDroplets_width, WaterDroplets_height, WHITE);
}
if (temp < 4){
	display.drawXBitmap(0, 43, SnowFlake_bits, SnowFlake_width, SnowFlake_height, WHITE);
}
else{
	display.drawXBitmap(0, 43, Flame_bits, Flame_width, Flame_height, WHITE);
}
if (light < 100){
	display.drawXBitmap(43, 43, Moon_bits, Moon_width, Moon_height, WHITE);
}
else{
	display.drawXBitmap(43, 43, Sun_bits, Sun_width, Sun_height, WHITE);
}

display.display();
```
Im Code ergeben sich zwei Besonderheiten: Zum einen mussten die Bilder zuvor als XBitmap-Bild abgespeichert werden, damit das Display sie verwenden konnte. Zum anderen konnte man nicht einfach das °-Symbol als Text an das Display übergeben. Das Display verfügt nur über einen begrenzten Zeichensatz, der stark an die CP437 erinnert, mit Ausnahme des Zeichens 0xB0. Das °-Symbol verbirgt sich daher hinter dem Code 0xF7 (dezimal 247).
![[Pasted image 20240205003037.png]]
(links der Default Zeichensatz, des Displays, rechts die CP 437 )

### Besonderheiten 
Um die Daten nicht permanent zu messen, wird ein Intervall von 10 Sekunden verwendet. In einer If-Bedingung wird überprüft, ob 10 Sekunden vergangen sind. Wenn dies der Fall ist, werden neue Werte gemessen und das Display entsprechend aktualisiert. Die Verwendung einer If-Bedingung anstelle eines Delays hat einen besonderen Grund, auf den ich später eingehen werde.

### Fazit
Die Grundanforderungen sind erfüllt: Es werden drei Werte in einem regelmäßigen Intervall gemessen und auf dem OLED-Display dargestellt, dabei werden sie mit Grafiken veranschaulicht. Die Umsetzung gestaltete sich als relativ einfach, da das bereitgestellte Lernmaterial alle nötigen Informationen und Kommandos beinhaltet. Die Darstellung der Werte auf dem Display lässt jedoch Raum für Verbesserungen, und eine eigene Webseite könnte eine ansprechendere Lösung bieten.


## Erweiterung 

### ESP8266 als Accesspoint 
Für die Erweiterung unseres Projekts "Wetterstation" entschied ich mich, einen Webserver auf dem ESP8266 laufen zu lassen, um die Wetterdaten auch über eine geringe Entfernung zugänglich zu machen. Zunächst wählte ich die Option, den ESP als Access Point zu nutzen, was sich als äußerst praktisch erwies. Dadurch konnte ich eine direkte Verbindung zu meinem ESP herstellen, ohne auf ein bestehendes WLAN-Netzwerk angewiesen zu sein. Die Implementierung erfolgte reibungslos, und ich konnte die gemessenen Daten problemlos über einen Webbrowser auf meinem Handy abrufen.

Das Schlüsselstück dieser Lösung war die Möglichkeit, eine Webseite direkt vom ESP an mein Handy zu senden. Dies ermöglichte es mir, die aktuellen Wetterdaten komfortabel und in Echtzeit auf meinem mobilen Gerät zu visualisieren. Diese Methode erwies sich als äußerst praktisch, da sie es mir erlaubte, die Wetterinformationen bequem von jedem Ort aus abzurufen, solange ich mich in Reichweite des ESP befand. Diese Erweiterung des Projekts verbesserte die Zugänglichkeit der Wetterdaten erheblich und trug zu einer insgesamt benutzerfreundlicheren Erfahrung bei.
Nachdem ich den ESP als Access Point eingerichtet hatte und erfolgreich eine Verbindung zu meinem Handy herstellen konnte, wurde deutlich, wie wichtig es war, dass die Messung der Daten nicht blockierend war. Ein blockierender Messvorgang hätte zur Folge gehabt, dass der Webserver des ESP auf eingehende Anfragen nicht hätte antworten können. Daher war es entscheidend, eine nicht-blockierende Messung zu implementieren, um sicherzustellen, dass der ESP gleichzeitig sowohl die Daten erfassen als auch auf Anfragen reagieren konnte. Umgesetzt durch die vorhin genannte If-Bedingung, anstatt des Delays.

### Erdkunde LK und das Wetterdiagramm
Da ich Erdkunde als Leistungskurs hatte, war es mir wichtig, eine 24-Stunden-Historie der Wetterdaten mit der üblichen Diagrammdarstellung zu erstellen. Anfangs erwog ich die Verwendung von Matplotlib in Python für diese Aufgabe. Allerdings stieß ich schnell auf die Herausforderung, wie ich Python auf dem ESP8266 oder im Browser einsetzen könnte, was diese Idee unpraktikabel machte.

Daraufhin kam mir die Idee, eine JavaScript-Library zu nutzen, um die Diagramme zu erstellen. Nach einigem Recherchieren entschied ich mich für die Verwendung von D3.js by Observables, einer Plattform für interaktive Datenvisualisierung und -analyse im Webbrowser. Diese Lösung schien ideal, da sie es mir ermöglichte, die Daten direkt im Browser zu visualisieren und gleichzeitig die Flexibilität und Leistungsfähigkeit von D3.js auszunutzen.

### Das Problem mit ESP8266 als Accesspoint
Jedoch ergab sich daraus ein Problem: Um diese Visualisierung in meine Webseite einzubinden, benötigte man einen Internetzugang. Das bedeutete, dass der ESP8266 nicht mehr als Access Point fungieren konnte, sondern sich stattdessen mit einem Access Point verbinden musste, der Internetzugang bereitstellt. Damit wurde die Konfiguration komplexer, da der ESP8266 nun in ein vorhandenes WLAN-Netzwerk eingewählt werden musste, um auf die erforderlichen Ressourcen und Daten zugreifen zu können.

### Ergänzung des Codes

#### Schritt 1
Nachdem ich mich mit D3.js vertraut gemacht hatte, erstellte ich die gewünschte Vorlage des Wetterdiagramms. Allerdings fehlten zu diesem Zeitpunkt noch die tatsächlichen Messwerte. Ich konzentrierte mich zunächst darauf, die Struktur und das Design des Diagramms gemäß meinen Vorstellungen umzusetzen. Dies ermöglichte es mir, eine klare Vorstellung davon zu bekommen, wie die Daten später in das Diagramm integriert werden könnten, und erleichterte mir die weitere Entwicklung des Projekts.
![[Pasted image 20240205010441.png]](Leeres Wetterdiagramm, letzten 24h mit Luftfeuchtigkeit auf der linken Seite und Temperatur auf der rechten)

#### Schritt 2
Nachdem ich das Diagramm verbessert und erste Dummydaten getestet hatte, fügte ich den Code zur Ergänzung der Webseite als Datei meinem ESP8266-Projekt hinzu. Diese Datei speicherte ich in einer Variable im PROGMEM-Bereich des Programms. Damit war die Webseite und das Diagramm direkt im Programm des ESP8266 enthalten und konnten bei Bedarf einfach abgerufen und angezeigt werden, ohne auf externe Ressourcen zugreifen zu müssen.
![[Pasted image 20240207211433.png]]

(Endgültiges aussehen des Diagrammes)

![[Pasted image 20240205010859.png]](Vorbild des Diagrammes (https://www.klimadiagramme.de/Deutschland/Plots/freiburg.gif))

#### Schritt 3
Im letzten Schritt erstellte ich ein Array mit 194 Plätzen, wobei jeweils zwei Plätze einen Wert für Temperatur und Luftfeuchtigkeit enthalten. Da alle 15 Minuten eine Messung erfolgt, ergibt sich dies aus 24 Stunden multipliziert mit 4 Messungen pro Stunde und 2 Werten pro Messung (192 + 2 wegen 0h). In der Webseite fügte ich entsprechenden JavaScript-Code hinzu, der mithilfe des zuletzt gespeicherten Index das Array rückwärts auswertet und die Werte zum richtigen Zeitpunkt in das Diagramm einträgt. Diese Datenverarbeitung findet im Browser statt, da dieser auf leistungsfähigeren Geräten ausgeführt wird als der ESP8266 und somit besser geeignet ist, um die erforderlichen Berechnungen durchzuführen.

## Verbesserung 
Zur Verbesserung des Projekts gibt es zwei entscheidende Punkte. Zum einen wäre die Erweiterung des ESP8266 um mehr Speicher, um eine noch langfristigere Historie der Wetterdaten zu ermöglichen. Dadurch könnten mehr Daten über längere Zeiträume gespeichert und analysiert werden, was eine detailliertere Auswertung und bessere Vorhersagen ermöglichen würde.

Zum anderen wäre die Anpassung des ESP8266-Codes für die Bildung von Durchschnittswerten anstatt von Rohwerten ein wichtiger Schritt. Durch die Berechnung von Durchschnittswerten über einen bestimmten Zeitraum könnten genauere und stabilerere Daten erfasst werden, was die Genauigkeit der Wettervorhersage verbessern würde. Diese beiden Punkte würden das Projekt deutlich leistungsfähiger machen und seine Anwendungsbereiche erweitern.

## Fazit
Insgesamt war die Entwicklung und Umsetzung des Projekts "Wetterstation" äußerst lehrreich und spannend. Angefangen von der Einbindung verschiedener Sensoren bis hin zur Implementierung eines Webservers auf dem ESP8266 gab es zahlreiche Herausforderungen zu bewältigen. Die Entscheidung, die Wetterdaten nicht nur lokal auf dem Display, sondern auch über eine Webseite verfügbar zu machen, erwies sich als äußerst sinnvoll, da dies die Zugänglichkeit und Benutzerfreundlichkeit des Systems deutlich verbesserte.

Die Integration von D3.js und Observable für die Erstellung des Wetterdiagramms stellte eine interessante Lösung dar und ermöglichte es, die gemessenen Daten ansprechend und interaktiv darzustellen. Die Tatsache, dass die Datenverarbeitung und Darstellung im Browser erfolgte, bot eine flexible und leistungsfähige Plattform für die Visualisierung der Wetterdaten.

Insgesamt bin ich mit dem Ergebnis des Projekts sehr zufrieden und habe viel darüber gelernt, wie man komplexe Systeme mit Mikrocontrollern und Webtechnologien entwickeln kann. Das Projekt hat mein Verständnis für die Anwendung von IoT-Technologien erweitert und mir wertvolle Erfahrungen in der Entwicklung von Embedded-Systemen sowie in der Webentwicklung gebracht.
