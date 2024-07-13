---
tags:
  - "#AP2"
---
## Dynamische Websites

### Definition
Dynamische Websites sind Websites, deren Inhalte sich basierend auf Benutzerinteraktionen oder anderen externen Faktoren ändern können. 

### Arten

#### CGI
+ **C**ommon **G**ateway **I**nterface ist ein Standardprotokoll, das es Webservern ermöglicht, externe Programme oder Skripte auszuführen um dynamische Inhalte zu generieren.
+ Mit CGI können Programme verschiedene Sprachen wie Perl, Python, C und anderen geschrieben werden um dynamische Inhalte wie Formulare, Suchfunktionen und Datenbankabfragen zu verarbeiten.

#### ASP
+ **A**ctive **S**erver **P**ages ist eine von Microsoft entwickelte Technologie, die es ermöglicht Webseiten mit serverseitigem Scripting zu erstellen.
+ Mit ASP können Entwickler Code in Skriptsprachen VBScript oder JScript einbetten, um dynamische generieren und mit Datenbanken zu interagieren.
+ ASP wird häufig mit Microsoft IIS (**I**nternet **I**nformation **S**ervices) verwendet.

#### JSP
+ **J**ava **S**erver **P**ages ist eine Java-Technologie, die es Entwicklern ermöglicht, dynamische Webseiten zu erstellen, indem sie Java-Code in HTML-Seiten einbetten.
+ JSP-Seiten werden auf einem Webserver ausgeführt und in Java-Servlets übersetzt, um dynamische Inhalte zu generieren und mit anderen Java-Technologien wie JDBC (**J**ava **D**atabase **C**onnectivity) zu integrieren.

#### PHP
+ Hypertext Preprocessor (ursprünglich **P**ersonal **H**ome**p**age Tools) ist eine serverseitige Skriptsprache, die speziell für die Entwicklung dynamischer Webseiten entwickelt wurde.
+ PHP-Skripte werden auf dem Webserver ausgeführt und können in HTML eingebettet werden, um dynamische Inhalte zu generieren, Formulare zu verarbeiten und mit Datenbanken zu interagieren.
+ PHP ist eine Open-Source-Technologie und wird auf einer Vielzahl von Webservern unterstützt, einschließlich Apache, Nginx und Microsoft IIS.

### Applet vs. Servlet
| **Applet**                                                         | **Servlet**                                                                                      |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| Wird im Webbrowser ausgeführt                                      | Wird auf dem Webserver ausgeführt                                                                |
| Haben Zugriff auf die lokalen Ressourcen des Benutzers             | Haben nur Zugriff auf die Serverressourcen                                                       |
| Entwicklung von interaktiven Anwendungen                           | Entwicklung von serverseitigen Webanwendungen                                                    |
| Erfordern einen Java-fähigen Webbrowser oder ein Java-Plug-in      | Benötigen dies nicht, werden in einer Containerumgebung auf dem Server ausgeführt                |
| Zugriff auf lokale Ressourcen -> anfälliger für Sicherheitsrisiken | Laufen auf dem Server und haben keinen direkten Zugriff auf die lokalen Ressourcen des Benutzers |
## Web 2.0
### Definition
Web 2.0 ist ein Schlagwort, das für eine Reihe interaktiver und kollaborativer Elemente des Internets, speziell des World Wide Webs, verwendet wird. Dabei konsumiert der Nutzer nicht nur den Inhalt, er stellt als Prosument selbst Inhalt zur Verfügung.

### Social Networks
Plattformen, die den Nutzern die Möglichkeit bieten, sich mit anderen Nutzern auszutauschen, Content zu erstellen, zu teilen und zu konsumieren.

### Wikis
Ein Wiki ist eine kollaborative Website oder eine Software, die es Benutzern ermöglicht, gemeinsam Inhalte zu erstellen, zu bearbeiten und zu organisieren.

### Blogs
Ein Blog ist eine Website oder Plattform, auf der Einzelpersonen oder Gruppen regelmäßig Einträge veröffentlichen, die als Beiträge bezeichnet werden.
### Twitter
Twitter ist eine Social-Media-Plattform, die es Benutzern ermöglicht, kurze Nachrichten, genannt Tweets, mit einer maximalen Länge von 280 Zeichen zu veröffentlichen.

### Forum 
Ein Forum ist eine Online-Diskussionsplattform, auf der Benutzer Beiträge veröffentlichen, auf Beiträge anderer Benutzer antworten und so an Diskussionen zu verschiedenen Themen teilnehmen können.

### Podcast  
Ein Podcast ist eine Serie von digitalen Audio- oder Videodateien, die über das Internet gestreamt oder heruntergeladen werden können

## Web 3.0
Web 3.0 ist ein Begriff, der verschiedene Konzepte und Entwicklungen beschreibt, die das Internet in eine neue Phase seiner Evolution führen sollen. Im Vergleich zu Web 2.0, das sich auf die Einführung von sozialen Netzwerken, User-generated Content und kollaborative Plattformen konzentrierte, zielt Web 3.0 darauf ab, das Internet zu einem stärker dezentralisierten und datenorientierten Ökosystem zu machen.


## RIA 
### Definition
**Rich Internet Application**
- RIA sind Webanwendungen, die reichhaltige Benutzeroberflächen und Interaktivität bieten, ähnlich wie traditionelle Desktop-Anwendungen.
- Sie verwenden häufig moderne Webtechnologien wie HTML5, CSS3 und JavaScript, um ansprechende Benutzeroberflächen, Animationen und Effekte zu erstellen.
- RIA ermöglichen eine verbesserte Benutzererfahrung durch schnelle Antwortzeiten, Echtzeitaktualisierungen und eine nahtlose Interaktion mit dem Benutzer.
- Sie bieten Funktionen wie Drag-and-Drop, automatische Vervollständigung, Kontextmenüs und vieles mehr, um die Benutzerfreundlichkeit zu verbessern.
- Beispiele für RIA sind Google Maps, Gmail, Trello und Spotify Web Player.

### Vor- und Nachteile
| **Vorteile**                                                                                                                                             | **Nachteile**                                          |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| Oft benutzerfreundlicher als klassische Webanwendungen durch die Verwendung moderner Interaktionstechniken (z. B. Drag and Drop).                        | Evtl. lange Download- und Ladezeiten.                  |
| Schnellere Reaktion auf Benutzereingaben durch lokale, client-seitige Verarbeitung.                                                                      | Höhere Ressourcenbelastung des Clientrechners möglich. |
| Keine „Cross-browser issues“ (durch den Einsatz von speziellen RIA-Frameworks).                                                                          | Manchmal Installation eines Plug-ins notwendig.        |
| Reduzierte Server- und Netzwerklast durch lokale Berechnungen.                                                                                           | Evtl. Sicherheitslücken durch installierte Plug-ins.   |
| Gegebenenfalls Zugriff auf lokales Dateisystem und Peripherie.                                                                                           |                                                        |
| Oft einfache GUI-Entwicklung durch reichhaltige UI-Komponenten, die in RIA-Frameworks enthalten sind („Viel WOW!-Effekt ohne viel Aufwand“).             |                                                        |
| Bei Plug-in-basiertem System mehr Performance möglich im Gegensatz zu reinen DHTML-Varianten. Keine Abhängigkeit von der JavaScript-engine des Browsers. |                                                        |

## AJAX 
**Asynchronous JavaScript and XML**
- AJAX ist eine Technik, mit der Webanwendungen Daten vom Server abrufen und anzeigen können, ohne die gesamte Seite neu zu laden.
- Sie ermöglicht es, dass Benutzeraktionen wie Klicken auf Schaltflächen oder Ausfüllen von Formularen asynchron verarbeitet werden, indem nur die erforderlichen Teile der Seite aktualisiert werden.
- AJAX verwendet JavaScript, um XMLHttpRequests zu erstellen und Daten im Hintergrund auszutauschen, normalerweise im JSON- oder XML-Format.
- Diese Technik verbessert die Leistung und Reaktionsfähigkeit von Webanwendungen, da sie weniger Bandbreite und Ladezeiten benötigen und eine interaktivere Benutzererfahrung ermöglichen.
- AJAX wird häufig zusammen mit anderen Webtechnologien wie HTML, CSS und serverseitigen Skriptsprachen wie PHP, Python oder Ruby verwendet.

### Vor- und Nachteile
| **Vorteile**                       | **Nachteile**                                                                      |
| ---------------------------------- | ---------------------------------------------------------------------------------- |
| Kein Neuladen aufgebauter Seiten   | Umfangreiche Tests erforderlich                                                    |
| Kein Browser-Plug-in wird benötigt | Verwendung der „Zurück“-Schaltfläche nicht möglich                                 |
| Serverseitige Browsererkennung     | Polling-Problem                                                                    |
| Verbesserte Benutzerinteraktion    | Ein Lesezeichen auf einen bestimmten Zustand der Seite zu setzen ist nicht möglich |
| Reduzierter Bandbreitenverbrauch   | Barriere für Suchmaschinenoptimierung (SEO)                                        |

## Anforderrungen durch Mobilgeräte
### Offline-Fähigkeit
- Webanwendungen sollten Mechanismen für die Offline-Nutzung bieten, da Mobilgeräte oft in Bereichen mit schlechter oder keiner Netzabdeckung verwendet werden.
- Die Verwendung von Technologien wie Service Workers und lokale Speicherung ermöglicht es, bestimmte Funktionen auch ohne Internetverbindung verfügbar zu machen.

### Deployment auf mehrere Plattformen
- Entwickler müssen sicherstellen, dass ihre Anwendungen auf verschiedenen mobilen Plattformen wie iOS und Android lauffähig sind.
- Die Verwendung plattformübergreifender Entwicklungswerkzeuge wie React Native oder Xamarin kann die Entwicklung und Wartung erleichtern.

### Verschiedene Programmiersprachen
- Entwickler sollten in der Lage sein, verschiedene Programmiersprachen wie Swift für iOS und Kotlin für Android zu beherrschen, um native Apps zu entwickeln.
- Alternativ kann die Verwendung von Webtechnologien wie HTML5, CSS und JavaScript für plattformübergreifende Anwendungen eine effiziente Lösung sein.

### Native Apps vs. HTML5/JavaScript
- Native Apps bieten oft eine bessere Leistung und Benutzererfahrung, da sie speziell für die jeweilige Plattform optimiert sind.
- HTML5/JavaScript-basierte Anwendungen bieten hingegen plattformübergreifende Kompatibilität und eine schnellere Entwicklungszeit, sind jedoch möglicherweise nicht so leistungsfähig wie native Apps.

### Geringe Bandbreiten
- Mobilgeräte haben oft Einschränkungen bei der Bandbreite, insbesondere in ländlichen Gebieten oder bei der Nutzung von Mobilfunknetzen.
- Die Optimierung von Datenübertragungen durch Komprimierung, Zwischenspeicherung und minimale Datenübertragungen kann helfen, die Auswirkungen geringer Bandbreiten zu minimieren.

### Kleine Auflösungen
- Mobilgeräte haben kleinere Bildschirme und niedrigere Auflösungen im Vergleich zu Desktop-Computern.
- Webdesign sollte für kleinere Bildschirme optimiert werden, indem Responsive Design-Techniken verwendet werden, um sicherzustellen, dass Inhalte gut lesbar und benutzerfreundlich bleiben.

## Angriffsmöglichkeiten gegen Anwendungen Abgrenzen
### SQL-Injection 
- Bei SQL-Injection werden schädliche SQL-Abfragen in Eingabeformulare oder URL-Parameter eingeschleust, um auf die zugrunde liegende Datenbank zuzugreifen oder sie zu manipulieren.
- Die Abwehr erfolgt durch die Verwendung von parametrisierten Abfragen oder durch die Verwendung von ORM-Frameworks (Object-Relational Mapping), die SQL-Injection-Angriffe automatisch verhindern können.

### XSS
- Bei XSS-Injektionen werden bösartige Skripte in Webseiten eingefügt, die von Benutzern ausgeführt werden, die die manipulierten Seiten besuchen.
- Zur Abwehr sollten Eingaben von Benutzern immer korrekt validiert und sanitisiert werden, bevor sie an den Browser gesendet werden. Content Security Policy (CSP) kann auch verwendet werden, um XSS-Angriffe zu verhindern.

### CSRF
- CSRF-Angriffe zielen darauf ab, dass ein Benutzer ohne sein Wissen eine schädliche Aktion auf einer Webseite ausführt, auf die er authentifiziert ist.
- CSRF-Token sollten in Formularen verwendet werden, um sicherzustellen, dass Aktionen nur von autorisierten Benutzern durchgeführt werden können.

### Session Hijacking
- Bei einem Session-Hijacking greift ein Angreifer auf die Session-ID eines Benutzers zu und übernimmt dadurch dessen Sitzung, um auf geschützte Ressourcen zuzugreifen.
- Zur Abwehr sollten Sessions sicher implementiert werden, z.B. durch die Verwendung von HTTPS, das automatische Ablaufdatum von Sitzungen und die Speicherung sensitiver Daten wie Passwörter in verschlüsselter Form.

### DoS
- Bei DoS-Angriffen versucht ein Angreifer, eine Anwendung oder einen Dienst durch Überlastung mit einer großen Anzahl von Anfragen lahmzulegen.
- Zur Abwehr können Firewalls, Lastenausgleich und Rate-Limiting eingesetzt werden, um den Datenverkehr zu steuern und Angriffe zu erkennen.

### DDoS
- DDoS-Angriffe sind ähnlich wie DoS-Angriffe, jedoch werden sie von mehreren Quellen gleichzeitig ausgeführt, was die Abwehr erschwert.
- Zur Abwehr können spezialisierte DDoS-Schutzdienste, Cloud-basierte Sicherheitslösungen und die Zusammenarbeit mit Internetdienstanbietern eingesetzt werden, um den Datenverkehr zu filtern und zu stoppen.

## HTTP
### Methods
#### Safe
- Eine HTTP-Methode wird als "safe" bezeichnet, wenn sie keine Auswirkungen auf den Zustand des Servers oder der Ressource hat.
- Das bedeutet, dass eine "safe" Methode eine Anfrage an den Server senden kann, ohne den Zustand der Ressource zu ändern oder Daten zu modifizieren.
- Beispiele für "safe" Methoden sind GET und HEAD, da sie lediglich Informationen von einem Server anfordern, ohne Daten zu ändern.

#### Idempotent
- Eine HTTP-Methode ist "idempotent", wenn sie bei wiederholter Ausführung mit denselben Eingaben dasselbe Ergebnis liefert, ohne zusätzliche Auswirkungen zu haben.
- Mit anderen Worten, eine "idempotent" Methode kann mehrmals ausgeführt werden, ohne den Endzustand zu verändern, sofern die Eingaben gleich bleiben.
- Beispiele für "idempotent" Methoden sind GET, HEAD, PUT und DELETE. PUT und DELETE können mehrmals hintereinander aufgerufen werden, ohne den Zustand der Ressource zu ändern, solange die Eingaben gleich bleiben.

### Statuscodes
1. **200 OK:**
    
    - Die Anfrage wurde erfolgreich bearbeitet und die Antwort enthält die angeforderten Daten.
2. **201 Created:**
    
    - Die Anfrage wurde erfolgreich bearbeitet und eine neue Ressource wurde erstellt. Die URL der neuen Ressource wird normalerweise in der Antwort angegeben.
3. **400 Bad Request:**
    
    - Die Anfrage konnte aufgrund eines ungültigen Clientanforderungssyntax nicht verarbeitet werden.
4. **401 Unauthorized:**
    
    - Die Anfrage erfordert eine Authentifizierung des Clients, die jedoch fehlgeschlagen ist oder nicht bereitgestellt wurde.
5. **403 Forbidden:**
    
    - Der Server hat die Anfrage des Clients verstanden, verweigert jedoch die Autorisierung für den Zugriff auf die angeforderte Ressource.
6. **404 Not Found:**
    
    - Die angeforderte Ressource wurde auf dem Server nicht gefunden.
7. **405 Method Not Allowed:**
    
    - Die Methode, die in der Anfrage verwendet wurde, ist für die angeforderte Ressource nicht zulässig.
8. **500 Internal Server Error:**
    
    - Ein allgemeiner Fehler ist auf dem Server aufgetreten, der die Bearbeitung der Anfrage verhindert hat.
9. **503 Service Unavailable:**
    
    - Der Server ist vorübergehend nicht in der Lage, die Anfrage zu bearbeiten, da er überlastet ist oder für Wartungsarbeiten offline ist.

---
## Backlinks
[[AP2]]

