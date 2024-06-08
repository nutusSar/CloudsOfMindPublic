## Definition

## Über CLI einrichten 
### Schritt 1
Mit dem folgenden Kommando den Routing Prozess auf den einzelnen Routern starten 
```CLI
Router(config)# router ospf <process id>
```

### Schritt 2
Danach die RouterID der einzelnen Router festlegen. Eine RouterID könnte wie folgt aussehen: 1.1.1.1 oder 2.2.2.2 ...
```CLI
Router(config-router)# router-id <rid>
```

### Schritt 3
Danach kann das OSPF-Routing auf 3 verschiedene Arten konfiguriert werden:
#### Möglichkeit 1: Routing mittels Netzwerkbefehlen und Platzhaltermasken
Es muss die Platzhaltermaske (Wildcard) berechnet werden. Dies geschieht durch das Invertieren der Subnetzmaske. Dabei wird aus der Subnetzmaske 255.255.255.0 die Wildcard 0.0.0.255 oder aus 255.255.255.252 wird 0.0.0.3.
Anschließend kann mit folgenden Befehl für jedes Netzwerk des Routers das OSPF Routing eingeschaltet werden.
```CLI
Router(config-router)# network <network-address> <wildcard-mask> area <area-id>
```

#### Möglichkeit 2: Routing mittels Quad-Zero-Maske
Der Befehl ist zu dem obigen gleich, jedoch wird die IP der Schnittstelle anstatt der Netzwerkadresse verwendet. Bei der Platzhaltermaske wird immer 0.0.0.0 eingetragen.

#### Möglichkeit 3: Konfigurieren mittels Routing auf Router Schnittstellen
Mit folgendem Befehl kann das Routing direkt über die Interfaces konfiguriert werden, d.h. der Router zieht sich die benötigten Informationen direkt aus der Schnittstelle. Somit muss keine Wildcard, Netzwerkadresse oder IP der Schnittstelle angeben werden.
```CLI
Router(config-if)# ip ospf <process-id> area <area-id>
```

### Schritt 4
Da OPSF Protokollverkehr aus allen Schnittstellen sendet, müssen zur Reduzierung des Traffics alle Schnittstellen, die nicht mit anderen Netzwerken konfiguriert sind (also Schnittstellen wie z.B. LANs) als **passive Interfaces** markiert werden. Dies geschieht über folgenden Befehl:
```CLI
Router(config-router)# passive-interface <interface>
```

