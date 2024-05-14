---
tags:
  - "#Angular"
---

## Erstellen einer Komponente
Komponenten sollten immer in einem eigenem gleichnamigen Ordner hinterlegt werden. Damit Komponenten für Angular bekannt sind, müssen diese in der "app.module.ts" bei "@NgModule" deklariert werden.
Komponenten benötigen eine TS-Datei und ein Template, welche Inline oder eine HTML-Datei sein kann.
Für die automatische Generierung von Komponenten siehe [[CLI]].
## Selektor

### Als Element
```ts
selcctor: "selektor"
```

### Als Attribut
```ts
selector: '[selektor]' 
``` 

### Als Klasse
```ts
selector: '.selector'
```


## Lebenszyklen Hooks
>[!info] Laufzeit
> Die Hooks laufen in der Reihenfolge, wie sie unten aufgelistet sind (von oben nach unten).

### ngOnChanges
Wird immer aufgerufen, wenn sich eine der Attribute mit @Input ändert

### ngOnInit
Wird einmalig ausgeführt, wenn die Komponente initialisiert wurde. Läuft also nach dem Konstruktor. Die Komponente wurde aber noch nicht gerändert.

### ngDoCheck
Wird immer ausgeführt, wenn die Änderungsdetektion am durchlaufen ist. Das heißt, dass es bei jedem Check ausgeführt wird. 

### ngAfterContentInit
Wird immer ausgeführt, wenn der Content welcher über [[ng-content]] in die Komponente projiziert wird initialisiert wurde.

### ngAfterContentChecked
Wird immer ausgeführt, wenn der Content von [[ng-content]] auf Änderungen überprüft wurde.

### ngAfterViewInit
Wird aufgerufen, wenn die View der eigenen Komponente fertiggestellt wurde.

### ngAfterViewChecked
Wird ausgeführt, nachdem die View auf Änderungen überprüft wurde.

### ngOnDestroy
Wird einmalig unmittelbar vor der Zerstörung des Objektes / der Komponente ausgeführt.

