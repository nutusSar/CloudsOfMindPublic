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


