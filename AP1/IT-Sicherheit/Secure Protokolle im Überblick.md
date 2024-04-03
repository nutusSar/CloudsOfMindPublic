---
tags:
  - "#AP1"
  - "#IT-Sicherheit"
---

## HTTPS (Hypertext Transfer Protocol Secure)
HTTPS ist eine sichere Variante des HTTP-Protokolls, das für die Übertragung von Daten im Web verwendet wird. Es integriert das Transport Layer Security (TLS)-Protokoll, um eine verschlüsselte Verbindung zwischen einem Webbrowser und einem Webserver herzustellen. Durch die Verschlüsselung werden die Vertraulichkeit und Integrität der übertragenen Daten gewährleistet, und HTTPS schützt vor Man-in-the-Middle-Angriffen.

### Schutz vor Man-in-the-Middle
HTTPS schützt vor Man-in-the-Middle-Angriffen durch die Implementierung von zwei entscheidenden Sicherheitsmechanismen: Verschlüsselung und Authentifizierung.

1. **Verschlüsselung:** HTTPS verwendet das Transport Layer Security (TLS)-Protokoll, um die Übertragung von Daten zwischen dem Webbrowser des Benutzers und dem Webserver zu verschlüsseln. Während der Kommunikation werden die Daten in einen undurchsichtigen Code (Chiffre) umgewandelt, der nur vom Webbrowser und dem Webserver entschlüsselt werden kann. Dies verhindert, dass ein Angreifer, der den Datenverkehr abfängt, den Inhalt verstehen kann.

2. **Authentifizierung:** Bei der Einrichtung einer HTTPS-Verbindung wird eine digitale Signatur verwendet, die durch ein digitales Zertifikat verifiziert wird. Das Zertifikat wird von einer vertrauenswürdigen Zertifizierungsstelle (CA) ausgestellt. Der Webserver präsentiert dieses Zertifikat dem Webbrowser, der dann die Signatur mit dem öffentlichen Schlüssel der CA überprüft. Dadurch wird sichergestellt, dass der Webbrowser tatsächlich mit dem beabsichtigten Webserver kommuniziert und nicht mit einem potenziell schädlichen Zwischenelement.

In einem Szenario ohne HTTPS könnte ein Angreifer versuchen, sich zwischen den Benutzer und den Server zu positionieren, um den Datenverkehr abzufangen oder zu manipulieren. Dies könnte beispielsweise durch Spoofing des DNS (Domain Name System) erreicht werden. Durch die Implementierung von HTTPS wird diese Art von Angriff erheblich erschwert.

## TLS (Transport Layer Security)
TLS, oder Transport Layer Security, ist ein Protokoll auf der Transportebene, das die Sicherung der Kommunikation über ein Netzwerk ermöglicht. Es bietet Verschlüsselung, Authentifizierung und Integritätsschutz für Datenübertragungen. TLS wird in verschiedenen Anwendungen eingesetzt, darunter HTTPS für die sichere Übertragung von Webdaten, SMTP für sichere E-Mail-Kommunikation und andere Anwendungen, die sichere Verbindungen erfordern.

### Funktionsweise
1. **Start der Kommunikation (ClientHello):** Die TLS-Verbindung beginnt mit dem Client, der eine Verbindung zum Server herstellen möchte. Der Client sendet eine "ClientHello"-Nachricht, in der er angibt, welche Verschlüsselungs- und Authentifizierungsalgorithmen er unterstützt.

2. **Antwort des Servers (ServerHello):** Der Server antwortet mit einer "ServerHello"-Nachricht, in der er aus den vom Client unterstützten Optionen auswählt. Diese Nachricht enthält auch das digitale Zertifikat des Servers, das von einer vertrauenswürdigen Zertifizierungsstelle (CA) ausgestellt wurde.

3. **Authentifizierung (Server Certificate):** Der Client überprüft das Zertifikat des Servers, um sicherzustellen, dass es echt ist und von einer vertrauenswürdigen CA ausgestellt wurde. Dadurch wird sichergestellt, dass der Client mit dem beabsichtigten Server kommuniziert und nicht mit einem potenziellen Angreifer.

4. **Schlüsselaushandlung (Key Exchange):** Client und Server führen eine Schlüsselaushandlung durch, um sicherzustellen, dass beide Parteien über einen gemeinsamen geheimen Schlüssel verfügen, der für die Verschlüsselung und Entschlüsselung der übertragenen Daten verwendet wird. Dies kann durch verschiedene Mechanismen erfolgen, einschließlich dem Diffie-Hellman-Schlüsselaustausch.

5. **Abschluss des Handshakes (Finished):** Nach der Schlüsselaushandlung senden sowohl der Client als auch der Server eine "Finished"-Nachricht, um den Abschluss des Handshakes zu bestätigen. Ab diesem Zeitpunkt wird die Kommunikation zwischen dem Client und dem Server durch die vereinbarten Verschlüsselungsalgorithmen geschützt.

6. **Datenübertragung (Verschlüsselte Kommunikation):** Nach dem erfolgreichen Handshake können der Client und der Server sicher miteinander kommunizieren. Die Datenübertragung erfolgt über eine verschlüsselte Verbindung, wodurch die Vertraulichkeit und Integrität der übertragenen Daten sichergestellt sind.

Während des gesamten Prozesses spielt das TLS-Protokoll eine zentrale Rolle bei der Sicherung der Kommunikation durch Verschlüsselung und Authentifizierung, wodurch ein sicherer Datenaustausch zwischen Client und Server ermöglicht wird.
## SSL/TLS-Protokollsuite
Die SSL/TLS-Protokollsuite besteht aus mehreren Protokollversionen, darunter SSL (Secure Sockets Layer) und die darauf aufbauenden TLS-Versionen (TLS 1.0, TLS 1.1, TLS 1.2, TLS 1.3). Diese Protokolle dienen dazu, die Sicherheit der Datenübertragung zu gewährleisten. TLS 1.3 ist die neueste Version, die Verbesserungen in Bezug auf Geschwindigkeit und Sicherheit bietet.

## SMTPS (Secure SMTP)
SMTPS ist eine Erweiterung des Simple Mail Transfer Protocol (SMTP) durch die Integration von TLS, um die E-Mail-Kommunikation zu sichern. Durch die Verwendung von TLS bei SMTPS wird eine verschlüsselte Verbindung zwischen E-Mail-Clients und -Servern hergestellt, um die Vertraulichkeit der übertragenen Nachrichten zu gewährleisten.

## FTPS (File Transfer Protocol Secure)
FTPS ist eine Erweiterung des File Transfer Protocol (FTP) unter Verwendung von TLS für die Sicherung von Dateiübertragungen. Es bietet eine verschlüsselte Übertragungsschicht, um sensible Daten vor unbefugtem Zugriff zu schützen. FTPS stellt eine sichere Alternative zum herkömmlichen FTP dar.

## XMPP over TLS (Extensible Messaging and Presence Protocol over TLS)
XMPP ist ein Protokoll für Instant Messaging und Präsenzinformation. Die Integration von TLS in XMPP stellt sicher, dass die Kommunikation zwischen den Instant-Messaging-Clients und -Servern verschlüsselt ist, um Datenschutz und Sicherheit zu gewährleisten.