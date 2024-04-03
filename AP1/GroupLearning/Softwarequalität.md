---
tags:
  - "#AP1"
  - "#Softwareentwicklung"
---
## Tests

![[Testebenen[1388].png]]

### Modultests
Modultests dienen dazu einzelne Module oder Komponenten zu testen. Das geschieht in der Regel in Form eines White-Box Test durch Entwickler. (JUnit hilft z.B. bei der Automatisierung)

### Integrationstest
Integrationstest prüft die einzelnen Komponenten im Zusammenspiel. In der Regel werden Komponenten nach dem Modultest direkt mit einem Integrationstest auf Fehler in der Interaktion mit bestehenden Komponenten geprüft.

### Systemtest
Systemtest prüft die komplette Software gegen die definierten Anforderungen. In der Regel findet der Test auch in einem Testsystem statt, das die Produktionsumgebung nachbildet.

### Abnahmetest
Abnahmetest (auch User Acceptance Test) wird durch den Auftraggeber durchgeführt. Er prüft das Produkt auf die geforderte Funktionalität. Der Test findet i.d.R. als Black-Box Test statt.

### Black-Box vs. White-Box
| **Black-Box**                                               | **White-Box**                                                               |
| ----------------------------------------------------------- | --------------------------------------------------------------------------- |
| Keine Kenntnisse zu Code                                    | Testpersonen haben Kenntnisse zum Code und der Funktionsweise der Software. |
| getestet werden sichtbare Komponenten anhand Spezifikation. | Sehr einfach                                                                |
|                                                             | Fehlersuche                                                                 |

## Barrierefreiheit
### Beschreibe BITV 2.0
Barrierefreie-Informationstechnische Verordnung hat das Ziel, eine grundsätzliche barrierefreie Gestaltung moderner Informations- und Kommunikationstechnik zu ermöglichen.

### Wie ist Barrierefreiheit in der IT definiert?
Soll dafür sorgen, dass Webseiten, Programme und Betriebssysteme so gestaltet sind, dass auch Menschen mit körperlichen Einschränkungen sie bedienen können.
**Beispiele**:
+ Bilder mit Alternativtext
+ Aussagekräftige Struktur mit jeweils HTML-Tags
+ Navigierbarkeit ohne Maus
+ Text muss skalierbar sein

