---
tags:
  - "#Angular"
---
## Definition
Im Gegensatz zu der lokalen Referenz, enthält View Chield ein ElementRef und nicht das komplette HTML-Element. Es ermöglicht direkten Zugriff auf Elemente in unserem Dom ohne Two-Way-Binding

```ts
@ViewChield('lokaleRefernz', {static: true}) htmlElement;

console.log(htmlElement.nativeElement.value)
```

>[!warning]
> Verändere Elemente nicht über @ViewChild, denn Angular bietet bessere Möglichkeiten, den Dom zu verändern (z.B. Databinding)

