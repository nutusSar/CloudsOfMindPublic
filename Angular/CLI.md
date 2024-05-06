---
tags:
  - Angular
topic: Commands
---
## Installieren von Angular
```CLI
npm install -g @angular/cli
```

>[!info]
> Für benutzen des Kommandos muss node.js installiert sein


## Neues Angular Projekt erstellen
Um ein neues Angular Projekt zu erstellen, öffne eine Bash in dem Ordner, in dem der Root-Ordner des Projektes liegen soll.
Anschließend wird dieser Befehl in die Bash eingegeben.
```bash
ng new <Project Name>
```
Die CLI erstellt dann ein Vanilla Angular Projekt. 
## Starten des Servers
Das Projekt kann jederzeit live im Browser nachverfolgt werden. Dafür wird folgender Command im Terminal eingegeben.
```bash
ng serve
```
Nach erfolgreichen Bauen des Projektes, wird unter **localhost:4200** die Angular Anwendung gehostet. Dabei handelt es sich um einen Liveserver, d.h., das Änderungen im Code direkt dargestellt werden.

## Komponente erstellen 
Die CLI ermöglicht das schnelle und einfache erstellen einer Komponente mit folgendem Command:
```bash
ng g c <optional: path to spicific folder + /><Component Name>
```
Dabei erstellt die CLI 4 Files in einem Ordner, der dem Komponenten Namen entspricht:
+ **.html:** Hier befindet sich das HTML für die Erstellung der Komponente
+ **.css:** Dieser File beinhaltet das Styling der Komponente
+ **.ts:** Dieser File beinhaltet die Logik der Komponente
+ **specs.ts:** Dabei handelt es sich um den File zum Testen der Komponente
