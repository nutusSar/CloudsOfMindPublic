---
tags:
  - Angular
topic: Commands
---
## Installieren von Angular
```bash
npm install -g @angular/cli
```

>[!info]
> Für benutzen des Kommandos muss node.js installiert sein, denn die CLI benutzt node.js 


## Neues Angular Projekt erstellen
Um ein neues Angular Projekt zu erstellen, öffne eine Bash in dem Ordner, in dem der Root-Ordner des Projektes liegen soll.
Anschließend wird dieser Befehl in die Bash eingegeben.
```bash
ng new <Project Name> [--no-strict] [--standalone false] [--routing false]
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

## Installieren von Bootstrap 3
```Shell
npm install --save bootstrap@3
```

Der Befehl installiert Bootstrap lokal für das Projekt. Zusätzlich muss in der "angular.jason" in dem "styles"-Arrayder Pfad zu Bootstrap hinzugefügt werden "node_modules/bootstrap/dist/css/boosttrap.min.css".
