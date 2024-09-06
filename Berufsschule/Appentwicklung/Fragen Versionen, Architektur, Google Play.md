---
tags:
  - "#Appentwicklung"
---
## Versionen
### 1. Welche Version ist momentan die populärste? Welche die neuste?
+ **Neuste**: Android 14 (released), Android 15 (vorabversion, noch nicht released)
+ **Populärste**: Android 14 (28,11%)

### 2. **K**: Welche Version war ausschließlich für Tablets konzipiert?
+ Android 3 "Honeycomb"

### 3. **K**: Ab welcher Version gab es nur noch eine Version für Tablets und Smartphones?
+ Android 4 "Ice Cream Sandwich"

### 4. **K**: Nenne zwei Vorteile der aktuellsten Versionen 12 und 13
**Android 12**:
+ Einfacher zu sehen ob auf Kamera und Mikrofon zugegriffen wird
+ Personalisierte Benutzeroberflächen "Materials You"

**Android 13**:
+ Ausbau von "Materials You"
+ Verbesserung der Sicherheit z.B. durch eine Foto-API und eingeschränkten zugriff auf Benachrichtigungen

### 5. Was ist "Vulkan" ? (nein, nicht der Planet...)
Bei Vulkan handelt es sich um eine Low-Level-API für 3D Grafiken. Sie soll bessere Leistung und Effizienz für Grafikintensive Anwendungen/Spiele ermöglichen.

### 6. **K**:Ab welcher Android-Version wurde ein optisches Redesign durchgeführt ("Material Design")  und welche Darstellungseigenschaften hat dieses Design für Apps?
+ Android 5.0 Lollipop
+ Bietet flüssigere und dynamischere Benutzeroberflächen, Animationen sowie Schatten und Tiefenebenen wurden hinzugefügt

### 7. **K:** Welchen Zusammenhang gibt es zwischen einer Android-Version und dem API-Level?
API-Level bestimmen welche Funktionen den Entwickler zur Verfügung stehen. Mit neuen Android Versionen werden auch neue API-Level für die entsprechende Android Version veröffentlicht.

## Architektur
### 1. **K**: Welches bekannte Betriebssystem bildet die "Basis" für alle Android Versionen?
+ Linux

### 2. **K**: Was ist eine HAL?
+ Schnittstelle zwischen Hardware und Betriebssystem
+ Ermöglich den Zugriff auf die Hardware wie Kamera und Sensoren ohne technische Details zu kennen

### 3. **K**: Kann man Linux-Software einfach so auf Android portieren? (mit Begründung)
**Nein**:
+ Eigene Dateiformate für ausführbare Programme
+ Eigene Bibliotheken
+ Eigene Umgebung "Android Runtime" (ART)

### 5. **K**: Welche Sprachen sollte ich nutzen, wenn ich laufzeitkritische (also schnelle) Anwendungen in Android realisieren möchte?
+ C
+ C++

### 6. **K**: Warum ist es in Android möglich, eine eigene App für Kurznachrichten oder zum Telefonieren zu erstellen?
+ **Starke Modularität**: Komponenten des Systems (bis auf Virtuelle Maschinen und das Kernsystem) gleichberechtigt, ermöglicht Austausch der Komponenten (also auch das Einsetzen einer eigenen App zum Telefonieren oder zum Schreiben von Kurznachrichten).

### 7. **K**: Welche Bestandteile benötigt man, um eigene Programme für Android zu entwickeln?
+ Java-SDK
+ Android-SDK
+ beliebige Java-Entwicklungsumgebung

## Google Play, Software
### 1. Wie viele Apps sind momentan im Play Store?
+ 1.6 Millionen

### 2. **K**: Mit welcher App-Kategorie wird das meiste Geld verdient?
+ Spiele

### 3. Wie hoch ist der App-Umsatz voraussichtlich im Jahr 2024 in dieser Kategorie?
+ [91.570 Millionen](https://de.statista.com/outlook/amo/medien/videospiele/mobile-games/weltweit)

### 4. **K**: Kann man Apps nur in Google Play anbieten und verkaufen?
+ Nein, es gibt auch noch andere Plattformen und Märkte

### 5. 
#### a) Wie hoch ist der Umsatz von Android-Apps?
+ [42,3 Milliarden US $](https://de.statista.com/themen/882/apps-app-stores/#topicOverview)(2022)

#### b) Wie hoch ist der Umsatz von iOS-Apps im Vergleich?
+ [86,8 Milliarden US $](https://de.statista.com/themen/882/apps-app-stores/#topicOverview)(2022)

#### c) Vergleiche zusätzlich die Anzahl der Android und iOS-Geräte.
+ **Android**: [71,6%](https://de.statista.com/statistik/daten/studie/184335/umfrage/marktanteil-der-mobilen-betriebssysteme-weltweit-seit-2009/)(2024)
+ **iOS**: [27,75%](https://de.statista.com/statistik/daten/studie/184335/umfrage/marktanteil-der-mobilen-betriebssysteme-weltweit-seit-2009/)(2024)

#### d) Welche Schlussfolgerung lässt der Vergleich zu?
+ iOS Nutzer besitzen eine höhere Kaufkraft bzw. eine höhere Kaufbereitschaft