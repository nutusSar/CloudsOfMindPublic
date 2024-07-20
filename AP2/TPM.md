---
tags:
  - "#AP2"
  - "#IT-Sicherheit"
---
## Definition
 Ein TPM ist ein spezieller Hardware-Chip, der zur sicheren Speicherung und Verwaltung von kryptografischen Schlüsseln und zur Durchführung von Verschlüsselungs- und Integritätsprüfungen verwendet wird. Es schützt Daten durch hardwarebasierte Sicherheitsmaßnahmen, sichert den Boot-Prozess und unterstützt die sichere Verwaltung von Zertifikaten und Passwörtern.

## Funktionalität und Aufgaben
+ **Kryptografische Schlüsselverwaltung**: TPM kann kryptografische Schlüssel sicher speichern und verwalten. Dies umfasst Schlüssel für Verschlüsselung, Entschlüsselung und digitale Signaturen.
+ **Sicherer Boot-Prozess**: TPM schützt den Boot-Prozess durch Verifizieren der Systemintegrität beim Hochfahren. Dies hilft, sicherzustellen, dass das Betriebssystem und die Systemsoftware nicht manipuliert wurden.
+ **Plattformintegritätsüberprüfung**: TPM kann zur Überprüfung der Integrität der Plattformkonfiguration verwendet werden, indem es Hash-Werte von Systemkomponenten speichert und vergleicht.

## Sicherheitsfunktionen
+ **Hardwarebasierte Verschlüsselung**: TPM führt Verschlüsselungs- und Entschlüsselungsoperationen direkt auf der Hardware durch, was die Sicherheit erhöht, da der Schlüssel nicht im Klartext gespeichert wird.
+ **Passwort- und Token-Schutz**: TPM kann zum Schutz von Passwörtern und Authentifizierungstoken verwendet werden, indem es diese sicher speichert und nur autorisierte Zugriffe zulässt.

## Anwendungen
+ **Datenschutz und -sicherheit**: TPM wird in modernen Computern und mobilen Geräten verwendet, um Daten durch hardwarebasierte Verschlüsselung zu schützen.
+ **Zertifikats- und Schlüsselmanagement**: TPM unterstützt das Management von digitalen Zertifikaten und kryptografischen Schlüsseln, die für verschiedene Sicherheitsprotokolle und -dienste benötigt werden.

## Vorteile von TPM
+ **Erhöhte Sicherheit**: TPM bietet zusätzlichen Schutz für Verschlüsselungsschlüssel und andere sicherheitsrelevante Daten durch hardware-isolierte Speicherung und Verarbeitungsmechanismen.
+ **Integritätsschutz**: TPM stellt sicher, dass das System beim Booten nicht durch Malware oder andere Angriffe kompromittiert wurde, indem es die Integrität des Systems überprüft.
+ **Zentralisierte Schlüsselverwaltung**: Durch die sichere Speicherung und Verwaltung von Schlüsseln in TPM können Unternehmen sicherstellen, dass Schlüssel nicht leicht gestohlen oder missbraucht werden können.

## Nachteile von TPM
+ **Kosten**: Die Integration von TPM-Chips kann zusätzliche Kosten für Hardware und Implementierung verursachen.
+ **Komplexität**: Die Nutzung und Verwaltung von TPM kann komplex sein und erfordert oft zusätzliche Software und Konfiguration, um die Vorteile vollständig zu nutzen.
+ **Kompatibilitätsprobleme**: Ältere Hardware und Software sind möglicherweise nicht mit TPM kompatibel, was zu Herausforderungen bei der Integration und Aktualisierung führen kann.
