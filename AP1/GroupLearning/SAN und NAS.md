---
tags:
  - "#AP1"
  - "#Netzwerktechnik"
---
## Definition
Ein SAN ist ein lokales, aus mehreren Speichergeräten bestehendes Netzwerk, ein NAS hingegen ein einziges Storage-Gerät, das sich mit einem Local Area Network (LAN) verbindet.

## Gegenüberstellung 
### Eigenschaften
|Eigenschaft|SAN|NAS|
|---|---|---|
|Speichertyp|Blockbasiert|Dateibasiert|
|Netzwerk|Dediziertes Hochgeschwindigkeitsnetzwerk|Standardnetzwerk wie Ethernet|
|Protokolle|Fibre Channel, iSCSI|NFS, SMB|
|Anwendungen|Datenbanken, virtuelle Maschinen|Dateifreigabe, automatische Sicherung|
|Komplexität|Höher, erfordert spezielle Konfiguration|Niedriger, einfache Installation und Konfiguration|
|Performance|Hohe Leistung, niedrige Latenz|Geringfügig niedrigere Leistung im Vergleich zu SAN|
|Kosten|Höher aufgrund spezialisierter Hardware|Niedriger aufgrund weniger spezialisierter Hardware|

### Vor- und Nachteile
| **SAN** | **NAS** |
| ---- | ---- |
| Hohe Leistung und niedrige Latenzzeiten | Geringere Leistung im Vergleich zu SAN<br><br> |
| Skalierbarkeit und Flexibilität | Begrenzt auf Dateibasierte Zugriffe |
| Geeignet für anspruchsvolle Anwendungen wie Datenbanken und virtuelle Maschinen | Begrenzte Unterstützung für anspruchsvolle Anwendungen wie Datenbanken<br> |
| Höhere Kosten aufgrund spezialisierter Hardware und Netzwerkinfrastruktur | Geringe Kosten aufgrund weniger spezialisierter Hardware |
| Komplexere Installation und Konfiguration | Einfache Installation und Konfiguration<br> |
| Potenziell erhöhte Ausfallanfälligkeit aufgrund komplexer Netzwerktopologien | Ausfallsicherer |
