---
tags:
  - "#Testing"
---
## Definition
Mockito ist ein mocking Framework für Unit-Tests in Java. Es ermöglicht das Simulieren des Verhaltens von Klassen und Funktionen. Es soll die Überprüfung mit dem Umgang gelieferter Werte ermöglichen, ohne die Logik von einer Klasse komplett in den Tests abbilden zu müssen. Somit werden externe Abhängigkeiten in den Unit-Tests entfernt, um eine kontrollierte Umgebung um das zu testende Objekt zu schaffen.
>[!warning]
>Mocke keinen Type, den du nicht selbst besitzt, z.B. beim Mocken einer Drittanbieter Bibliothek, kann es passieren, dass diese sich verändert, jedoch durch das Mocken keine Fehler geworfen werden und der Code trotzdem in der Produktion nicht funktioniert.



