---
tags:
  - "#Angular"
---
## Problem 
Alles was zwischen dem öffnendem und schließendem Tag einer eigenen Komponente geschrieben ist, wird nicht gerändert.
## Lösung
In der Komponente, welche HTML-Code zwischen ihrem öffnendem und schließendem Tag enthält, wird ein ng-content hinzugefügt, an der Stelle wo der HTML-Code gerändert werden soll.

```html
<meine-komponente>mein HTML</meine-komponente>
```

```html 
<!-- meine-komponente template -->
<div>
	<ng-content></ng-content>
</div>
```

## @ContentChild
Ermöglicht die ElementRef von einem HTML-Element innerhalb der Komponente zu erhalten, zwischen dessen öffnendem und schließendem Tag sich das HTML-Element befindet.

