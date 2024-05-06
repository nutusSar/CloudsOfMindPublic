---
tags:
  - "#Angular"
---
## Definition
Databinding ermöglicht die Kommunikation zwischen dem TS Code und dem HTML Template.


## Arten von Databinding
### Daten ausgeben
#### String Interpolation
```html
{{ data }}
```

Zwischen den geschweiften Klammern, kann jetzt eine TS-Expression, welche zu einem String evaluiert, geschrieben werden. Es ermöglicht also die einfache Ausgabe der Werte der Attribute einer Komponente. 

#### Property Binding
```html
[property]="data"
```

Es kann eine Eigenschaft eines HTML-ELements (Angular Komponenten und Direktiven sind auch möglich) in die eckigen Klassen geschrieben werden und mit einem Attribut der Komponente verknüpft werden.

**Beispiel**:
```html
<button [disabled]="isDisabled()">
```

### Auf User Events reagieren
#### Event Binding
```html
(event)="expression"
```

Zischen den runden Klammern kann ein Event des HTML-Elements eingetragen werden, welche dann mit TS-Code verknüpft wird.
$event ist eine reservierte Variable, welche als Argument einer Expression mitgegeben werden kann. Sie ermöglicht den Zugriff auf die Eventdaten.

**Beispiel**:
```HTML
<button (click)="onClick()">
```

### Kombinierung von Beidem
#### Two-Way-Binding
```html
[(ngModel)]="data"
```

In die Klammern muss eine Direktive, welche dann mit einem Attribut der Komponente verknüpft wird.
## Eigenschaften und Events
>[!tip]
>console.log() des Elements ermöglicht das Ausgeben der Eigenschaften und der Events.
>
>Anderweitig bietet die Seite von Mozilla Developer Network eine zentrale Anlaufstelle.







