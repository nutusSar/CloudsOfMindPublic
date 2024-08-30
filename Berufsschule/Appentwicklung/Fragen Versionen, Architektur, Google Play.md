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
+ Einfacher zu sehen ob auf auf Kamera und Mikrofon zugegriffen wird
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

### 3. 1. **K**: Kann man Linux-Software einfach so auf Android portieren? (mit Begründung)
**Nein**:
+ Eigene Dateiformate für ausführbare Programme
+ Eigene Bibliotheken
+ Eigene Umgebung "Android Runtime" (ART)